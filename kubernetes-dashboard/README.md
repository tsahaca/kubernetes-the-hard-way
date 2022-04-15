## Install kubernetes dashboard using Helm Chart
. helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/
. helm repo update
. helm show values kubernetes-dashboard/kubernetes-dashboard > kubernetes-dashboard-values.yaml
. helm install kubernetes-dashboard kubernetes-dashboard/kubernetes-dashboard -n kubernetes-dashboard --values kubernetes-dashboard-values.yaml --create-namespace

