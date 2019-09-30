# Creating a Kubernetes (k8s) Namespace

Namespace is the way to isolate project or create a scope in kubernetes.

### Creating a namespace with kubectl
``` kubectl create namespace testing ```

### Creating a namespace with manifest file:
we can use the following manifest file to create a namespace. Learning to create kubernetes namespace using the manifest will help the beginners to become familiar with kubernetes manifest. The template is kind of same and easy too. We use the kind of Namespace for creating namespace in kubernetes.


custom-namespace.yaml

```
apiVersion: v1
kind: Namespace
metadata:
  name: dev
  labels:
    env: development
```

run:
----
``` kubectl apply -f custom-namespace.yaml```


### Deleting the kuberentes Namespace:
``` kubectl delete ns <namespace-name> ```
``` kubectl delete namespace <namespace-name> ```

If you are not sure about the name of the nameserver use the following command
``` kubectl get namespace ```
``` kubectl get ns ```

### Switching between the kubernetes Namespace
By default, the namespace is created for us named as *default*. All our resources are aligned to this namespace(default) if we don't assign namespace while creating a resources.

So, if we list the resources using the ```kubectl get``` command, It will look into default namespace. So in such scenario we also need to pass the namespace name as following
```kubectl get pods --namespace=<namespace-name>```

In case, if we don't want to pass the namespace name and want to be in that particular context than we can do the following

``` kubectl config set-context --current --namespace=<namespace-name> ```


