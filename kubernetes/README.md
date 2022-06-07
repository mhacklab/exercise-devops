# Kubernetest basic deploy

## Solution

In order to deploy application in kubernetes cluster you should change 
`containers image registry` to your docker image repository in `deploy.yaml` file. 
Then deploy it to kubernetes with a follwoing command 

```
kubectl apply -f 

```
In order to provide an URL to access /hello endpoint from outside the Kubernetes cluster,
please implement nginx-ingress and make change to `host: <your_domain>` to our domain.
After that please deploy it to kubernetes with a follwoing command:

```
kubectl apply -f 

```
