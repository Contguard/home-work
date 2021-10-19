# home-work
create a free azure account https://azure.microsoft.com/en-us/free/ (there shouldnt be any additional charges with this task , but we're not responsible if for some reason youre getting charged)

### create a a kubernetes cluster on (AKS) (which stands in the free trial ) through the UI / CLI 
# any other platform will be accepted but should be on the cloud.


```

Install `kubectl`.

connect to the cluster and show it (e.g. attach here output of : kubectl get all )

```
## clone the repo 
## create a Dockerfile for each service (dashboard-service and counting-service)
---
create a workflow (using github-actions) which build's the app's . push the images to a container registry .  & deploy the applications to the cluster.

```
attach a screen shot of the dashboard service . check that each refresh the counter incerment's .


### clean everything ! send me a link to the repo . 

### BONUS :

1. add a nginx ingress controller with an ingress rule in order to have external acceess to the dashboard service.
2. add a helm chart for the app
3. feel free to show more skills .. :)

### important 
# the code for the service's is taken from hashicorp github repo . so you may find more info that can help you to complete the task.
# all files should be included in the repo. (Dockerfile & yaml etc..)
# as mentioned , there shoudnt be any charge  but we're not responsible for any charges .