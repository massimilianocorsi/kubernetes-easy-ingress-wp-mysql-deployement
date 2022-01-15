# kubernetes-easy-ingress-wp-mysql-deployement-letsencrypt
Easy deployment for K8s with :

# Namespace, ingress, svc, pv, pvc, pod  
Wordpress (4.8-apache) / Mysql 5.7<br />

# You have to do before using<br />

replace <b>[your_email@your_domain.ext]</b> with your mail into letsencrypt-staging.yaml<br />
replace <b>[your_email@your_domain.ext]</b> with your mail into letsencrypt-prod.yaml<br />
replace <b>[site_name_ext]</b> with your domain into ingress-route.yaml<br />
replace <b>[name_space]</b> with your namespace into namespace.yaml<br />
replace <b>[your_secret_password]</b> with your secret password into kustomization.yaml<br />

# Usage:<br />
kubectl apply -f ./ letsencrypt-staging.yaml
kubectl apply -f ./ letsencrypt-prod.yaml
kubectl apply -f ./namespace.yaml<br />
kubectl apply -k ./ --namespace=[name_space] --validate=false

This directory contains an example of how to run real applications with Kubernetes.<br />

