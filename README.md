# home-work
create a free azure account https://azure.microsoft.com/en-us/free/ (there shouldnt be any additional charges with this task , but we're not responsible if for some reason youre getting charged)

### create a a kubernetes cluster on (AKS) (which stands in the free trial ) through the UI / CLI 


```

Install  and `kubectl`.

connect to the cluster and show it (e.g. attach here output of : kubectl get all )





### Create minimal yaml config

Here is the simplest configuration that will deploy a container. Create a file named `counting-minimal.yaml` and paste these
contents into it.

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: counting-minimal-pod
  labels:
    app: counting
spec:
  containers:
    - name: counting
      image: hashicorp/counting-service:0.0.1
      ports:
      - containerPort: 9001
```

Connect to the pod from your local machine.

```sh
$ kubectl port-forward pod/counting-minimal-pod 9001:9001
```

Now visit http://localhost:9001/

You should see JSON that contains a number and the name of the host.



service/counting-minimal-load-balancer created
```

Visit the Google Cloud console and go to "Services." You will see a service of type "Load Balancer" with an IP address
next to it. Click the IP address and you'll see JSON output from the counting service.

```json
{"count":1,"hostname":"counting-minimal-pod"}
```

### Gather data

```sh
$ kubectl get pods
```

```sh
$ kubectl logs counting-minimal-pod

Serving at http://localhost:9001
(Pass as PORT environment variable)
```

```sh
$ kubectl get pods --output=json
```

Connect to a running pod.

```sh
$ kubectl exec -it counting-minimal-pod /bin/sh
```

Run commands like `env` or try to start `counting-service` manually with a different port.

```sh
$ PORT=9002 ./counting-service
```




In order for Consul service discovery to work, we need to enable Consul within the Kubernetes DNS system. See the
[documentation](https://www.consul.io/docs/platform/k8s/dns.html) for details.

Run the stub DNS script in this demo repo. This script will add a [Stub-domain](https://kubernetes.io/docs/tasks/administer-cluster/dns-custom-nameservers/)
config map entry for the Consul DNS server.

```sh
$ bin/enable-consul-stub-dns.sh
configmap/kube-dns configured
```

binding admin --clusterrole=admin --user="system:serviceaccount:default:default" --namespace=default
```
