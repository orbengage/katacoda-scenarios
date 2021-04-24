## Configmaps

How to work with configuration data in Kubernetes?

We can define environment variables in the  pod  definition file.  when you have a lot of pod definition files it become difficult to manage the environment data. So we can take this data out of the pod definition files and manage it centrally using configuration Maps.

Config Maps are used to pass configuration data in the form of key value pairs.  When a pod is created inject the config map into the pod.   Now the key value pairs are available as environment variables for the application, -hosted inside the container in the pod, to use.

There are two steps
* Create a config map
* Inject the configmap into the pod.

Like other K8s objects we can create configmaps imperatively or declaratively.

 In the imperative method you can use the  kubectl create configmap map command and specify the required arguments.  In this method you can directly specify the key value pairs in the command line. 

We are creating a config map by the name app config with a key value pair of app color equals blue if you wish to add additional key value pairs simply specify the from literal options multiple times.

We specify a name for the config map we will call it app config under data and the configuration data in a key value format for on the  that creates the app config config map with the values we specified.


```
kubectl create configmap \
> app-config --from-literal=APP_COLOR=blue
```

This will get complicated when you have many configuration items. So another way to input configuration data is through a file.  use the from file option to specify a path to the file that contains the required data.


kubectl create configmap \
  app-config --from-file=app_config.properties
  
  app_config.properties
  
  config-map.yaml
  
  apiVersion: v1
  kind : ConfigMap
  metadata:
    name: app-config
  data:
     APP_COLOR: blue
     APP_MODE: prod
    
    
    kubectl create -f config-map.yaml
 
 ### to view config Maps run the cube control get config Maps

 kubectl get configmaps
 
 ### To list the configuration data
 
 kubectl describe configmaps
 
 
 
 
