# Kubernetes examples #

## Indice ##
- Secrets

## Comandi da lanciare ##
`kubectl apply -f secrets.yml`
`kubectl apply -f mysql.yml`

## How to create a secret value ##
* `echo -n '<yourSecretValue>' | base64`
* Add it to the secret configuration file

## Alla fine... ##
`kubectl delete -f secrets.yml`
`kubectl delete -f mysql.yml`
