## Kubernetes Commands

###### To pull nginx image from docker

`kubectl run nginx --image=nginx`

`kubectl get pods`

`kubectl describe pod nginx`

`kubectl get pods -o wide`

`kubectl delete pod nginx`

###### To create a deploymeny
`kubectl create deploymeny nginx-deployment --image=nginx`

`kubectl get deployments`

`kubectl scale deployment nginx-deployment --replicas=3`

###### To expose internal deployment port to external port

Create ClusterIp service with type ClusterIp

`kubectl expose deployment nginx-deployment --port=8030 --target-port=80`

Create ClusterIp service with type NodePort

`kubectl expose deployment nginx-deployment --type=NodePort --port=8030`

Create ClusterIp service with type NodePort

`kubectl expose deployment nginx-deployment --type=LoadBalancer --port=8030`

`kubectl get services`

`kubectl describe service nginx-deployment`

`kubectl delete deployment nginx-deployment`

New docker image version rollout to current k8s deployment

`kubectl set image deployment nginx-deployment nginx-deployment=jatindra/jatindra/k8-hello-app:0.0.2`

Check the deployment status with

`kubectl rollout status deploy nginx-deployment`

### docker Commands
`docker exec -it imageId sh`

`hostname`

`hostname -i`

### To delete all

This will delete pods, deployment and services

`kubectl delete all --all`

### Deploymenmt using deployment/service specification file

`kubectl apply -f deployment.yaml`

`kubectl apply -f service.yaml`

`kubectl delete -f deployment.yaml -f service.yaml`

###### Build and push image to docker hub

- In below command jatindra is username of docker hub and k8-hello-app is name of directory.
- Make sure to run this command from same folder where `Dockerfile` resides.
- `latest` will be tag name. We can also add version name there.
- `docker build . -t jatindra/k8-hello-app`
- `docker login`
- `docker push jatindra/k8-hello-app`


