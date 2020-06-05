# dctmkubernetes

Below are steps for setting of Documentum Development on Google Kubernetes Engine.

1. Create a GKE Cluster on the GCP

2. Setup the GCLoud SDK on your Desktop.

   https://cloud.google.com/sdk/docs/downloads-versioned-archives

3. Configure Kubectl and GKE CLuster.
     
https://kubernetes.io/docs/tasks/tools/install-kubectl/

4. Dowload the Docuemntum 20.2 Content Server & DA docker Images and push it to the GCR 


https://cloud.google.com/container-registry/docs/pushing-and-pulling

5. Check out the files to your machine.

6. Execute the below command for setting up of Postgres database

  Kubectl apply -f postgres.yaml
  
7. After successful creation of Postgres POD , execute the below commands

   
Kubectl exec postgresserver-0 —  mkdir /var/lib/postgresql/data/db_dctmrepo_dat.dat

Kubectl exec postgresserver-0 —  chown postgres /var/lib/postgresql/data/db_dctmrepo_dat.dat


8. Execute the below command for Install & Setup up of Docbroker
 
   Kubectl apply -f docbroker.yaml

9. Execute the below command for Install & Setup up of Docbase

   Kubectl apply -f docbase.yaml

10. Execute the below command for Install & Setup up of Docbroker

   Kubectl apply -f daclient.yaml
