[![Build Status](https://kubernetes.io/images/nav_logo2.svg?branch=master)](https://kubernetes.io)

# Deployment Appwork at Kubernetes
[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Este é um projeto para a criação da aplicação appwork rodando em Kubernetes:

 Criando Volumes, Deployment e Services do banco de dados Mongodb:
  - kubectl create -f mongo-pv.yml
  - kubectl create -f mongo-pvc.yml
  - kubectl create -f mongo-deploy.yml
  - kubectl create -f mongo-service.yml
 
  Criando Deployment e Services da aplicação
  - kubectl create -f appwork_web_deploy.yml
  - kubectl create -f appwork_web-service.yml
  
  Criando Ingress Nginx
Entre no diretório do ingress e crie os deployments, services, roles e configmap, utilizando o kubectl, usando o namespace ingress:

  - kubectl create -f defaut-backend.yml -n ingress
  - kubectl create -f defaut-backend-service.yml -n ingress
  - kubectl create -f nginx-ingress-controller-config-map.yml
  - kubectl create -f nginx-ingress-controller-roles.yaml
  - kubectl create -f nginx-ingress-controller-deployment.yml
  - kubectl create -f nginx-ingress-controller-service.yml

Edite o arquivo appserver para alterar o endereço do host, após alterar crie o ingress
  - kubectl create -f appserver.yml
