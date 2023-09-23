                                            Cloud computing
```
```
Cloud computing is the on-demand availability of computer system resources, especially data storage and computing power, without direct active management by the user. Large clouds often have functions distributed over multiple locations, each of which is a data cente.

There are four main types of cloud computing: private clouds (data center/on permisse/Local data center)), public clouds (AWS/gcp/azure), hybrid clouds (private+public), and multiclouds(private+public(aws+gcp)

Type of pulic cloud
IaaS vs. PaaS vs. SaaS

IaaS, or infrastructure as a service, is on-demand access to cloud-hosted physical and virtual servers, storage and networking - the backend IT infrastructure for running applications and workloads in the cloud.

PaaS, or platform as a service, is on-demand access to a complete, ready-to-use, cloud-hosted platform for developing, running, maintaining and managing applications.

SaaS, or software as a service, is on-demand access to ready-to-use, cloud-hosted application software.
```
```
```
https://www.simplilearn.com/tutorials/devops-tutorial/devops-tools#devops_monitoring_tools

1. Version Control Tool: Git (GitLab, GitHub, Bitbucket)
2. Build Tool: Maven or ant or Gradle
3. Continuous Integration Tool: Jenkins or Gitlab CI/CD
4.Configuration Management Tool: Ansible or puppet
5. Communication and Collaboration: Slack or Ms teams
6.Testing Tool: Selenium
7. Terraform  or  Pulumi
8. mysql or mariadb
9. grafana and promothiues
10. sonarqube
11. nexus
12. Linux or window os
13. cloud aws/azure/googlecloud
14. python
15. tomcat ,httpd, nginx
```
```
A. Container Platforms: Docker or podman or Linux Daemon (LXD)
B. Docker compose
C. Container Platforms: Kubernetes or docker swarm

```
```
Benefits of Linux
Free and Open Source OS.
Secure and Reliable.
Easy to Install, System Updation.
Lightweight.
Flexible.
Various Linux Distributions.
Large Community Support.
```
```

Waterfall is best used on software development projects that are well defined, predictable and unlikely to significantly change.
This usually applies to simpler, small-scale projects.Its sequential nature makes it largely unresponsive to adjustments, so budget
and delivery timelines will be affected when business requirements change during the development cycle.It is tradtional method.

```
```
Agile methods are based on iterative, incremental development that rapidly delivers a viable business product. Incremental development breaks the product into smaller
 pieces, building some of it, assessing and adapting.

```
```
• What is DevOps

DevOps is a combination of software development (dev) and operations (ops). (dev+OPS)
DevOps is a software development approach emphasizing collaboration, automation, and continuous delivery to
provide high-quality products to customers quickly and efficiently.

Benefits of DevOps
Faster, better product delivery.
Faster issue resolution and reduced complexity.
Greater scalability and availability.
More stable operating environments.
Better resource utilization.
Greater automation.
Greater visibility into system outcomes.
Greater innovation.

DevOps Stages
DevOps follows positive techniques that consist of code, building, testing, releasing, deploying, operating,
displaying, and planning. DevOps lifecycle follows a range of phases such as non-stop development, 
non-stop integration, non-stop testing, non-stop monitoring, and non-stop feedback.

DevOps Lifecycle
What are the 7 C's of DevOps?
DevOps lifecycle phases: the 7Cs of DevOps lifecycle
Continuous development.
Continuous integration.
Continuous testing.
Continuous deployment.
Continuous feedback.
Continuous monitoring.
Continuous operations.
```
```
#########################################################################

Differences Between Git and GitHub ( Bigbuket, Gitlab)


Git is  distributed version control system facilitates the management and tracking of source code histories.

Types of Version Control System :
There are two types of version control: centralized(SVN) and distributed.

Features of Git
 Tracks history.
 Free and open source.
 Supports non-linear development.
 Creates backups.
 Scalable.
 Supports collaboration.
 Branching is easier.
 Distributed development.

####################Github########################################
Git repositories are managed through GitHub's cloud-based service.
GitHub is a code hosting platform for version control and collaboration.

yum install git
git --version

There are 3 stages of a file
•	untracked - files have not been added to the Git repository
•	staged - files that have been added to Git repository or existing files that have had changes
•	committed - we commit the changes to the Git repository

There are four areas of git
•	working directory - untracked files
•	staging area - files/directories that have been added to Git using the add command (also known as index area)
•	local repository - files/directories that have been committed to Git using the commit command
•	remote repository - files/directories that have been pushed to a remote repository like GitHub

Basic Git Commands — Refresh your mind once again
git init: creating a new repository.
git clone: to copy or check out the working repository.
git add: It adds file changes in an existing directory to index.
git commit –m [type in a message] — It is used to snapshot or record a file.
git push: sending the changes to the master branch.
git pull: fetch the code already in the repository.
git diff [first branch] [second branch] — it is used to display the differences present between the two branches.
git rest [commit] — It is used to undo all the changes that have been incorporated as a part of a commit after a specified commit has taken place.
git reset –hard [commit] — This command is used to discard all the history and takes us to the last specified commit.
git log –follow [file] — his is similar to that of git log with the additional difference that it lists the version history for a particular file.
git show [commit] — This is used to display the metadata and all the content related changes of a particular commit.
git tag [commitID] — This is used to give particular tags to the code commits.
git branch [branch-name] — This is used to create a new branch.
git branch –d [branch name] — It is used to delete the current branch name specified.
git checkout [branch-name] — It is helpful in switching from one branch to another.
git status: To know the comparison between the working directories and index.


Q1 Can you tell the difference between git pull and git fetch?
Git pull command pulls new changes or commits from a particular branch from your central repository and updates your target branch in your local repository. (Git pull = git fetch + git merge)

Git fetch is also used for the same purpose but it works in a slightly different way. When you perform a git fetch,
 it pulls all new commits from the desired branch and stores it in a new branch in your local repository. If you want
 to reflect these changes in your target branch, git fetch must be followed with a git merge.


Q2 What is origin in Git?
Origin refers to the remote repository that a project was originally cloned from and is used instead of the original repository’s URL.

Q 3. What is the difference between resetting and reverting?
git reset changes the state of the branch to a previous one by removing all of the states after the desired commit,

git revert does it through the creation of new reverting commits and keeping the original one intact.

Q4. What is the purpose of branching and its types?
It allows the user to switch between the branches to keep the current work in sync without disturbing master branches and other developer’s work as per their requirements.

Q5. Explain about “git cherry-pick”?
This command enables you to pick up commits from a branch within a repository and apply it to another branch. This command is useful to undo changes when any commit is accidentally made to the wrong branch. Then, you can switch to the correct branch and use this command to git cherry-pick the commit.

Q6. How to revert a commit that has already been pushed and made public?
There are two processes through which you can revert a commit:
1. Remove or fix the bad file in a new commit and push it to the remote repository. Then commit it to the remote repository using:
git commit –m “commit message”
2. Create a new commit to undo all the changes that were made in the bad commit. Use the following command:
git revert <commit id>

Q7.Explain the difference between rebasing and merge in Git?
• Git rebase is a command that allows developers to integrate changes from one branch to another.
• Git merge is a command that allows you to merge branches from Git.

Git rebase and merge both integrate changes from one branch into another. Where they differ is how they used. Git rebase moves a feature branch into a master. Git merge adds a new commit, preserving the history.

Q8.What is a git stash?
git stash temporarily shelves (or stashes) changes you've made to your working copy so you can work on something else, and then come back and re-apply them later on.

```
```

##################### Build tool############################
Build tool (Make, ANT, Maven, Ivy, Gradle, and others)

https://www.devopsschool.com/blog/maven-tutorials-maven-lifecycle-phases-goal/
```
```
##########################################Jenkins#############################
```
```
Jenkins master ----jenkins salve architecture
The Jenkins master acts to schedule the jobs, assign slaves, and send builds to slaves to execute the jobs.

Jenkins server cannot handle multiple builds simultaneously for this, the Master distributes the workload and allows us
to run different builds on different environments each called a Slave.
```
```
Jenkins is an open source automation server. It helps automate the parts of software development related to building,
 testing, and deploying,facilitating continuous integration and continuous delivery.it is written in Java programming
 language. default port 8080.
#### build abort by jenkins console####################################
Jenkins.instance.getItemByFullName("build name").getBuildByNumber(179).finish(hudson.model.Result.ABORTED, new java.io.IOException("Aborting build"));

CI tools like Jenkins, TeamCity, Bamboo, GitLab, etc.

Jenkins Plugins: Plugins are the primary means of enhancing the functionality of a Jenkins. There are thousands of plugins
 available in Jenkins.

1) Git plugin for Jenkins. ...
2) Mailer Plugin ...
3) Kubernetes plugin for Jenkins. ...
4) SonarQube Plugin for Jenkins. ...
5) Docker plugin for Jenkins. ...
6) Maven Integration Plugin for Jenkins. ...
7) Amazon EC2 Plugin for Jenkins. ...
8) Build Pipeline Plugin for Jenkins.
9)JUnit Plugin 
10)Green Balls Plugin

Q1 In Jenkins, the “Choice Parameter” is a parameter that allows you to select a single value from a predefined list of values. 

Q2 How do I run a Jenkins job periodically?
The steps for scheduling jobs in Jenkins:
click on "Configure" of the job requirement.
scroll down to "Build Triggers" - subtitle.
Click on the checkBox of Build periodically.
Add time schedule in the Schedule field, for example: @midnight.

Q3 
What is the difference between poll SCM and build periodically?
Builds Periodically triggers builds as per the schedule (every 10 minutes) even if you haven't changed anything. Poll SCM will
 check for changes before triggering any build, if there are changes to the previous version there only build will be triggered.
 Builds Periodically is not recommended

Q4 How many slaves we can connect to master in Jenkins?
I recommend 1-200 agents per master as a practical maximum
'
Q5 A Jenkins slave node is simply a device configured to act as an automation executor on behalf of the master.The master will continue to perform basic operations and serve the user interface, while the slaves do the heavy lifting. 

sudo vi /etc/default/Jenkins  #8081 # change port 
sudo cat /var/lib/jenkins/secrets/initialAdminPassword  # default password path it hsow first time
```
```
CI vs CD: Continuous Integration (CI) is an approach of testing each change to codebase automatically, whereas Continuous Delivery (CD) is an approach to obtain changes of new features, configuration, and bug fixes.

Continuous Integration is a software development method where team members integrate their work at least once a day.
Continuous deployment: - Continuous deployment goes one step further than continuous delivery.
Continuous Deployment ensures that any change that passes through the stages of production is released to the end-users.

development without CI vs. Development with CI
Here are key differences between development using CI or without CI:
Development without CI	       Development with CI
Lots of Bugs	                Fewer bugs
Infrequent commits	            Regular commits
Infrequent and slow releases	Regular working releases
Difficult integration	        Easy and Effective Integration
Testing happens late	        Continuous Integration testing happens early and often.
Issue raised are harder to fix	Find and fix problems faster and more efficiently.
Poor project visibility	        Better project visibility

```
```

#Types of jobs or projects, New Build in Jenkins
1	Freestyle project. #Jenkins freestyle projects allow users to automate simple jobs. 
2	Maven project.
3	Pipeline.
4	Multibranch pipeline.
5	External Job.

Jenkinsfile is a text file that contains the definition of a Jenkins Pipeline and is checked into source control.

Jenkinsfile offers two types of syntax to create pipelines: declarative and scripted.

•	Declarative. Declarative Pipeline is a relatively recent addition to Jenkins Pipeline which presents a more simplified and
 opinionated syntax on top of the Pipeline sub-systems.
pipeline {

    agent any 

    stages {

        stage(‘Build’) { 

            steps {

                …….

            }

        }

        stage(‘Test’) { 

            steps {

                …….

            }

        }

        stage(‘Deploy’) { 

            steps {

                …….

            }

        }

    }

}
#	Scripted. A scripted pipeline uses the Groovy (JVM-based) language to create a pipeline as code.
•	
          Jenkinsfile (Scripted Pipeline)
•	
•	node {  
•	
•	    stage('Build') { 
•	
•	       …….
•	
•	    }
•	
•	    stage('Test') { 
•	
•	       …….
•	
•	    }
•	
•	    stage('Deploy') { 
•	
•	       …….
•	
•	    }
•	}


Login Jenkins -- Manage Jenkins---
•	Configure Global Security
•	Set configuration parameters that secure your Jenkins instance.
•	
•	Manage Credentials
•	Configure the credentials that provide secure access to third-party sites and applications that interact with Jenkins.
•	
•	Configure Credential Providers
•	Configure credential providers and types
•	
•	Manage Users
•	Manage users defined in the Jenkins user database. This is not used if you use a different security realm such as LDAP or AD.
•	
•	Status Information group
•	
•	System Information
•	Displays information about the Jenkins environment.
•	System Log
•	Jenkins log that contains all java.uil.logging output related to Jenkins.
•	Load Statistics
•	Displays information about resource utilization on you Jenkins instance.
•	About Jenkins
•	Provides version and license information for your Jenkins instance.
•	Troubleshooting group
•	Manage Old Data
•	Remove configuration information related to plugins that have been removed from the instance.
•	
•	Tools and Actions group
•	Screens for common management tasks and management tools that enable you to do administrative tasks without using the UI.

#!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

```
```
############################ ssh-server configration for cloud to enable user authictication with password ######################
yum install ssh-server
/etc/ssh/sshd_config
PasswordAuthentication and PermitRootLogin   # uncomment line
systemctl restart sshd  # restart sshd services after changes
```
```
################## update and user in sudoers file###################

vi /etc/sudoers  #  user ansible to run any command which requires root privileges.
amit ALL=(ALL) NOPASSWORD: ALL   # provide user become root permission
```
```
##################### password less authenticaltion ##########################
# user ansible 
ssh-keygen  # generate privite and public key
ssh-copy-id 192.168.1.3  # copied public in client machine
ssh ansible@192.168.1.3
```
```
#########################Ansible ###############################

http://www.datadisk.co.uk/html_docs/ansible/ansible_cheatsheet.html
https://www.golinuxcloud.com/ansible-cfg/
https://www.golinuxcloud.com/ansible-variables/ https://www.softwaretestinghelp.com/ansible-tutorial-1/
https://www.middlewareinventory.com/blog/ansible-ad-hoc-commands/

ANSIBLE_CFG: This environment variable is used, provided it is set
ansible.cfg: This is located in the current directory.

~/.ansible.cfg: This is located in the user's home directory

/etc/ansible/ansible.cfg # main confirmation file of ansible

log_path = /var/log/ansible.log

Default inventory file = /etc/ansible/hosts


# Ansible is a suite of software tools that enables infrastructure as code. It is open-source and the suite includes
 software provisioning, configuration management, and application deployment functionality.


#############inventory##########################################
An Ansible inventory file is a text file consisting of host names and IP addresses of remote servers that stores the information
of the target system where the Ansible script will be executed.

There are two types of Ansible inventories, depending on host management:
Static inventories-- it is divided 2 sub category (A)-default /etc/hosts and (B)custom inventory 
Dynamic inventories.

###########################Ad hoc command#######################

An Ansible ad hoc command uses the /usr/bin/ansible command-line tool to automate a single task on one or more managed nodes. ad hoc commands are
quick and easy, but they are not reusable.
ansible web -m ping  -b -K
#########################play##################################

A playbook is a list of plays.

##################################Playbook ##########################################
Ansible Playbooks is a yml file. In playbook written some tasks with help of module and command. When we run playbook
all task that automatically execute against hosts.

ansible-playbook httpd.yml -kK   # k ask user password and K ask sudo password

###################use before running playbook to find error######################
ansible-playbook httpd.yml -kK --syntax-check 
Using the --limit parameter of the ansible-playbook command is the easiest option to limit
###########Playbook work#################################
Playbooks are collections of one or more plays that are performed in a certain order. A play is an ordered sequence of tasks
 performed against hosts from your inventory.
The role is the primary mechanism for breaking a playbook into multiple files. This simplifies writing complex playbooks, 
and it makes them easier to reuse. The breaking of playbook allows you to logically break the playbook into reusable components.

##################################Ansible roles#######################################
Ansible roles allow you to develop reusable automation components by grouping and encapsulating related automation artifacts, like configuration files, templates, tasks, and handlers. Because roles isolate these components, it's easier to reuse them and share them with other people.
```
```
https://www.devopsschool.com/tutorial/ansible/ansible-roles-explained-with-examples.html
ansible-galaxy init /etc/ansible/roles/apache --offline

Directory Structure:
tasks - contains the main list of tasks to be executed by the role.
handlers - contains handlers, which may be used by this role or even anywhere outside this role.
defaults - default variables for the role.
vars - other variables for the role. Vars has the higher priority than defaults.
files - contains files required to transfer or deployed to the target machines via this role.
templates - contains templates which can be deployed via this role.
meta - defines some data / information about this role (author, dependency, versions, examples, etc,.)
Lets take an example to create a role for Apache Web server.

Ansible roles benefits:
1.	Allowing easy sharing of code with others
2.	Make larger projects more manageable
3.	Can use community-supported roles from Ansible Galaxy
4.	Can use rhel-system-roles as part of Red Hat Enterprise Linux
```
```
Run role command:-   ansible-playbook httpd.yml 
```
```
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
######################################## Teraform ##################################################
What is a Terraform used for?
Terraform is an IAC tool, used primarily by DevOps teams to automate various infrastructure tasks.The provisioning of cloud resources, for instance, is one of the main use cases of Terraform
Terraform is an infrastructure as code tool that enables you to safely and predictably provision and manage infrastructure in any cloud.

#Initialize Terraform. You only need to do this once per directory.

terraform init: Prepare your working directory for other commands
terraform plan: Show changes required by the current configuration
terraform apply: Create or update infrastructure
terraform destroy: Destroy previously-created infrastructure

terraform fmt                #Reformat
terraform fmt --diff — Display differences between original configuration files and formatting changes.

terraform fmt -help — Display help options for the fmt command.

terraform init -migrate-state — Reconfigure a backend, and attempt to migrate any existing state.

terraform apply --auto-approve #apply changes without being prompted to enter "yes"
terraform destroy --auto-approve #destroy/cleanup deployment without being prompted for “yes”
terraform plan -out plan.out #output the deployment plan to plan.out.
```
```
There are two types of backends in Terraform: local and remote. The local backend stores state file on your local filesystem, while the remote backend stores it on a remote service like AWS S3, Google Cloud Storage, or Terraform Cloud.

terraform init -migrate-state # migrate bekend 
##########migrate state file in s3##########
terraform { 
 backend "s3" {
    bucket                 = "terraformy"
    key                    = "state/terraform.tfstate"
    region                 = "us-east-1"
    encrypt                = true
    dynamodb_table = "terraformy_tf_lockid"
  }
}
#LockID
```
```

```
```
#########Terraform consists of two chief components: Terraform Core and Terraform Plugins.##########

Terraform Core: This component monitors the reading and interpolation of configuration files, resource plan executions, state management features, and resource graphs. Terraform Core is made up of compiled binaries written in the Go language.

Terraform Plugin: The plugins define resources for specific services, including initializing the libraries used to make API calls and authenticating infrastructure providers. As is the case with Terraform Core, Terraform Plugins are written in the Go programming language as executable binaries for either a specific server or as a provisioner.
Providers are plugins that implement the resource types. They contain all the necessary code to authenticate and connect to a specific service, usually from a public cloud provider, on the user’s behalf. Terraform supports 100 cloud providers, including Alibaba Cloud, AWS, Azure, Google Cloud Platform, Kubernetes, and the Oracle Cloud Infrastructure.
```
```
terraform refresh — Modify the state file with updated metadata containing information on the resources being managed in Terraform.
 Will not modify your infrastructure terraform show — Show the state file in a human-readable format.


Q1. Define Modules in Terraform?
Answer: A module in Terraform is a container for multiple resources that are used in tandem. Every Terraform that includes resources mentioned in.tf files requires the root module.

Cloudformation(aws)

```
```

##########################################Docker and virtual machine different ##################################
https://www.geeksforgeeks.org/difference-between-docker-and-virtualization/

               pysical server (laptop)
               Operating system---window, centos
               virtulation   --- virtual machine, vmware
               containerzation ---Docker,LXC,Podman

VM	                 Container
Less Efficient	         More Efficient
VMs run their own OS	 Containers share a host OS
Hardware Virtualization    OS Virtualization
More secure (segregated)   Less secure (Process-level isolation)

Containers are more lightweight compared to virtual machines (VM). Containers share the host OS kernel and libraries, eliminating the need to run a separate OS instance for each container like you would for a VM.

#############################docker hub and git different####################################

Docker Hub is primarily used for storing and sharing Docker images Docker Hub allows developers to build, test, and deploy
 Docker images while GitHub is used for version control and collaboration.

################Different terraform and Ansible ##############
https://www.geeksforgeeks.org/difference-between-terraform-vs-ansible/
What is the difference between Ansible and Terraform?

 Differentiate between Terraform and Ansible.
Answer: Ansible is a deceptively simple IT automation tool. Configuration management, application deployment, cloud provisioning,
 ad-hoc job execution, network automation, and multi-node orchestration are all handled by this software. Ansible simplifies
complex changes such as zero-downtime rolling updates with load balancers.
```

The following table compares and contrasts Ansible and Terraform:
Terraform	                                                   Ansible
Terraform is a tool for provisioning.	                       Ansible is a tool for managing configurations.
It uses a declarative Infrastructure as Code methodology.	   It takes a procedural method.
It’s ideal for orchestrating cloud services and building cloud
infrastructure from the ground up.                           	It is mostly used to configure servers with the appropriate software and to update resources that have previously been configured.
By default, Terraform does not allow bare metal provisioning.	The provisioning of bare metal servers is supported by Ansible.
In terms of packing and templating, it does not provide better support. 	It includes complete packaging and templating support.
It is strongly influenced by lifecycle or state management.   	It doesn’t have any kind of lifecycle management. It does not store the state.


These two tools help in automating configurations and deploying infrastructure. (ANSIBLE, TERRAFORM)
Terraform offers to deploy Infrastructure as a Code, helps in readability and lift and shift deployments. 

Terraform provides a mechanism to manage the status of infrastructure resources and handles the whole lifecycle of those resources, 
from creation to deletion. Ansible focuses on configuring and maintaining already-existing systems rather than managing the entire lifecycle.
```
Ansible is a configuration management tool for automating system configuration and management
Ansible is a suite of software tools that enables infrastructure as code. It is open-source and the suite includes software provisioning, configuration management, and application deployment functionality.
```
```

##########################Docker########################################################
# Download image from dockerhub. # create own custom image
create machine  
create network
create storge

```
There are four components that we will discuss in this Docker tutorial:
Docker client and server 
Docker image 
Docker registry 
Docker container

How Does Docker Work?
Docker works via a Docker engine that is composed of two key elements:
a server and a client; and the communication between the two is via REST API. The server communicates the instructions to the client

https://geekflare.com/docker-commands/   # command list

```
```
What are disadvantages of Docker?
Disadvantage of Dockers
Docker is not good for application that requires rich GUI.
It is difficult to manage large amount of containers.
Docker does not provide cross-platform compatibility means if an application is designed to run in a Docker 
container on windows, then it cannot run on Linux Docker container.

    #############Virtual Machine Vs Docker#############

Narration	                                         Virtual                 Machine	Docker
Infrastructure Management                           Hypervisor Layer         Docker Engine layer
Memory Usage                                        Very high                       Very low
Memory Reallocation                              Not possible                Unused memory can be reallocated to other containers
Performance        As virtual machines increase, the performance decreases  As Docker uses a single engine, the performance is high, regardless of the increase in containers
Boot Time                                         VMs take time to boot          Docker containers take milliseconds to boot on.
Portability     Virtual machines depend on the Host OS, libraries and dependencies. So, portability is a challenge  Docker is highly portable


```
```
Docker Hub is primarily used for storing and sharing Docker images. Docker Hub allows developers to build, test, and deploy Docker
 images.

Docker is a software platform that allows you to build, test, and deploy applications quickly.

A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image.
By default, Docker uses the Overlay2 driver, which stores images in a directory called /var/lib/docker/overlay2 .


docker run – This command is used to start a new Docker container from an image.
docker ps – This command is used to list all the running Docker containers.
docker stop – This command is used to stop a running container.
docker rm – This command is used to remove a Docker container.
docker images – This command is used to list all the Docker images that are currently available on your system.
docker pull – This command is used to download a Docker image from a registry.
docker exec – This command is used to execute a command in a running container.
docker-compose – This command is used to manage multi-container Docker applications.

# docker search centos9 # to search mysql realted images from Dockerhub

# docker pull centos9  # this command pulls a specific image from the Docker Hub.

# docker run --name nginx-root -p 80:80 -d nginx   ####-d or --detach helps in running the container in the background in detached mode.

# docker exec -ti nginx-root /bin/bash   # remote like ssh

# docker run -id --name=my-website --cpus=1.5 --memory=2048m -p 80:80 -v ./website:/usr/share/nginx/html/ nginx:latest
https://phoenixnap.com/kb/docker-volumes

https://blog.devops.dev/creating-a-docker-bridge-network-a085ff8559c3

https://www.mygreatlearning.com/blog/top-essential-docker-commands/
```
```

################################ Docker compose###############################

Docker Compose is a tool that helps you define and share multi-container applications. With Compose, you can create a YAML file to define the services and with a single command, you can spin everything up or tear it all down.
we define a multi-container application in a single file, then spin your application up in a single command which does everything that needs to be done to get it running

https://github.com/wrender/docker-compose-lamp/blob/master/docker-compose.yml
https://medium.com/@sajjad_dehghani/php-7-3-25-apache-dockerfile-22b26ebb78d9 
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-centos-7

docker-compose up -d
docker-compose down
docker-compose stop
docker-compose rm 
```
```
##################################kubernet ############
Kubernetes is a portable, extensible, open source platform for managing containerized workloads and services  that facilitates both declarative configuration and automation. It has a large, rapidly growing ecosystem. Kubernetes services, support, and tools are widely available.

master
These components are the API server, etcd, scheduler, controller-manager,container runtime and cloud controller manager.

The controller manager. This component is a single binary composed of four sub-processes and they are:

The node controller: Responsible for the health of the nodes in the cluster. The replication controller: responsible for keeping the desired amount of pods for each replication. The endpoints controller: handles the Endpoints object that links services and pods. The service account and token controller: handles the default accounts and API access for namespaces.

Client nodes
kubelet, kubeproxy,container runtime

The kubelet, which makes sure all containers are running and healthy.

https://www.bluematador.com/learn/kubectl-cheatsheet  #### importtant 

https://kubernetes.io/docs/concepts/overview/
A Kubernetes cluster consists of a set of worker machines, called nodes, that run containerized applications. Every cluster has at least one worker node.

https://kubernetes.io/docs/concepts/overview/components/

https://codefresh.io/learn/kubernetes-deployment/top-6-kubernetes-deployment-strategies-and-how-to-choose/
https://spot.io/resources/kubernetes-autoscaling/5-kubernetes-deployment-strategies-roll-out-like-the-pros/

```
```
ELB is a generic term for AWS load balancing services that have three types of attractive load balancers: ALB, CLB, and NLB.

Compared to CLBs, ALBs are more distinctive in many ways and have their own unique appeal.
For example, the following points are characteristic of ALB.

・ Operation in Layer 7 (Application Layer)
Older ELBs acted as load balancers, both in the transport layer at layer 4 and the application layer at layer 7.
Layer 4 balances the load without scrutinizing the contents of the network packets, and Layer 7 balances the load more efficiently by accessing information such as HTTP and HTTPS in the packets.

On the other hand, ALB is a load balancer that only works with Layer 7, and unlike ELB, it has a style that specializes in the application layer.
This has allowed for the implementation and addition of more useful and easy-to-use features and increased overall support.

・ Supports WebSocket and HTTP/2
The ALB now supports two new protocols, WebSocket and HTTP/2, which expands the user's choice.
By supporting each communication standard, network traffic can be reduced and connections can be used more efficiently.

・ Targets the latest application architectures
When using the ALBs, you can configure them for the latest application architectures, such as micro services and containers.
It provides advanced request routing, so you'll be able to use it more freely and smoothly.

・ Can route to target groups
An ALB can tie instances to different groups of servers, called target groups, and configure routing.
Unlike ELBs, which are directly instantiated, services can be run independently and multiple routing rule definitions can be created.
```
```



```
```

Web server: a computer program that serves requested HTML pages or files. In this case, a web browser acts as the client. (Httpd, tomcat, nginx)
Application server: a program in a computer in a distributed network that provides the business logic for an application program. (Tomcat etc.)
```
```
https://www.guru99.com/what-is-aws.html

1. Cloud computing is the on-demand delivery of compute power, database, storage, applications, and other IT resources through a cloud services platform via the internet with pay-as-you-go pricing.

2. EC2 ( Amazon Elastic Compute Cloud ) is a web service that provides secure, resizable computing capacity in the cloud. just like a virtual machine.
The AWS EC2 Instance Types are as follows:
General Purpose Instances
Compute Optimized Instances
Memory-Optimized Instances
Storage Optimized Instances
Accelerated Computing Instances

3. ######################differnce s3 and EC2############################################
Amazon Simple Storage Service (S3) and Amazon Elastic Compute Cloud (EC2) are two major storage services for AWS.
S3 provide block level storge service and ec2 provide compute service.

4. ##########################################S3#####################################################
S3 is object storage service designed for incredible durability, high scalability, availability, security, and performance.
 It has various storage classes for different use cases

5. Amazon Glacier- It is an extremely low-cost storage service. It offers secure and fast storage for data archiving and backup.

6. ###############################Route 53###########################################

Route 53 is an advanced, highly available, and scalable DNS Service. it provide various routing types like GeoDNS, Geoproximity,
and Latency Based Routing. Together with health checks and DNS failover, this enables different fault-tolerant low-latency
architectures configurable with a simple visual editor.

7. ######################Amazon VPC (Virtual Private Cloud)#################
VPC is logically isolated virtual networks inside AWS. You have full control over the configuration of the network, its subnets,
 and routing tables.

8. #########################Amazon EBS (Elastic Block Storage)##################################
EBS is generic long-term high-performance block storage for EC2 instances. It’s designed for both throughput and transactional
 workloads and can scale to petabytes of data.

9. Amazon Elastic Container Service (Amazon ECS) is a highly scalable, fast container management service that makes it easy to run, stop, and manage containers on a cluster. ECS comes with two launch types: EC2 and Fargate.
9A. EKS (Elastic Container Service for Kubernetes)- The tool allows you to Kubernetes on Amazon cloud environment without installation.

10. IAM (Identity and Access Management)— IAM is a secure cloud security service which helps you to manage users, assign policies,
form groups to manage multiple users.

11. Amazon RDS- This Database AWS service is easy to set up, operate, and scale a relational database in the cloud.

12. AWS Auto Scaling— The service allows you to automatically scale your resources up and down based on metrics.

13. Amazon CloudWatch: The tools monitor AWS resources like Amazon EC2 and Amazon RDS DB Instances. It also allows you to monitor
 custom metrics created by user’s applications and services.

14. AWS Lambda is an event-driven, serverless computing service that lets you run code without provisioning or managing servers.

What is AMI in AWS EC2?
Instances and AMIs - Amazon Elastic Compute Cloud

15. An Amazon Machine Image (AMI) is a template that contains a software configuration (for example, an operating system, an
 application server, and applications)

16. IgW allows both inbound and outbound access to the internet whereas the NAT Gateway only allows outbound access.

17. NAT gateway gives cloud resources without public IP addresses access to the internet without exposing those resources to incoming internet connections

18. Elastic Load Balancing automatically distributes your incoming traffic across multiple targets, such as EC2 instances, containers, and IP addresses, in one or more Availability Zones. It monitors the health of its registered targets, and routes traffic only to the healthy targets. Application Load Balancers, Network Load Balancers, Gateway Load Balancers, and Classic Load Balancers.

19. A security group acts as a firewall that controls the traffic allowed to and from the resources in your virtual private cloud (VPC).

```
```
#################################DATABASE#################################
There are two types of SQL databases: relational (SQL) and non-relational (NoSQL)
Relational Database Service (Amazon RDS) exm. MySQL, PostgreSQL

sudo grep "A temporary password" /var/log/mysqld.log

mysql_secure_installation  #Config the MySQL root user

mysql -u root -p  # Log in to MySQL

CREATE DATABASE example_database;  # create database with name example_database

CREATE USER 'example_user'@'%' IDENTIFIED BY 'password';  # user for example_database database

GRANT ALL ON example_database.* TO 'example_user'@'%'; # Now give this user permission over the example_database database:

CREATE TABLE example_database.breakfastMenu(food VARCHAR(50), description VARCHAR(255));  #Create a breakfastMenu table in the testDB

https://www.tecmint.com/mysql-backup-and-restore-commands-for-database-administration/

https://www3.ntu.edu.sg/home/ehchua/programming/sql/MySQL_Beginner.html

```
```
####################### Monitering##########################

Zabbix is an open-source software tool to monitor IT infrastructure such as networks, servers, virtual machines, and cloud services.
Zabbix collects and displays basic metrics. The Zabbix monitoring tool is used to provide monitoring metrics and monitor network usage, disk space consumption, and CPU load. (LAMP +zabbix)
```
```
Prometheus is a free software application used for event monitoring and alerting. It records metrics in a time series database built using an HTTP pull model, with flexible queries and real-time alerting.

```
```
Grafana is a multi-platform open source analytics and interactive visualization web application. It provides charts, graphs, and alerts for the web when connected to supported data sources.
https://www.projectpro.io/compare/prometheus-vs-zabbix
```


