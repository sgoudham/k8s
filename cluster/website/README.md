# Setup

1. `kubectl create namespace website`
2. `kubectl create deployment website --image sgoudham/website:latest --port 3000`
3. `kubectl expose deployment website --port 3000`
4. `kubectl create ingress website --rule=goudham.com/\*=website:3000,tls`
5. `kubectl get deployment.apps website -o yaml > deployment.yaml`
6. `kubectl get services website -o yaml > service.yaml`
7. `kubectl get ingress website -o yaml > ingress.yaml`