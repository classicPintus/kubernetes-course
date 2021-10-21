# Kubernetes examples #

## Indice ##
- config map

## Comandi da lanciare ##
`kubectl apply -f config-map.yml`
`kubectl apply -f mysql.yml`

## How to create a secret value ##
* `echo -n '<yourSecretValue>' | base64`
* Add it to the secret configuration file

## Alla fine... ##
`kubectl delete -f config-map.yml`
`kubectl delete -f mysql.yml`
