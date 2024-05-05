```sh
helm upgrade -i confluence atlassian-data-center/confluence --namespace confluence --create-namespace  --values confluence-values.yaml
kubectl get pod -n confluence
kubectl get svc -n confluence
kubectl describe pod confluence-0 -n confluence
kubectl get ing -n confluence
kubectl get pod -n confluence -w
kubectl logs confluence-0 -n confluence

### To delete a confluence
helm uninstall confluence -n confluence
kubectl delete ns confluence

aws rds describe-db-instances --db-instance-identifier jiradb | jq '.DBInstances[].Endpoint.Address's
```