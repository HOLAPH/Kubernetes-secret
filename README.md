# Assignment 

## Create secrets within your minikube:
1. try creating using imperative command using --from-literal option
2. try creating declaratively

## Inject secrets into your nginx pod using all the below ways:
1. As an ENV ( All secrets as an env variable )
2. As a Single ENV
3. As Volume

---

# Answer

__Step1.__

 * kubectl create secret generic imperative-secret  \
 --from-literal=username=admin \
 --from-literal=password='changeme'
 
__Step2.__

kubectl apply -f Secret-declaratively.yml

*NOTE: You can only put base64 value in yml file for username and password.*
