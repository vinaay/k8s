# Volumes

volumes are a way to provide data storage that can persist across container restarts or share data between containers in the same pod. Kubernetes volumes can integrate with a wide range of storage backends, including cloud storage services, local disks, and networked storage systems.


1. EmptyDir
- Description: A temporary directory that is created when a pod is assigned to a node. The data persists only as long as the pod runs on that node.
- Use Case: Temporary scratch space, caching, or sharing data between containers in a pod.
- Key Feature: Data is lost if the pod is deleted or rescheduled.


2. HostPath
- Description: Mounts a file or directory from the host node’s filesystem into a pod.
- Use Case: Accessing files on the node (e.g., system logs or host configuration files).
- Key Feature: Tied to the specific node hosting the pod.


3. PersistentVolumeClaim (PVC)
- Description: Dynamically or statically allocates persistent storage that can survive pod restarts and rescheduling.
- Use Case: Long-term storage, databases, or any application requiring persistent data.
- Key Feature: Abstracts storage details, integrates with cloud and on-prem storage.


4. ConfigMap
- Description: Provides configuration data as files or environment variables.
- Use Case: Storing non-sensitive configuration data such as application settings.

5. Secret
- Description: Stores sensitive data (e.g., passwords, tokens) as files or environment variables.
- Use Case: Handling credentials securely.


6. NFS (Network File System)
- Description: Mounts a remote NFS share into the pod.
- Use Case: Shared storage between multiple pods.


7. AWS EBS (Elastic Block Store)
- Description: Mounts an AWS EBS volume into a pod.
- Use Case: Persistent storage for applications running on AWS.
- Key Feature: Works only with pods scheduled on AWS nodes.

8. Azure Disk
- Description: Mounts an Azure managed disk into a pod.
- Use Case: Persistent storage for workloads on Azure.
