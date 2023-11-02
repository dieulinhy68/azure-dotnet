Absolute:
- POD, Deployments, service

Components: 
- API server
etcd
Scheduler
kubelet
Container runtime 
Controller


controlller manager:


Openshift cli (oc)
Red Hat OpenShift Container Platform
https://docs.openshift.com/container-platform/4.12/getting_started/kubernetes-overview.html

Docker pull specific image
docker compose up -d (with the image)
if successed -> add tag for the image with "stable"
    docker rmi dangling=true /// don't change image ID
else revert to previous image
    dockercompose down
    docker compose up -d image_tag=stable
healcheck: docker-compose.yml
    test: ["CMD", "curl", "-f", "http://localhost:8080/health"]
    interval: 30s
    timeout: 10s
    retries: 3

for i in {996..999}; do history -d $i; done