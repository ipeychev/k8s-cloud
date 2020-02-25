Based on: https://github.com/kubernetes/examples/tree/f3d89d074fe992d12adb54ad9859a68fe1e1e082/staging/volumes/nfs

Changes:
1. ReplicationController was changed to be a Deployment
2. A few labels were renamed


Deployment:
1. kubectl apply -f k8s-nfs-server-pvc.yaml
2. kubectl apply -f k8s-nfs-server-deployment.yaml
3. kubectl apply -f k8s-nfs-server-service.yaml

Get the Server IP by executing:

1. kubectl get services and get the IP of the `nfs-server`
2. Replace the IP in `k8s-nfs-pv.yaml` with those from 1)
3. Deploy:
 - kubectl apply -f k8s-nfs-pv.yaml
 - kubectl apply -f k8s-nfs-pvc.yaml