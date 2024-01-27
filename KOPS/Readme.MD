# Kubernetes-Zero-to-Hero


kubectl version --short
kubectl get nodes
kubectl get nodes --no-headers
kubectl cluster-info
kubectl cluster-info dump
kubectl get ns
kubectl config set-context --current --namespace=default
kubectl get pods
kubectl get pods -n kube-system
ku describe pod kube-apiserver-ip-172-20-114-198.ec2.internal -n kube-system
ku logs kube-apiserver-ip-172-20-114-198.ec2.internal -c  kube-apiserver -n kube-system
kubectl get service -A

kubectl run pod01 --image=sreeharshav/rollingupdate:v5
kubectl expose pod pod01 --port=8000 --target-port=80 --type=NodePort
kubectl get pods -o wide
kubectl get pods -o wide --no-headers
kubectl create deployment deploy01 --image=sreeharshav/rollingupdate:v5 --dry-run -o yaml
kubectl create deployment deploy01 --image=sreeharshav/rollingupdate:v5 --replicas 3
kubectl scale deployment deploy01 --replicas=6
ku cordon ip-172-20-103-135.ec2.internal
ku drain ip-172-20-103-135.ec2.internal
ku drain  ip-172-20-38-30.ec2.internal
ku uncordon ip-172-20-103-135.ec2.internal

