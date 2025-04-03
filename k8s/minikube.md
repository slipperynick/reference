# Minikube Command Reference

## Cluster Lifecycle Management
- **Start a Minikube Cluster**  
  `minikube start`
- **Stop the Minikube Cluster**  
  `minikube stop`
- **Delete the Minikube Cluster**  
  `minikube delete`
- **Check Minikube Status**  
  `minikube status`

## Cluster Information
- **View Cluster Information**  
  `minikube dashboard`
- **Retrieve Cluster IP**  
  `minikube ip`
- **View Cluster Logs**  
  `minikube logs`

## Configuration and Environment
- **Configure Docker Environment**  
  `minikube docker-env`
- **Configure Podman Environment**  
  `minikube podman-env`
- **Modify Minikube Configuration**  
  `minikube config set <key> <value>`

## Addons Management
- **List Available Addons**  
  `minikube addons list`
- **Enable an Addon**  
  `minikube addons enable <addon-name>`
- **Disable an Addon**  
  `minikube addons disable <addon-name>`

## Service Management
- **Access a Service**  
  `minikube service <service-name>`
- **Retrieve Service URL**  
  `minikube service <service-name> --url`

## SSH and File Management
- **SSH into Minikube VM**  
  `minikube ssh`
- **Copy Files to Minikube**  
  `minikube cp <source> <target>`

## Multi-Node and Profiles
- **Manage Minikube Profiles**  
  `minikube profile list`
- **Start a Cluster with a Specific Profile**  
  `minikube start -p <profile-name>`
- **Delete a Specific Profile**  
  `minikube delete -p <profile-name>`

## Resource Management
- **View Resource Usage (CPU/Memory) for Pods**  
  `kubectl top pod`
- **View Resource Usage for Nodes**  
  `kubectl top node`
- **Apply a Configuration File**  
  `kubectl apply -f <file.yaml>`
- **Delete Resources from a File**  
  `kubectl delete -f <file.yaml>`

## Networking and Ports
- **Check Minikube Tunnel Status**  
  `minikube tunnel`
- **Forward Ports from a Pod to Local Machine**  
  `kubectl port-forward <pod-name> <local-port>:<pod-port>`

## Persistent Volumes
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

## Debugging and Troubleshooting
- **List Events in the Cluster**  
  `kubectl get events`
- **View Logs from a Pod**  
  `kubectl logs <pod-name>`
- **Describe a Pod for Debugging**  
  `kubectl describe pod <pod-name>`
- **Restart a Deployment**  
  `kubectl rollout restart deployment/<deployment-name>`
- **Run a Debugging Pod**  
  `kubectl run -i --tty busybox --image=busybox -- sh`

## Backup and Restore
- **Backup etcd**  
  `ETCDCTL_API=3 etcdctl snapshot save /opt/etcd-backup.db --endpoints=<etcd-endpoint> --cacert=/etc/kubernetes/pki/etcd/ca.crt --cert=/etc/kubernetes/pki/etcd/server.crt --key=/etc/kubernetes/pki/etcd/server.key`
- **Restore etcd**  
  `ETCDCTL_API=3 etcdctl snapshot restore /opt/etcd-backup.db --data-dir /var/lib/etcd-from-backup`

## Access Control
- **View Service Accounts**  
  `kubectl get serviceaccounts`
- **Describe a Service Account**  
  `kubectl describe serviceaccount <serviceaccount-name>`
- **Create a Role Binding for a Service Account**  
  `kubectl create rolebinding <binding-name> --role=<role-name> --serviceaccount=<namespace>:<serviceaccount-name> --namespace=<namespace>`

## Miscellaneous Commands
- **Explain a Kubernetes Resource**  
  `kubectl explain <resource>`
- **Get API Resources**  
  `kubectl api-resources`
- **Get API Versions**  
  `kubectl api-versions`
- **Change the Current Context**  
  `kubectl config use-context <context-name>`
- **View Current Context**  
  `kubectl config current-context`
- **Delete a Context**  
  `kubectl config delete-context <context-name>`
- **View Kubeconfig File**  
  `kubectl config view`
- **Get Cluster Nodes and Their IPs**  
  `kubectl get nodes -o wide`
- **Delete Everything in the Current Namespace**  
  `kubectl delete all --all`

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
- **View Helm Chart Values**  
  `helm show values <chart-name>`

