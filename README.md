# K8s

## Pod

- Abstraction over container.
- 1 app per Pod.
- Each Pod get its own IP adds.

### Service

- Static IP adds to attach to Pod.
- Type:
    - External service (Ingress).
    - Internal service.

### ConfigMap

- External configuration of your app.
- Ex: db service name.

### Secret

- Use to store secret data (Ex: password).
- base64 encoded.

### Volumes

- Attach storage to Pod.
- Data persistance . 
- Storage can be local, remote of outside of the K8s cluster.

### Deployment
- Define blueprints for Pods, ex: number of Pods need to replicate.
- Can config the scale.
- Abtraction of Pods.

### StatefulSet
- For stateful apps like ElasticSearch, DB.
- Use StatefulSet (not Deployment) for stateful apps.
- No recommended, not easy to use.


## Refs (22:01):
- https://www.youtube.com/watch?v=X48VuDVv0do&t=1358s