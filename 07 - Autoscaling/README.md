# Kubernetes examples #

## Table of contents ##
- Autoscaling

## Steps ##
1. In a separate shell run `minikube tunnel` -> It allows to access inside the cluster
2. In a separate shell run `minikube dashboard`
3. `kubectl apply -f nginx.yml`
4. `kubectl get services` -> It allows to know the ip of the load balancer. Pick the "external ip" column
5. Run something that call many times http://<external ip>
6. Through the dashboard you will see that after some time the pod is replicated up to 5 instances

## At the end... ##
1. `kubectl delete -f nginx.yml`
2. Close the terminal of the `minikube tunnel` command
3. Close the terminal with the `minikube dashboard` command
