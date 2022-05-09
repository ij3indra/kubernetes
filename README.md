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

### docker Commands
`docker exec -it imageId sh`
`hostname`
`hostname -i`
