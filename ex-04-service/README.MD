# Creating the kubernetes Service 
Here, We will see how we can create a service for the nginx deployment we have created in exercise 04. 

## clusterType:
  Here, we will be using the service type of ClusterIP , there are other options like NodePort too. Will see in more details about it in later chapter.

### Getting the cluster created

``` kubectl get svc ```
     or
``` kubectl get service ```
