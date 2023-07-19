kubectl run nginx --image=nginx -o yaml --dry-run=client > nginx-pod.yml
kubectl expose pod nginx --port=80 --type=NodePort --name=webserver -o yaml --dry-run=client > nginx-svc.yml
