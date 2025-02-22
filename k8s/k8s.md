# Kubernetes Command Reference

## Cluster Management
- **View Cluster Information**  
  `kubectl cluster-info`
- **List Nodes**  
  `kubectl get nodes`
- **Describe a Node**  
  `kubectl describe node <node-name>`

## Namespace Management
- **List All Namespaces**  
  `kubectl get namespaces`
- **Create a New Namespace**  
  `kubectl create namespace <namespace-name>`
- **Delete a Namespace**  
  `kubectl delete namespace <namespace-name>`

## Pod Management
- **List Pods**  
  `kubectl get pods`
- **List Pods in All Namespaces**  
  `kubectl get pods --all-namespaces`
- **Describe a Pod**  
  `kubectl describe pod <pod-name>`
- **Create a Pod from a YAML File**  
  `kubectl apply -f <file.yaml>`
- **Delete a Pod**  
  `kubectl delete pod <pod-name>`
- **Execute a Command in a Pod**  
  `kubectl exec -it <pod-name> -- <command>`
- **View Pod Logs**  
  `kubectl logs <pod-name>`

## Deployment Management
- **List Deployments**  
  `kubectl get deployments`
- **Describe a Deployment**  
  `kubectl describe deployment <deployment-name>`
- **Create a Deployment**  
  `kubectl create deployment <deployment-name> --image=<image-name>`
- **Update a Deployment**  
  `kubectl set image deployment/<deployment-name> <container-name>=<new-image>`
- **Scale a Deployment**  
  `kubectl scale deployment/<deployment-name> --replicas=<number>`
- **Delete a Deployment**  
  `kubectl delete deployment <deployment-name>`

## Service Management
- **List Services**  
  `kubectl get services`
- **Describe a Service**  
  `kubectl describe service <service-name>`
- **Expose a Deployment as a Service**  
  `kubectl expose deployment <deployment-name> --type=<service-type> --port=<port>`
- **Delete a Service**  
  `kubectl delete service <service-name>`

## ConfigMap and Secret Management
- **Create a ConfigMap from a File**  
  `kubectl create configmap <configmap-name> --from-file=<file-path>`
- **Create a Secret from Literal Values**  
  `kubectl create secret generic <secret-name> --from-literal=<key>=<value>`
- **View Secrets**  
  `kubectl get secrets`
- **Describe a Secret**  
  `kubectl describe secret <secret-name>`

## Resource Management
- **Apply a Configuration File**  
  `kubectl apply -f <file.yaml>`
- **Delete Resources from a File**  
  `kubectl delete -f <file.yaml>`
- **View Resource Usage (CPU/Memory)**  
  `kubectl top pod`  
  `kubectl top node`

## Access Control
- **View Service Accounts**  
  `kubectl get serviceaccounts`
- **Describe a Service Account**  
  `kubectl describe serviceaccount <serviceaccount-name>`
- **Create a Role Binding**  
  `kubectl create rolebinding <binding-name> --role=<role-name> --serviceaccount=<namespace>:<serviceaccount-name> --namespace=<namespace>`

## Miscellaneous Commands
- **Explain a Resource**  
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

## Ingress Management
- **List Ingresses**  
  `kubectl get ingress`
- **Describe an Ingress**  
  `kubectl describe ingress <ingress-name>`
- **Apply an Ingress Rule**  
  `kubectl apply -f ingress.yaml`
- **Delete an Ingress**  
  `kubectl delete ingress <ingress-name>`

## Persistent Volumes and Claims
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

## Horizontal Pod Autoscaler
- **Autoscale a Deployment**  
  `kubectl autoscale deployment <deployment-name> --cpu-percent=<percent> --min=<min-replicas> --max=<max-replicas>`
- **View Horizontal Pod Autoscaler**  
  `kubectl get hpa`

## Backup and Restore
- **Backup etcd**  
  `ETCDCTL_API=3 etcdctl snapshot save /opt/etcd-backup.db --endpoints=<etcd-endpoint> --cacert=/etc/kubernetes/pki/etcd/ca.crt --cert=/etc/kubernetes/pki/etcd/server.crt --key=/etc/kubernetes/pki/etcd/server.key`
- **Restore etcd**  
  `ETCDCTL_API=3 etcdctl snapshot restore /opt/etcd-backup.db --data-dir /var/lib/etcd-from-backup`

## Debugging and Troubleshooting
- **List Events**  
  `kubectl get events`
- **View Logs from a Container**  
  `kubectl logs <pod-name> -c <container-name>`
- **Check Pod Status**  
  `kubectl get pod <pod-name> -o wide`
- **Restart a Pod**  
  `kubectl rollout restart deployment/<deployment-name>`
- **Run a Debugging Pod**  
  `kubectl run -i --tty busybox --image=busybox -- sh`

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
