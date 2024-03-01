1. helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
1. helm repo update
1. kubectl get nodes
1. helm install my-nginx ingress-nginx/ingress-nginx 
1. kubectl get ingressClass
1. kubectl delete -A ValidatingWebhookConfiguration my-nginx-ingress-nginx-admission
> nginx   k8s.io/ingress-nginx   <none>       4m43s
1. helm repo add kcert https://nabsul.github.io/helm
1. helm install kcert kcert/kcert --namespace kcert --create-namespace --set acmeEmail=webtechguru@gmail.com --set acmeDirUrl=https://acme-v02.api.letsencrypt.org/directory --set acmeTermsAccepted=true --version 1.0.6
## DNS cache clean
1. sudo systemd-resolve --flush-caches
1. sudo systemd-resolve --statistics


## To delete all the resources you've installed using Helm, you can follow these steps:
1. Get a list of releases with the following command:
```sh
helm list
```
2. Delete each release one by one using the following command:
```sh
helm delete my-nginx
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Replace <release-name> with the name of each release listed in the previous step. Repeat this step for each release until you've deleted all of them.
3. Once all releases are deleted, you can also delete the ingress-nginx Helm repository. Run:
```sh
helm repo remove ingress-nginx
```
4. These steps will help you delete all the resources installed using Helm and remove the ingress-nginx repository if desired.  
