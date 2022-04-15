## Install kubernetes dashboard using Helm Chart
1. helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/
2. helm repo update
3. helm show values kubernetes-dashboard/kubernetes-dashboard > kubernetes-dashboard-values.yaml
4. helm install kubernetes-dashboard kubernetes-dashboard/kubernetes-dashboard -n kubernetes-dashboard --values kubernetes-dashboard-values.yaml --create-namespace

