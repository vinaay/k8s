# RBAC 

## Roles and ClusterRoles:

- Role: Grants permissions within a specific namespace.
- ClusterRole: Grants permissions cluster-wide or can be used in any namespace.

## RoleBinding and ClusterRoleBinding:

- RoleBinding: Associates a Role with a user, group, or service account within a specific namespace.
- ClusterRoleBinding: Associates a ClusterRole with a user, group, or service account at the cluster level.

- Define who the permissions apply to. Subjects can be:
Users
Groups
Service Accounts

## Resources and Verbs:
- Resources: Kubernetes objects (e.g., pods, services, deployments).
- Verbs: Actions that can be performed on resources (e.g., get, list, create, delete).



How to check permission 

````
kubectl auth can-i <verb> <resource> --as=<user>

kubectl auth can-i list pods --as=system:serviceaccount:my-namespace:my-service-account 


kubectl auth can-i list pods --as=system:serviceaccount:my-namespace:my-service-account -n my-namespace


kubectl run my-pod --image=nginx:latest --restart=Never --as=system:serviceaccount:my-namespace:my-service-account

kubectl run my-pod --image=nginx:latest --restart=Never --as=system:serviceaccount:my-namespace:my-service-account -n my-namespace




````
