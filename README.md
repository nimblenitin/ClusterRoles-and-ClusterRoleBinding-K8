# ClusterRoles-and-ClusterRoleBinding-K8
ClusterRole is a non-namespaced resource that can be used to grant permission across cluster. A RoleBinding grants permissions within a specific namespace whereas a ClusterRoleBinding grants that access cluster-wide.

Simple example to demonstrate ClusterRole and ClusterRoleBinding-

Steps followed:

*As Root*
```

1. Create the ClusterRole and ClusterRoleBinding
$ vi clusterRole.yaml
$ vi clusterRoleBinding.yaml
$ kubectl apply -f clusterRole.yaml
$ kubectl apply -f clusterRoleBinding.yaml

2. Verify the access
$ kubectl auth can-i create node --as cluster-admin --namespace kube-system
$ kubectl auth can-i delete node --as cluster-admin
$ kubectl auth can-i create pods --as cluster-admin --namespace kube-system

```
*As Root*
