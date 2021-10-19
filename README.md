# Home-work for DEVOPS & IT POSITION

create a free azure account https://azure.microsoft.com/en-us/free/ (there shouldnt be any additional charges with this task , but we're not responsible if for some reason youre getting charged)

### getting started :  
## create a a kubernetes cluster on (AKS) (which stands in the free trial ) through the UI / CLI 

any other platform will be accepted but should be on the cloud.



___
Install `kubectl`.

connect to the cluster and show it e.g. attach here output of : 
```
kubectl get all 
```
----

##  1 clone the repo 
```
git clone https://github.com/Contguard/home-work.git
```

## 2  create yaml files
 that will pull image's from your repo, and will push it to the cluster 
---
## create a workflow(s) for each service  using github-actions that does that:
 1. build's  dockerfile for each service.
 2. push the images to a container registry (dosent matter which one)

3. deploy app .
## check that the app is functional





determine the svc name . 
```
kubectl get svc
```

use " kubectl port-forward ... " then youll be able to reach service on your localhost.

attach a screen shot of the dashboard service . check that by refreshing the page ,  the counter incerment's  .

### BONUS :

1. add a nginx ingress controller with an ingress rule in order to have external acceess to the dashboard service.
2. add a helm chart for the app
3.use cert-manger to add ssl cert for the dashboard app.
4. (hard one) build the app from source
5. feel free to show more skills .. :)

----
 important: 
the code for the service's is taken from hashicorp github repo . so you may find more info that can help you to complete the task.
 all files created for the task should be included in the repo. 
please add some documents the showing the proccess . 
as mentioned , there shoudnt be any charge  but we're notresponsible for any charges .

## dont hesitate to ask any questions  .
## take 3 days for the task .
## clean everything ! &  send me a link to the repo / zip file.

good luck! 
