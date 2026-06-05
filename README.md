```bash
docker login

docker compose up --build

docker build -t dsuprunov/demo-app:1.0.1 . --no-cache

docker push dsuprunov/demo-app:1.0.1
```

```bash
helm lint ./charts/demo-app-chart

helm template demo-app ./charts/demo-app-chart --namespace demo-app

mkdir -p dist

helm package ./charts/demo-app-chart --version 0.1.1 --app-version 1.0.1 --destination dist

helm registry login registry-1.docker.io -u dsuprunov

helm push dist/demo-app-chart-0.1.1.tgz oci://registry-1.docker.io/dsuprunov
```

```bash
helm upgrade --install demo-app oci://registry-1.docker.io/dsuprunov/demo-app-chart --version 0.1.0 --namespace demo-app --create-namespace
```
