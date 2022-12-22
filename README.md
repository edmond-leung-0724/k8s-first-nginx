# k8s-first-nginx

1) Create Nginx Pod

kubectl create -f nginx-pod.yaml
 
2) Check Pod status

kubectl get pod -A
  
kubectl get pod -o wide
  
kubectl get pod nginx-pod -o yaml
  
kubectl describe pod nginx-pod
  
3) Connect to the pod

kubectl get pod -A

kubectl exec -it nginx-pod -- /bin/sh
  
cd /usr/share/nginx/html
  
echo "testing pages" > test.html
  
exit

4) Expose Pod by create NodePort service

kubectl expose pod nginx-pod --type=NodePort --port=80

5) Check the port number of the Node Port (for example 30547)

kubectl get svc
  
kubectl describe svc nginx-pod
  
6) Open the browser and check whehter can access the test page by master-node-ip/worker-node-ip
  
http://master-node-ip:30547/test.html or http://worker-node-ip:30547/test.html

curl http://master-node-ip:30547/test.html or curl http://worker-node-ip:30547/test.html 

7) Remote the service and Pod

kubectl delete pod nginx-pod
  
kubectl delete svc nginx-pod
  
kubectl get pod -A
  
kubectl get svc -A
  
