# Basic Kubernetes Commands for troubleshooting

To view all nodes in cluster:

```bash
$ kubectl get nodes
```

To view the running containers in current namespace:

```bash
$ Kubectl get pods -o wide
```

To view all pods (containers):

```bash
$ Kubectl get pods --all-namespaces
```
To view all namespaces:

```bash
$ Kubectl get namespaces
```

To view the logs for a specific container:

```bash
$ kubectl logs -f pod name
```

To view the configuration for a specific container:

```bash
$ kubectl describe pods/pod name
```

To enter a bash shell of a container:

```bash
$ kubectl exec -ti pod name -- /bin/sh
$ exit
```