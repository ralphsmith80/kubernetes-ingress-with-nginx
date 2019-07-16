# kubernetes-ingress-with-nginx

# Ingress-nginx

- [guide](https://matthewpalmer.net/kubernetes-app-developer/articles/kubernetes-ingress-guide-nginx-example.html)
- [ingress-nginx](https://kubernetes.github.io/ingress-nginx/deploy/)
- [ingress-nginx github](https://github.com/kubernetes/ingress-nginx/blob/master/docs/deploy/index.md#docker-for-mac)
- `kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/mandatory.yaml`
- (Docker for Mac) `kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/provider/cloud-generic.yaml`
- Detect installed version

  ```
  POD_NAMESPACE=ingress-nginx
  POD_NAME=$(kubectl get pods -n $POD_NAMESPACE -l app.kubernetes.io/name=ingress-nginx -o jsonpath='{.items[0].metadata.name}')
  kubectl exec -it $POD_NAME -n $POD_NAMESPACE -- /nginx-ingress-controller --version
  ```

- [ingress-nginx using helm](https://kubernetes.github.io/ingress-nginx/deploy/#using-helm)
- [setup ingress]https://kubernetes.io/docs/tasks/access-application-cluster/ingress-minikube/()
