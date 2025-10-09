
# DevOps Assessment - Next.js App

## Setup Instructions

### Local Run
```bash
npm install
npm run dev
```

### Docker Run
```bash
docker build -t nextjs-app .
docker run -p 3000:3000 nextjs-app
```

### GitHub Actions
- On push to `main`, Docker image is built and pushed to GHCR.

### Minikube Deployment
```bash
minikube start
kubectl apply -f k8s/
kubectl get pods
kubectl get svc nextjs-service
```

### Access App
```bash
minikube service nextjs-service
```
