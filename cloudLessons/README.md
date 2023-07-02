## Google Cloud Engineer

#### Kubernetes
- Download and install the gcloud cli/sdk in the home directory.
- gcloud login auth.
- kubectl authentication update `gcloud components install gke-gcloud-auth-plugin`.
- gcloud container clusters get-credentials cluster-1 --zone us-central1-c --project NAME.
-  Deploy a service: `kubectl create deployment hello-world-rest-api --image=in28min/hello-world-rest-api:0.0.1.RELEASE`.
- Check your deployment `kubectl get deployment`.
- Create a service by exposing your deployment `kubectl expose deployment hello-world-rest-api --type=LoadBalancer --port=8080`.
- Check for the service created `kubectl get services`.
- Send a get request to that url: `curl IP Address:PORT`
- Check the project in the browser:`35.193.106.160:8080/hello-world`.
- Check the events within your deployment `kubectl get events`.
- Multiple instance for the deployment: `kubectl scale deployment hello-world-rest-api --replicas=3`.
- Increasing and decreasing cluster node pool: `gcloud container clusters resize cluster-1 --node-pool default-pool --num-nodes=2 --zone=us-central1-c`.
- HPA Autoscaling based on cpu usage:`kubectl autoscale deployment hello-world-rest-api --max=4 --cpu-percent=70`.
- Horizontalpodautoscaler: `kubectl get hpa`.
- Autoscaling a cluster: `gcloud container clusters update cluster-name --enable-autoscaling --min-nodes=1 --max-nodes=10`.
- Delete service: `kubectl delete service`
- Delete deployment: `kubectl delete deployment`
- Delete cluster: `gcloud container clusters delete`.
