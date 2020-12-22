Поды являются статическими и управляются kubelet. При удалении пода или остановке контейнера kubelet его перезапускает. Политика описана тут:
root@minikube:/home/docker# ls -lah /etc/kubernetes/manifests/
total 28K
drwxr-xr-x 1 root root 4.0K Dec  9 14:45 .
drwxr-xr-x 1 root root 4.0K Dec  9 14:45 ..
-rw------- 1 root root 2.2K Dec  9 14:45 etcd.yaml
-rw------- 1 root root 3.8K Dec  9 14:45 kube-apiserver.yaml
-rw------- 1 root root 3.2K Dec  9 14:45 kube-controller-manager.yaml
-rw------- 1 root root 1.4K Dec  9 14:45 kube-scheduler.yaml 
CoreDNS контролируется ReplicaSet, описание можно посмотреть:
kubectl describe deployments coredns -n kube-system
