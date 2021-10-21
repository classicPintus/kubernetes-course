# Kubernetes examples #

## Prerequisites ##

* [Kubernetes](https://kubernetes.io/)
* [Minikube](https://minikube.sigs.k8s.io/docs/start/)

## Nomenclatura ##
* **pod** -> "Point Od Delivery". E' l'unica atomica di elaborazione di kubernetes. Può contenere uno o più container e risorse (tipo volumi)
* **service** -> Permettono di far/poter dialogare i pod con l'esterno o con altri nodi

## Tipi di service
A Service in Kubernetes is an abstraction which defines a logical set of Pods and a policy by which to access them

* **ClusterIp** -> Exposes the Service on an internal IP in the cluster. This type makes the Service only reachable from within the cluster
* **NodePort** -> Exposes the Service on the same port of each selected Node in the cluster using NAT. Makes a Service accessible from outside the cluster using <NodeIP>:<NodePort>. Superset of ClusterIP.
* **LoadBalancer** -> Creates an external load balancer in the current cloud (if supported) and assigns a fixed, external IP to the Service
* **ExternalName** -> Maps the Service to the contents of the externalName field (e.g. foo.bar.example.com), by returning a CNAME record with its value

## Comandi ##
* `minikube start` -> it allows to start minikube
* `kubectl cluster-info` -> Cluster's info
* `kubectl get nodes` -> Get all the nodes of the cluster
* `kubectl get pods`  -> Get all the pods of the cluster
* `kubectl describe pods`  -> Get details of the pods
* `kubectl proxy` -> ?
* `kubectl exec <podName> -- env` -> Execute "env" command on the selected pod 
* `kubectl exec -it <podName> -- bash` -> Esegue il comando `bash` sul pod indicato
* `kubectl wait --for=condition=ready pod -l app=inventory` -> aspettare la readiness del pod inventory
* `kubectl create configmap sys-app-name --from-literal name=my-system` -> creare un configMap. Una mappa chiave/valore in chiaro
* `kubectl create secret generic sys-app-credentials --from-literal username=bob --from-literal password=bobpwd` -> Mappa chiave/valore cifrata (con cosa?)
* `kubectl replace --force -f kubernetes.yaml` -> DOVREBBE rimpiazzare 
* `kubectl get --watch pods` -> Boh
* `kubectl get deployment mysql -o yaml` -> Allows to get the yaml of the selected kind 
