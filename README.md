# Test Plan for Multi-cluster environment in Contrail


### 1. Analyse the product

* Multiple k8s cluster
    * Multiple k8s clusters
    * Multiple kube-managers
    * Multiple kube-master
* OpenStack controller with k8s cluster
    * Reference link: https://github.com/Juniper/contrail-ansible-deployer/wiki/Deployment-Example:-Contrail-and-Kubernetes-and-Openstack

#### Why Multiple k8s clusters?
* No idea

### 2. Scope of Testing
#### Concepts with OpenStack controller with k8s cluster
* Kube-manager to Contrail mappings check
    * Namespace to Project
    * Pod to Virtual Machine
    * Service to ECMP Loadbalancer
    * Ingress to Haproxy Loadbalancer
    * Network Policy to Contrail Security
* Analyse the test cases regarding the above in contrail-test repo
* Test cases include
    * Kube-manager restart cases
    * Docker restart cases
    * Ping between pods
    * Pod availability in contrail-api and kube-manager
    * Pod deletion and creation
    * RBAC test cases for Admin control
    * Namespace, Service, Ingress and Network policy test cases
    * OpenStack test cases
