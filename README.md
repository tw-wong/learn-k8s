# K8s

[Mindmap](https://raw.githack.com/tw-wong/learn-k8s/master/mindmap.html)

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


## Node

### Type
#### Master node

##### 4 Processes required
- Api Server: cluster gateway, authentication (gatekeeper).

- Scheduler: Check node resources, decide which node new Pod should be scheduled (ex: start Pod).
    - send request to Kubelet.

- Controller manager: detects cluster state changes (ex: Pod die), reschedule it when necessary.
    - send request to Scheduler.

- etcd: Key value store for cluster state.


#### Worker node

##### 3 Processes required

- Kubelet: interface to interacts with both container and node.
- Kube proxy: forwards the requests.
- Container runtime.

## Cluster setup

### Basic architecture
- 2 Master node, 3 worker nodes.
- Master node should have lower spec (CPU, RAM) compare with Worker node.

### Minikube and Kubectl

## Refs (34:50):
- https://youtu.be/X48VuDVv0do?t=2090