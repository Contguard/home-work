# Home-work for DEVOPS & IT POSITION

create a free azure account https://azure.microsoft.com/en-us/free/ (there shouldn't be any additional charges with this task , but we're not responsible if for some reason youre getting charged)

### getting started :  
## create a a kubernetes cluster on (AKS) (which stands in the free trial ) through the UI / CLI 

any other platform will be accepted but should be on the cloud.



___
Install `kubectl`.

connect to the cluster and show the output of : 
```
kubectl get all 
```
----

##  1. clone the repo 
```
git clone https://github.com/Contguard/home-work.git
```

## 2.  create yaml files for deployment :
```
#that will pull image's from your repo(see next step ), and will push it to the cluster 


```
---
## 3. create a workflow(s) for each service  using github-actions that does that:
 1. build's  dockerfile for each service.
 2. push the images to a container registry (dosent matter which one)
 3. deploy app .

more info can be found here https://docs.github.com/en/actions
## check that the app is functional
 ```
 tip: make sure that the dashboard service can reach the counting service when you deployed the app,
      the address to it may be different .
      so make sure to set right the value of : 
      ENV COUNTING_SERVICE_URL 
 ```




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
## it may be easier if you test everything manually, and then move each step, to the workflow (for your choice).
## dont hesitate to ask any questions  .
## take 3 days for the task .
## clean everything ! &  send me a link to the repo / zip file.

good luck! 
