## Google Kubernetes Engine - EKS


#### Standard Public Cluster
 - GKE Standard: The user maintains and operates nodes.
 - GKE Autopilot: GKE provisions, maintains and operates nodes.
 - Connecting to the standard-cluster `gcloud container clusters get-credentials standard-cluster-korea --region us-central1 --project polished-watch`.
 - Run `ls -lrta` to locate `.kube` and change into it to check for kubectl.
- Upload your application and then deploy `kubectl apply -f kube-manifests`.
- Lists your deployments with `kubectl get deploy`.
- Check for the list of pods `kubectl get pod`
- Check for the service `kubectl get svc`.
- Check your deployed application `curl + IP External Address` provided by the service created.
- Clean your deployments ` kubectl delete -f kube-manifests`.
- Verify kubectl version `kubectl version` and check `which kubectl` 
- Removing existing local kubectl `rm /usr/local/bin/kubectl`
- Install kubectl client `gcloud components install kubectl`.
#### Kubectl version config
- Locate the kubectl in the sdk bin folder.
- As our GKE cluster version is 1.27, we will also upgrade our kubectl to 1.27 `cp kubectl.1.27 kubectl`.
- Then config the cluster with `gcloud container clusters get-credentials standard-cluster-korea --region us-central1 --project polished`.
- View all configurations `kubectl config view`.