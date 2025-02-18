kubectl apply -f client-pod.yaml

kubectl describe pod client-pod

kubectl get deployments
            services
            pods
            storageclass
            pv
            pvc


kubectl delete -f <config file>


Deployment is a kubernets object that is meant to maintain a set of identical pods


Kada promenimo source-code, izbildamo image-e i okacimo ih na DockerHub, moramo kubernetesu reci da osvezi
podove sa najnovijim image-ima na sledeci (imperativni) nacin:

kubectl set [image] <object_type> / <object_name> <container_name> = <new_image_to_use>

kubectl describe storageclass

SECRET pravimo i lokalno i na produkcionom okruzenju:

kubectl crete secrete generic pgpassword --from-literal PGPASSWORD=12345asdf
generic - opcija
pgpassword - namespace za nase key-value parove
key - PGPASSWORD
value - 12345asdf


------
Kubeernetes Services:
    - ClusterIP
    - NodePort
    - Load Balancer - los jer se vezuje za jedan Deployment 
    - Ingress