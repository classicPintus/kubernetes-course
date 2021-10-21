# Kubernetes examples #

## Table of contents ##
- service interno
- service esterno
- liveness
- readness
- startup probe

## Steps ##
1. `minikube tunnel` -> It allows to access inside the cluster
2. `kubectl apply -f mysql.yml`
3. `kubectl get services` -> It allows to know the ip of the load balancer. Pick the "external ip" column
4. With a db client try to access to <external-ip>:3306. If you use dbeaver you must enable the public key retrieval. Go to the selected connection -> ssl tab -> enable "allow public key retrieval"

## At the end... ##
1. `kubectl delete -f mysql.yml`
2. Close the terminal of the `minikube tunnel` command
