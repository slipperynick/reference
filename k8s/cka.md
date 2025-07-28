# Certified Kubernetes Administrator (CKA) Exam Command Reference

## Core Concepts
- **View Resources in a Specific Namespace**  
  `kubectl get pods -n <namespace>`
- **View All Pods Across All Namespaces**  
  `kubectl get pods -A`
- **View All Resources Across All Namespaces**  
  `kubectl get all -A`
- **Generate a Pod YAML File with Specific Labels**  
  `kubectl run nginx --image=nginx --labels=env=prod --dry-run=client -o yaml > nginx_pod.yaml`
- **Delete a Pod Immediately**  
  `kubectl delete pod nginx --grace-period=0 --force`
- **Generate a Deployment YAML File**  
  `kubectl create deployment nginx --image=nginx --dry-run=client -o yaml > nginx-deployment.yaml`
- **Expose a Pod as a Service**  
  `kubectl expose pod valid-pod --port=444 --name=frontend`
- **Replace a Resource Using a YAML File**  
  `kubectl replace --force -f nginx.yaml`
- **Edit an Existing Deployment**  
  `kubectl edit deployment nginx`
- **Update the Image of a Deployment**  
  `kubectl set image deployment/nginx nginx=nginx:1.18`
- **Scale a Deployment**  
  `kubectl scale deployment/nginx --replicas=4 --record`
- **Retrieve Cluster Events**  
  `kubectl get events`

## Scheduling
- **Display Pods with Their Labels**  
  `kubectl get pods --show-labels`
- **Filter Pods by Label**  
  `kubectl get pods -l env=dev`
- **Describe Node Taints**  
  `kubectl describe node node01 | grep -i taints`
- **Label a Node**  
  `kubectl label node node01 env=production`
- **Taint a Node**  
  `kubectl taint node node01 key=value:NoSchedule`
- **Remove a Taint from a Node**  
  `kubectl taint node node01 key=value:NoSchedule-`

## Networking & Services
- **List Services in a Namespace**  
  `kubectl get svc -n <namespace>`
- **Get Cluster IP of a Service**  
  `kubectl get svc <service-name> -o wide`
- **Describe a Service**  
  `kubectl describe svc <service-name>`
- **Expose a Deployment as a LoadBalancer Service**  
  `kubectl expose deployment nginx --type=LoadBalancer --port=80`
- **Port Forward a Pod Locally**  
  `kubectl port-forward pod/nginx 8080:80`
- **Get Ingress Resources**  
  `kubectl get ingress`
- **Describe an Ingress**  
  `kubectl describe ingress <ingress-name>`
- **Apply an Ingress Rule**  
  `kubectl apply -f ingress.yaml`
- **Delete an Ingress**  
  `kubectl delete ingress <ingress-name>`

## Persistent Volumes & Storage
- **List Persistent Volumes**  
  `kubectl get pv`
- **List Persistent Volume Claims**  
  `kubectl get pvc`
- **Describe a Persistent Volume**  
  `kubectl describe pv <pv-name>`
- **Describe a Persistent Volume Claim**  
  `kubectl describe pvc <pvc-name>`
- **Delete a Persistent Volume Claim**  
  `kubectl delete pvc <pvc-name>`

## Security & Access Control
- **View Service Accounts**  
  `kubectl get serviceaccounts`
- **Describe a Service Account**  
  `kubectl describe serviceaccount <serviceaccount-name>`
- **Get Role Bindings**  
  `kubectl get rolebindings`
- **Describe a Role Binding**  
  `kubectl describe rolebinding <rolebinding-name>`
- **Get Cluster Roles**  
  `kubectl get clusterroles`
- **Describe a Cluster Role**  
  `kubectl describe clusterrole <clusterrole-name>`

## Logs & Monitoring
- **View Logs from a Pod**  
  `kubectl logs <pod-name>`
- **View Logs from a Specific Container**  
  `kubectl logs <pod-name> -c <container-name>`
- **Watch Logs in Real-Time**  
  `kubectl logs -f <pod-name>`
- **View Resource Usage for Pods**  
  `kubectl top pod`
- **View Resource Usage for Nodes**  
  `kubectl top node`

## Debugging & Troubleshooting
- **Get Events in the Cluster**  
  `kubectl get events`
- **Describe a Pod for Debugging**  
  `kubectl describe pod <pod-name>`
- **Check a Node's Status**  
  `kubectl get nodes -o wide`
- **Restart a Deployment**  
  `kubectl rollout restart deployment/<deployment-name>`
- **Run a Debugging Pod**  
  `kubectl run -i --tty busybox --image=busybox -- sh`

## Backup & Restore
- **Backup etcd**  
  `ETCDCTL_API=3 etcdctl snapshot save /opt/etcd-backup.db --endpoints=<etcd-endpoint> --cacert=/etc/kubernetes/pki/etcd/ca.crt --cert=/etc/kubernetes/pki/etcd/server.crt --key=/etc/kubernetes/pki/etcd/server.key`
- **Restore etcd**  
  `ETCDCTL_API=3 etcdctl snapshot restore /opt/etcd-backup.db --data-dir /var/lib/etcd-from-backup`

## Helm Commands
- **List Installed Helm Charts**  
  `helm list`
- **Install a Helm Chart**  
  `helm install <release-name> <chart-name>`
- **Uninstall a Helm Chart**  
  `helm uninstall <release-name>`
- **Upgrade a Helm Chart**  
  `helm upgrade <release-name> <chart-name>`
- **Rollback a Helm Release**  
  `helm rollback <release-name> <revision>`

## Context & Config Management
- **View Current Context**  
  `kubectl config current-context`
- **Change the Current Context**  
  `kubectl config use-context <context-name>`
- **List All Contexts**  
  `kubectl config get-contexts`
- **Delete a Context**  
  `kubectl config delete-context <context-name>`

## Autoscaling
- **Enable Horizontal Pod Autoscaling**  
  `kubectl autoscale deployment <deployment-name> --cpu-percent=80 --min=2 --max=10`
- **View Autoscalers**  
  `kubectl get hpa`

## Summary
This **CKA exam cheat sheet** covers **core Kubernetes administration tasks** including:
- **Cluster & Namespace Management**
- **Pods, Deployments, and Services**
- **Security, Logs, and Debugging**
- **Networking & Storage**
- **Helm & Autoscaling**



## `kubectl patch` 
- Update a Kubernetes resource by applying a partial update to its configuration. 


## `kubectl rollout restart`
- **Restarts** a Deployment, StatefulSet, or DaemonSet **without downtime**.
- **Triggers a rolling restart** by updating the **Pod template hash**.
- **Useful for**:
  - Applying changes to **environment variables**.
  - Updating **ConfigMaps** or **Secrets** without deleting Pods.
  - Restarting applications **gracefully**.


## `kubectl drain`
- Purpose: Evacuates all workloads from a node before maintenance (e.g., upgrades, scaling, or decommissioning).
- How it Works:
  - Cordons the node (prevents scheduling new pods).
  - Evicts running pods from the node (if controlled by a ReplicaSet, StatefulSet, etc.).
  - Taints the node (optional, for preventing rescheduling).
  - e.g. `kubectl drain my-node --ignore-daemonsets --delete-emptydir-data`


## `kubectl uncordon`
-  Purpose: Re-enables scheduling on a node after it was drained.
- How it Works:
  - reverses the kubectl drain operation.
  - Removes the cordon (which marks the node as unschedulable).
  - Allows new pods to be scheduled on the node.


## `kubectl rollout undo`
- Rolls back a Deployment, StatefulSet, or DaemonSet to its previous version.
- e.g `kubectl rollout undo deployment web-app`

## `kubectl delete pod`
- Deletes a pod immediately, but it will be replaced if managed by a controller (e.g., Deployment).

## `kubectl create job example-job --image=busybox -- echo "Hello, Kubernetes!"`
- create a job that says hello, kubernetes with image busybox

## `kubectl get priorityclass`
- get the priority classes currently in use by the cluster


kubectl get priorityclass [name] -o yaml
check for details of priority class




## Q&A
- What is a headless service?
  - A headless service is a Kubernetes Service without a cluster IP. Instead of load balancing traffic, it directly returns the IP addresses of the backing pods

- What is a stateful set vs a deployment
  - statefulsets manage stateful apps (databases, message queues).
  - deployments manages stateless apps (web servers, APIs).


- What is the difference between a Persistent Volume (PV) and a Persistent Volume Claim (PVC)?
  - PV represents actual storage available in the cluster (disk, NFS, cloud storage).
  - PVC is a request for storage made by a pod.

- What is a StorageClass in Kubernetes?
  - A StorageClass in Kubernetes defines how storage is dynamically provisioned for Persistent Volumes (PVs). It allows admins to set up different types of storage backends (e.g., SSD, HDD, cloud storage) and lets developers request storage without worrying about the underlying infrastructure.

- What is a NodeSelector, and how does it help in Kubernetes scheduling?
  - A NodeSelector is a simple way to schedule pods onto specific nodes based on labels. It restricts a pod to run only on nodes that match a specified label.
  - NodeSelector uses labels to match pods to nodes.
  - e.g. `kubectl label nodes node-1 disktype=ssd`

- What is Node Affinity, and how does it improve scheduling over NodeSelector?
  - Node Affinity is a more advanced and flexible way to schedule pods onto specific nodes compared to NodeSelector.
  - Supports: ✔️ "Hard" rules (requiredDuringSchedulingIgnoredDuringExecution), "Soft" rules (preferredDuringSchedulingIgnoredDuringExecution)


- What is a Pod Disruption Budget (PDB), and why is it useful in Kubernetes?
  - A Pod Disruption Budget (PDB) helps limit the number of pods that can be disrupted (voluntarily evicted) at the same time due to maintenance tasks, like node upgrades or scaling events.

- What is a Kubernetes Job, and how is it different from a Deployment?
  - A Kubernetes Job runs a task to completion, while a Deployment manages long-running applications.

- What is a CronJob, and how is it different from a Job?
  - A Job runs once and completes, while a CronJob runs on a schedule.

- What is a PriorityClass

- What is difference between node port, target port and port?
	-	port: The entry point into the Service.
	-	targetPort: The actual container port in the Pod.
	-	nodePort: The external port on the Node’s IP (optional, only for external access).
  - You (External) → NodeIP:nodePort → Service (port) → Pod IP:targetPort
