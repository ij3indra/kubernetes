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
`kubectl expose deployment nginx-deployment --port=8030 --target-port=80`

`kubectl get services`

`kubectl describe service nginx-deployment`

`kubectl delete deployment nginx-deployment`

### docker Commands
`docker exec -it imageId sh`

`hostname`

`hostname -i`

###### Build and push image to docker hub

- In below command jatindra is username of docker hub and k8-hello-app is name of directory.
- Make sure to run this command from same folder where `Dockerfile` resides.
- `latest` will be tag name. We can also add version name there.

`docker build . -t jatindra/k8-hello-app:latest`


