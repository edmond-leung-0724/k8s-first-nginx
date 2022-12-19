# k8s-first-nginx

  143  kubectl create -f nginx-pod.yaml
  144  kubectl get pod
  145  kubectl get pod -A
  146  kubectl get pod -o wide
  147  kubectl get pod nginx-pod -o yaml
  148  kubectl describe pod nginx-pod
  149  ls
  150  cat nginx-pod.yaml
  151  kubectl get pod -A
  152  ls
  153  cat nginx-pod.yaml
  154  kubectl exec -it nginx-pod -- /bin/sh
  155  kubectl get svc
  156  kubectl expose pod nginx-pod --type=NodePort --port=80
  157  kubectl get svc
  158  kubectl get nod -A
  159  kubectl get node -A
  160  kubectl get node -A -o wide
  161  kubectl describe svc nginx-pod
  162  kubectl get svc
  163  kubectl delete svc nginx-pod
  164  kubectl get pod -A
  165  kubectl delete pod nginx-pod
  166  kubectl get pod -A
  167  kubectl get po -A
