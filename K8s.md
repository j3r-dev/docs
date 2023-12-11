- [K9s](https://github.com/derailed/k9s#readme)
```
curl -sS https://webinstall.dev/k9s | bash
```
- [Minikube](https://github.com/kubernetes/minikube#readme)

- Run debian container with bash open
```
kubectl run j3r-test -n <namespace> --rm -i --tty --image debian -- bash
```

- Create proxy to contact PG db inside the network
```
kubectl run postgres-proxy -n <namespace> --image docker.io/alpine/socat -- tcp-listen:5432,fork,reuseaddr tcp-connect:<db-host-url>:5432

kubectl port-forward pod/postgres-proxy 5432:5432 -n <namespace>
```
