kubectl create --filename gce_ssl_deploy.yml
kubectl create --filename gce_ssl_managed_cert.yml
kubectl create --filename gce_ssl_service.yml
kubectl create --filename gce_ssl_ingress.yml

kubectl describe managedcertificates.networking.gke.io/hello-k8s-gce-ssl

gcloud compute ssl-certificates list \
 --filter "hello." \
 --format "$FORMAT"