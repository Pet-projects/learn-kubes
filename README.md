# learn-kubes

Performing role based auth using bearer token
```
kubectl describe secret
TOKEN="x"
curl --insecure --header "Authorization: Bearer $TOKEN" https://192.168.99.100:8443/api/v1/namespaces/kube-system/services/http:kubernetes-dashboard:/proxy/#!/role?namespace=kube-system
```

Performing role based auth using TLS
```
cat ~/.kube/config
curl --cacert /Users/julianghionoiu/.minikube/ca.crt --cert  /Users/julianghionoiu/.minikube/client.crt --key /Users/julianghionoiu/.minikube/client.key https://192.168.99.100:8443/api/v1/namespaces/kube-system/services/http:kubernetes-dashboard:/proxy/#!/role?namespace=kube-system
```
