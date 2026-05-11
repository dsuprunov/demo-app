```bash
docker login dhi.io

docker compose up --build

docker build -t dsuprunov/demo-app:latest . --no-cache

docker push dsuprunov/demo-app:latest
```