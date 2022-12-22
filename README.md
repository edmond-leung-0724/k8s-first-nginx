# k8s-first-nginx

1) Create Nginx Pod

kubectl create -f nginx-pod.yaml
 
2) Check Pod status
kubectl get pod -A
  
  kubectl get pod -o wide
  
  kubectl get pod nginx-pod -o yaml
  
  kubectl describe pod nginx-pod
  
  
  kubectl get pod -A
  
  kubectl exec -it nginx-pod -- /bin/sh
  
  cd /usr/share/nginx/html
  
  echo "testing pages" > test.html
  
  exit
  
    kubectl expose pod nginx-pod --type=NodePort --port=80
  
  kubectl get svc
  
  kubectl describe svc nginx-pod
  
  Open the browser and check whehter can access the test page by master-node-ip/worker-node-ip
  
  http://master-node-ip:30547/test.html or http://worker-node-ip:30547/test.html

  kubectl delete pod nginx-pod
  
  kubectl delete svc nginx-pod
  
  kubectl get pod -A
  
  kubectl get svc -A
  
