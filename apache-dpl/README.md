create deployment:
kubectl create deploy apache --image=httpd -o yaml --dry-run=client > apache-dpl.yaml
kubectl apply -f apache-dpl.yaml

Expose Deploymenr:
kubectl expose deploy apache --port=80 --type=LoadBalancer --name=apache-webserver -o yaml --dry-run=client > apache-svc.yaml
kubectl apply -f apache-svc.yaml


scaleup a deployment:
kubectl scale deploy apache --replicas=2