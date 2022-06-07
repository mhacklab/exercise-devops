# Kubernetest basic deploy

## Solution

In order to deploy application in kubernetes cluster you should change 
`containers image registry` to your docker image repository in `deploy.yaml` file. 
Then deploy it to kubernetes with a follwoing command 

```
kubectl apply -f deploy.yaml

```
In order to provide an URL to access /hello endpoint from outside the Kubernetes cluster,
please implement nginx-ingress and make change to `host: <your_domain>` line in ingress.yaml file to your domain.
After that please deploy it to kubernetes with a follwoing command:

```
kubectl apply -f ingress.yaml

```
## WORKING EXAMPLE 

Working example of app deployed in kubernetees cluster can be find under following address:

`67.207.73.1.nip.io`

Which can be accessed with following command :

```
curl http://67.207.73.1.nip.io/hello

```

