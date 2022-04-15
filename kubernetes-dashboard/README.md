## Install kubernetes dashboard using Helm Chart
1. helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/
2. helm repo update
3. helm show values kubernetes-dashboard/kubernetes-dashboard > kubernetes-dashboard-values.yaml
4. helm install kubernetes-dashboard kubernetes-dashboard/kubernetes-dashboard -n kubernetes-dashboard --values kubernetes-dashboard-values.yaml --create-namespace
5. kubectl apply -f dashboard-admin-sa.yaml
6. kubectl apply -f dashboard-role-binding.yaml
7. get the token
8. ```
9. kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/dashboard-admin -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"
10. ```

