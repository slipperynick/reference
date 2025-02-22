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

