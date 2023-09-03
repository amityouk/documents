```
https://codefresh.io/learn/kubernetes-deployment/
https://jamesdefabia.github.io/docs/user-guide/kubectl/kubectl/
https://codefresh.io/learn/kubernetes-deployment/
https://kubernetes.io/docs/reference/kubectl/cheatsheet/#kubectl-context-and-configuration
https://kubernetes.io/docs/tasks/run-application/run-stateless-application-deployment/

https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/

https://akomljen.com/kubernetes-persistent-volumes-with-deployment-and-statefulset/
https://phoenixnap.com/kb/kubernetes-mysql
https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/

kubernet installtion on centos7
https://jhooq.com/15-steps-to-install-kubernetes-on-bento-centos7/
```
```
vi /etc/fastab

1. master
These components are the API server, etcd, scheduler, controller-manager, and cloud controller manager.

The controller manager. This component is a single binary composed of four sub-processes and they are:

The node controller: Responsible for the health of the nodes in the cluster.
The replication controller: responsible for keeping the desired amount of pods for each replication.
The endpoints controller: handles the Endpoints object that links services and pods.
The service account and token controller: handles the default accounts and API access for namespaces.


2. Client nodes

kubelet, kubeproxy,container runtime

The kubelet, which makes sure all containers are running and healthy.

The proxy allows communication to the inside network of the cluster by using network rules, mainly used for development and testing pods, it is recommended to remove it in production for security reasons.

The container runtime, which is responsible for running the containers, the most common runtimes choices are: Docker and Containerd


3. Namespaces are a way to organize clusters into virtual sub-clusters — they can be helpful when different teams or projects share a Kubernetes cluster. Any number of namespaces are supported within a cluster, each logically
 separated from others but with the ability to communicate with each other.

A Kubernetes namespace provides the scope for Pods, Services, and Deployments in the cluster. Users interacting with one namespace do not see the content in another namespace

Kubernetes starts with four initial namespaces:
default The default namespace for objects with no other namespace.
kube-node-lease This namespace holds Lease objects associated with each node. ...
kube-public This namespace is created automatically and is readable by all users (including those not authenticated).
#############################################

Default: Namespace for objects without any other object.

Kube-node-lease: It holds a lease object which is associated with all nodes.

Kube-public: It is created automatically and can be readable by both authenticated and unauthenticated users.

Kube-system: It is created by the system of Kubernetes.
####################################################################


4. Types of Kubernetes Services (networking for pods)
ClusterIP. (ClusterIP (default))Exposes a service which is only accessible from within the cluster.
NodePort. Exposes a service via a static port on each node's IP.
LoadBalancer. Exposes the service via the cloud provider's load balancer.
ExternalName.
########################################################################################
Here are important aspects of the service manifest:

metadata:name—this is the logical name of the service, which will also become the DNS name of the service when it is created.
spec:selector—the selector identifies which pods that should be included in the service. In this example, pods that have the label app: nginx will become part of the service.
spec:ports—a list of port configurations (there can be one or more). Each port configuration defines a network protocol and port number. Optionally, the port configuration can define a targetPort, which is the port the pod should send traffic to.

5. A Kubernetes Deployment tells Kubernetes how to create or modify instances of the pods that hold a containerized application. Deployments can help to efficiently scale the number of replica pods, enable the rollout of updated code in a
 controlled manner, or roll back to an earlier deployment version if necessary.

6. A pod is a unit including one or more containers that share storage and networking resources. Pods are the smallest application building blocks in a Kubernetes cluster.

7. A StatefulSet is a workload API object for managing stateful applications.imilar to Deployments, StatefulSets manage the behavior of pods.
However, it differs from deployments in that it maintains a static ID for each pod. Pods are created from the same template, but each one has a separate identity, making it possible to maintain a persistent state across the full lifecycle of the pod.

Deployment	                                   StatefulSet
Intended for stateless applications	          Intended for stateful applications
Pods are interchangeable	                  Pods are unique and have a persistent ID
All replicas share the same volumes and PersistentVolumeClaims	Each pod has its own volumes and PersistentVolumeClaims

8. A ReplicaSet is a Kubernetes object that runs multiple instances of a pod and ensures a certain number of pods is running at all times. 
The goal is to ensure that the applications running in the pods have enough resources and do not experience downtime, even if one or more pods fail. 
```
```
9. Kubernetes Deployment Status and Lifecycle
A Kubernetes Deployment object has the following lifecycle stages:

Progressing—this means the Deployment is currently making changes to the cluster to meet the desired state in the declarative configuration.
Completed—this means the deployment has finished matching cluster state to the desired state. All required pods are available and running the latest pods specification, and old pods are no longer running.
Failed—this means that the deployment encountered a problem while trying to reconcile cluster state with desired state. For example, there may have been insufficient resources or errors when running pods. 
To understand the cause of a failed deployment, use the command kubectl rollout status.
```
```
10. Kubernetes offers the following two deployment strategies out of the box:
10A.Recreate Deployment

The recreate strategy kills the currently running pod instances and creates new instances running the latest version. This is often used in development environments where users are not actively working on the instances and downtime is acceptable. 

10B. Rolling Update Deployment
Rolling Update Deployment
A rolling update deployment strategy allows for a sequential, gradual transition from one application version to another. In this deployment, a new version of a ReplicaSet is started alongside the existing ReplicaSet with the old version. The Deployment object launches new pods using the new version of the pod specification, and when the new pods start successfully, shuts down the old pods.  
Rolling updates allow you to migrate between versions in a safe and controlled manner, but the transition to the new version can take time. Also,
 it can be difficult to roll back or interrupt the deployment in the middle if something goes wrong.

11. Blue/Green Deployment (Also Known as Red/Black Deployment)
The downside of a blue/green deployment is that it requires twice the resource utilization, at least during the staging and cut-off period.

12.Canary Deployment
Canary deployments are great for testing new features with small groups of users and can be rolled back easily. Therefore, canary deployment is a good way to determine how new code will affect the system as a whole and whether it will have a positive or negative impact on user experience. 
you also need a service mesh or network gateway to split traffic between current and canary versions.

13.A/B Testing

14. Shadow Deployment

15. Progressive Deployment in Kubernetes with Argo Rollouts
Blue/Green Deployment with Argo Rollouts
Canary Deployment with Argo Rollouts
```
```
Let’s update the Nginx Pods to use the nginx:1.16.1 image instead of the nginx:1.14.2 image.
kubectl --record deployment.apps/nginx-deployment set image deployment.v1.apps/nginx-deployment nginx=nginx:1.16.1

##############################################################
kubectl cluster-info  # kubernet cluster info

To create deployment
## kubectl create deployment nginx-depl --image=nginx:1.19

create deployment with custom namespace
#kubectl create deployment my-app --image=redis --replicas=2 --namespace dev

To update the Deployment, e.g. update the Nginx image version to 1.21, execute:
## kubectl set image deployment/nginx-depl nginx=nginx:1.21

To scale the Deployment, e.g. create one more replica Pod:
## kubectl scale --replicas=2 deployment/nginx-depl

To Create a Service to expose the Deployment outside the cluster:
## kubectl create service nodeport nginx-depl --tcp=80:80

Delete the Deployment (also deletes the Pods) and the Service:
## kubectl delete deployment nginx-depl
## kubectl delete service nginx-depl

to take ssh ### kubectl exec -it nginx-depl-6cddfb994d-mmkcb /bin/bash
#########################################
kubectl describe deployment nginx-deployment ## given more information related namespace 
kubectl get all --all-namespaces
kubectl get pods --show-labels
kubectl get deployment -o wide

kubectl create deployment india
kubectl describe deployment india
kubectl delete deployment my-deployment  ###to delete your deployment

kubectl get services (svc)
kubectl create services india
kubectl describe services india
kubectl delete services services delete your deployment

kubectl get rs
kubectl get pods
kubectl describe pods india

kubectl get nodes
kubectl cordon - Mark node as unschedulable

################################investigation######################

kubectl edit svc nginx-depl -n <namespace> # kubectl edit svc nginx-depl -n default
kubectl patch svc nginx-depl -p '{"spec": {"type": "LoadBalancer"}}'
kubectl patch svc nginx-depl -p '{"spec": {"type": "NodePort"}}'

kubectl config set-context --current --namespace=india


kubectl rollout undo deploy my-deployment-name -n my-namespace
kubectl get namespaces --show-labels
kubectl config view  # more detials like namespace

kubectl config set-context dev --namespace=development \
  --cluster=lithe-cocoa-92103_kubernetes \
  --user=lithe-cocoa-92103_kubernetes

# kubectl run nginx --image=nginx --namespace=default
To create a pod using the nginx image, run the command kubectl run nginx --image=nginx --restart=Never. 
This will create a pod named nginx, running with the nginx image on Docker Hub. And by setting the flag --restart=Never
 we tell Kubernetes to create a single pod rather than a Deployment.



#####################
the kubectl apply command can be used to update an already existing deployment, kubectl create but cannot. kubectl create can only be used when the resource does not already exist

kubectl delete -f deployment.yaml  # to delete your deployment

kubectl create -f deployment.yaml


###https://matthewpalmer.net/kubernetes-app-developer/articles/kubernetes-apiversion-definition-guide.html

# 1 metadata 
#2 specification
# 3 status # which aupdate kuberneties automatically and update # desired = autual states

kubectl get deployment nginx-deployment -o yaml > deployment-result.yaml


======================Deployment===========================
apiVersion: apps/v1
kind: Deployment
metadata:                                   ## labels # app: nginx       
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 3
  selector:                         ## selector # matchLabels: app: nginx
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80


##############service file######################

apiVersion: v1
kind: Service
metadata:
  name: nginx-service
spec:
  selector:
    app.kubernetes.io/name: nginx   ## it is taking from deploymennts files
  ports:
    - protocol: TCP
      port: 80
      targetPort: 9376

######################ReplicaSet#############################

apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: frontend
  labels:
    app: guestbook
    tier: frontend
spec:
  # modify replicas according to your case
  replicas: 3
  selector:
    matchLabels:
      tier: frontend
  template:
    metadata:
      labels:
        tier: frontend
    spec:
      containers:
      - name: php-redis
        image: gcr.io/google_samples/gb-frontend:v3

##########################StatefulSets######################
apiVersion: v1
kind: Service
metadata:
  name: nginx
  labels:
    app: nginx
spec:
  ports:
  - port: 80
    name: web
  clusterIP: None
  selector:
    app: nginx
---
apiVersion: apps/v1
kind: StatefulSet
metadata:
  name: web
spec:
  selector:
    matchLabels:
      app: nginx # has to match .spec.template.metadata.labels
  serviceName: "nginx"
  replicas: 3 # by default is 1
  minReadySeconds: 10 # by default is 0
  template:
    metadata:
      labels:
        app: nginx # has to match .spec.selector.matchLabels
    spec:
      terminationGracePeriodSeconds: 10
      containers:
      - name: nginx
        image: registry.k8s.io/nginx-slim:0.8
        ports:
        - containerPort: 80
          name: web
        volumeMounts:
        - name: www
          mountPath: /usr/share/nginx/html
  volumeClaimTemplates:
  - metadata:
      name: www
    spec:
      accessModes: [ "ReadWriteOnce" ]
      storageClassName: "my-storage-class"
      resources:
        requests:
          storage: 1Gi

##############################DaemonSet
apiVersion: apps/v1
kind: DaemonSet
metadata:
  name: fluentd-elasticsearch
  namespace: kube-system
  labels:
    k8s-app: fluentd-logging
spec:
  selector:
    matchLabels:
      name: fluentd-elasticsearch
  template:
    metadata:
      labels:
        name: fluentd-elasticsearch
    spec:
      tolerations:
      # these tolerations are to have the daemonset runnable on control plane nodes
      # remove them if your control plane nodes should not run pods
      - key: node-role.kubernetes.io/control-plane
        operator: Exists
        effect: NoSchedule
      - key: node-role.kubernetes.io/master
        operator: Exists
        effect: NoSchedule
      containers:
      - name: fluentd-elasticsearch
        image: quay.io/fluentd_elasticsearch/fluentd:v2.5.2
        resources:
          limits:
            memory: 200Mi
          requests:
            cpu: 100m
            memory: 200Mi
        volumeMounts:
        - name: varlog
          mountPath: /var/log
      terminationGracePeriodSeconds: 30
      volumes:
      - name: varlog
        hostPath:
          path: /var/log

############################################################




apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: web
spec:
  selector:
    matchLabels:
      app: web
  replicas: 5
  strategy:
    type: RollingUpdate

  template:
    metadata:
      labels:
        app: web
    spec:
      containers:
       —name: nginx
          image: nginx
          resources:
            limits:
              memory: 200Mi
            requests:
              cpu: 100m
              memory: 200Mi
          ports:
           —containerPort: 80



```


@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@


https://phoenixnap.com/kb/docker-volumes

https://blog.devops.dev/creating-a-docker-bridge-network-a085ff8559c3

https://www.tecmint.com/install-lamp-server-linux/   ## setup lamp server ## pysical server

https://github.com/arocki7/ansible-centos7-lamp    ansible role playbbok. ## pysical server

Laptop ----centos (os) ----install lamp server.

laptop ---centos (os) ---ansible setup --- install lamp--playbook/ role...


laptop ---centos(OS) ----Docker-----docker-hub(take images) --- install lamp --- ## https://hub.docker.com/r/mattrayner/lamp

https://www.linuxhelp.com/how-to-build-a-lamp-stack-docker-container-on-ubuntu-21-04
https://stackoverflow.com/questions/44497351/dockerfile-with-lamp-running-ubuntu

https://www.kubermatic.com/blog/keeping-the-state-of-apps-1-introduction-to-volume-and-volumemounts/
Docker and Kubernetes are two different technologies with different use cases. You use Docker Desktop to run, edit and manager container development. You use Kubernetes to run production grade applications at scale.

 https://www.dynatrace.com/news/blog/kubernetes-vs-docker/
https://www.bmc.com/blogs/kubernetes-deployment/

https://linuxhint.com/lamp_server_docker/

Cloud-Native: Microservices, Kubernetes, Service Mesh, CI/CD




















