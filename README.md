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

## Chapter 4: The Operator Framework
- (33) The Red Hat Operator Framework \[...\] makes building Operators easier with a software development kit that automates much of the repetitive implementation work.
    - [Operator SDK](https://oreil.ly/IcfRf)
- (33) Operator Lifecycle Manager (OLM) is an Operator that installs, manages, and upgrades other Operators
    - [Operator Lifecycle Manager](https://oreil.ly/SDL7q) 
    - ^^ broken link on page 36
- (33) The Operator SKD builds atop the Kubernetes [controller-runtime](https://oreil.ly/AM0TP)
- (35)The subsequent examples in this book use version series 0.11.x of operator-sdk
    - most recent version is 1.25.2, this book may be more dated than I thought
- (36) OLM defines a schema for Operator metadata, called the Cluster Service Version (CSV), for describing an Operator and its dependencies

## Chapter 5: Sample Application: Visitors Site
- (40) The Visitors Site is a traditional, three-tier application consisting of:
    - A web frontend, implemented in React
    - A REST API, implemented in Python using the Django framework
    - A database, using MySQL
- [app-manifests](https://github.com/kubernetes-operators-book/chapters/tree/master/ch05)
    - use mcmull27 images for app arm64 builds
    - mysql adds arm builds in version 8
    - ui loads fine, fails to fetch backend api
        - [python error message](./error.txt)
