# Kubernetes Operators
Reading notes on _Kubernetes Operators_ by Jason Dobies adn Joshua Wood (O'Reilly). Copyright 2020 Red Hat, Inc., 978-1-492-04804-6
- accompanying [git repo](https://github.com/kubernetes-operators-book/chapters.git)

## Chapter 1: Operators Teach Kubernetes New Tricks
- (1) An Operator builds on Kubernetes abstractions to automate the entire lifecycle of the software it manages \[, and\] provide application specific automation
- (6) CRDS extend the API of the particular cluster where they are defined


## Chapter 2: Running Operators 
- Book examples have been tested on kube versions 1.11 up to 1.16
- Minikube is recommended for testing book examples
- Examples can also be run on [OpenShift learning portal](https://learn.openshift.com)
    - [etcd operator lab](https://oreil.ly/j-xKh)

## Chapter 3: Operators at the Kubernetes Interface
- native kubernetes resources are also managed by a controller the same way an operator is
- (28) An Operator is the application-specific combination of CRs and a custom controller \[...\] the Operator's _operand_ is what we call the application, service, or whatever resources an Operator manages
