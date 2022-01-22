# kubernetes-easy-ingress-wp-mysql-deployement-letsencrypt
Easy deployment for K8s with :

# Namespace, ingress, svc, pv, pvc, pod  
Wordpress (4.8-apache) / Mysql 5.7<br />

# You have to do before using<br />

replace <b>${MAIL}</b> with your mail into letsencrypt-staging.yaml<br />
replace <b>${MAIL}</b> with your mail into letsencrypt-prod.yaml<br />
replace <b>${SITEURLEXT}</b> with your domain into ingress-route.yaml<br />
replace <b>${NAMESPACE}</b> with your namespace into namespace.yaml<br />
replace <b>${SECRETPWD}</b> with your secret password into kustomization.yaml<br />

# Usage:<br />
kubectl apply -f ./ letsencrypt-staging.yaml<br />
kubectl apply -f ./ letsencrypt-prod.yaml<br />
kubectl apply -f ./namespace.yaml<br />
kubectl apply -k ./ --namespace=${NAMESPACE} --validate=false<br />
<br />
This directory contains an example of how to run real applications with Kubernetes.<br />

