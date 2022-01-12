# Kubernetes

 is an open source **container orchestration platform** that automates many of the manual processes involved in deploying, managing, and scaling containerized applications.

 ## Features
-   **Controlling resource consumption** by application or team
-   Evenly spreading application load across a host infrastructure with different:
	- datacenters
	- hardware
	- hosting providers
-   **Automatically load balancing** requests across the different instances of an application
-   **Monitoring resource consumption and resource limits** to automatically stop applications from consuming too many resources and restarting the applications again
-   **Moving an application instance from one host to another** if there is a shortage of resources in a host, or if the host dies
-   Automatically **leveraging additional resources** made available when a new host is added to the cluster
-   Easily performing [canary deployments](https://medium.com/google-cloud/kubernetes-canary-deployments-for-mere-mortals-13728ce032fe) and rollbacks

>**Kubernetes is cloud-agnostic**

![Kubernetes Architecture](https://newrelic.com/sites/default/files/styles/1200w/public/2021-05/kubernetes_architecture-1024x649.jpeg?itok=224Yqhs6)

## Kubernetes master 
The Kubernetes master is the **access point** (or the control plane) from which administrators and other users interact with the cluster to manage the scheduling and deployment of containers. 

A cluster will always have at least one master, but may have more depending on the cluster’s replication pattern.

## Nodes
All nodes in a Kubernetes cluster must be configured with a container runtime, which is usually [[Docker]]. 
The container runtime starts and manages the containers as Kubernetes deploys them to nodes in the cluster. 

Applications (web servers, databases, API servers, etc.) run inside the containers.