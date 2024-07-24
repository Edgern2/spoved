
# I love DevOps

## 1. Create Namespace

```sh
kubectl create namespace my-namespace
```
*Creates a namespace called `my-namespace`*

```sh
kubectl run nginx --image=nginx -n my-namespace
```
*Creates an nginx pod in `my-namespace`*

## 2. Create and Expose Pods

```sh
kubectl run nginx1 --image=nginx
```
*Creates an nginx pod in the default namespace*

```sh
kubectl expose pod nginx1 --port=8080
```
*Exposes port 8080*

## 3. Create Pod with Environment Variable

```sh
kubectl run nginx2 --image=nginx --env="var1=val1"
```
*Creates an nginx pod in the default namespace with an environment variable `var1` set to `val1`*

## 4. Create and Scale Deployments
```sh
kubectl create deployment {name} --image=nginx
```
*Creates a deployment with the image nginx*

```sh
kubectl scale deployment {name} --replicas=3
```
*makes 3 replicas for the deployment*

## 5. Create Secret

```sh
kubectl create secret generic my-secret --from-literal=passcode=Ilovekubernetes!
```
*Creates a secret called `my-secret` with a key `passcode` set to `Ilovekubernetes!`*

## 6. Create ConfigMap

```sh
kubectl create configmap my-configmap --from-literal=var1=val2
```
*Creates a ConfigMap called `my-configmap` with a key `var1` set to `val2`*
