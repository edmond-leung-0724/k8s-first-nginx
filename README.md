# k8s-first-nginx

  kubectl create -f nginx-pod.yaml
  
  kubectl get pod -A
  
  kubectl get pod -o wide
  
  kubectl get pod nginx-pod -o yaml
  
  kubectl describe pod nginx-pod
  
  
  kubectl get pod -A
  
  kubectl exec -it nginx-pod -- /bin/sh
  
  kubectl get svc
  
  kubectl expose pod nginx-pod --type=NodePort --port=80
  
  kubectl get svc
  
  kubectl describe svc nginx-pod
  
   
  kubectl delete svc nginx-pod
  
  

  kubectl delete pod nginx-pod
  
  kubectl get pod -A
  
