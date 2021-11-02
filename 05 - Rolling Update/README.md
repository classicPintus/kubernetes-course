# Kubernetes examples #

## Table of contents ##
- Rolling update

## Steps ##
1. In a separate shell run `minikube tunnel` -> It allows to access inside the cluster
2. `kubectl apply -f nginx.yml`
3. `kubectl get services` -> It allows to know the ip of the load balancer. Pick the "external ip" column
4. Run `watch curl -I <externalIp>`
5. Open a new terminal and change the deployment image using `kubectl set image deployment/nginx-deployment nginx=nginx:stable` and  `kubectl set image deployment/nginx-deployment nginx=nginx:mainline`
6. Watching the output of the `watch` command you will see the change in the nginx version but all the http statuses are always 200 (OK)

## At the end... ##
1. `kubectl delete -f nginx.yml`
2. Close the terminal of the `minikube tunnel` command
3. Close the termina with the `watch` command
