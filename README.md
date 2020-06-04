# dctmkubernetes



https://cloud.google.com/sdk/docs/downloads-versioned-archives

https://cloud.google.com/container-registry/docs/pushing-and-pulling

https://kubernetes.io/docs/tasks/tools/install-kubectl/

Kubectl apply -f postgres.yaml

Kubectl exec postgresserver-0 —  mkdir /var/lib/postgresql/data/db_dctmrepo_dat.dat

Kubectl exec postgresserver-0 —  chown postgres /var/lib/postgresql/data/db_dctmrepo_dat.dat
 
Kubectl apply -f docbroker.yaml

Kubectl apply -f docbase.yaml

Kubectl apply -f daclient.yaml
