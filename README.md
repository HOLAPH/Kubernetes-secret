# Assignment 

## Create secrets within your minikube:
1. try creating using imperative command using --from-literal option
2. try creating declaratively

## Inject secrets into your nginx pod using all the below ways:
3. As an ENV ( All secrets as an env variable )
4. As a Single ENV
5. As Volume

---

# Answer:

![](https://media.giphy.com/media/3NtY188QaxDdC/giphy.gif)

__Step1.__

    kubectl create secret generic imperative-secret  \
    --from-literal=username=admin \ 
    --from-literal=password='changeme'
 
__Step2.__

    kubectl apply -f Secret-declaratively.yml

[Secret-declaratively.yml](https://github.com/HOLAPH/Kubernetes-secret/blob/main/Secret-declaratively.yml)

*NOTE: You can only put base64 value in yml file for username and password.*



__Step3.__

    kubectl apply -f secret-for-all-env-pod.yml
[secret-for-all-env-pod.yml](https://github.com/HOLAPH/Kubernetes-secret/blob/main/secret-for-all-env-pod.yml)

__Setp4.__

    kubectl apply -f secret-for-one-env-pod.yml
[secret-for-one-env-pod.yml](https://github.com/HOLAPH/Kubernetes-secret/blob/main/secret-for-one-env-pod.yml)

__Setp5.__

    kubectl apply -f secret-as-volume-for-pod.yml
[secret-as-volume-for-pod.yml](https://github.com/HOLAPH/Kubernetes-secret/blob/main/secret-as-volume-for-pod.yml)    