## Configmaps

How to work with configuration data in Kubernetes?

We can define environment variables in the  pod  definition file.  when you have a lot of pod definition files it become difficult to manage the environment data. So we can take this data out of the pod definition files and manage it centrally using configuration Maps.

Config Maps are used to pass configuration data in the form of key value pairs.  When a pod is created inject the config map into the pod.   Now the key value pairs are available as environment variables for the application, -hosted inside the container in the pod, to use.

There are two steps
* Create a config map
* Inject the configmap into the pod.

Like other K8s objects we can create configmaps imperatively or declaratively.

```
kubectl create configmap \
> app-config --from-literal=APP_COLOR=blue
```

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
    
 kubectl get configmaps
 kubectl describe configmaps
 
 
