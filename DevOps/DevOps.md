
DevOps is the term used for the practice of collaboration and communication between software engineers and Information Technology professionals. 

- It support cross department communication by promoting set of process and methods in different department development, QA and IT Operations.     
- It promote the development of agile infrastructure.     
- It also allow formation of Cross-functional team (we can refer it as Dev-ops team). 

As this pratise touches to different department, it need set of tools which commonly refered as Devops tool chain for different functionality. 

1. Code:-  Version controlling tools     
2. Build:- Continuous integration tools (example: Jenkins)     
3. Test:- Continuous Testing tools     
4. Package:- Package Repository tools, Package pre-deployment staging     
5. Release:- Change Management, Release Approval, Release approval     
6. Configure: - Infrastructure configuration and management, Infrastructure as code tool. (Puppet)     
7. Monitor:- Application Performance monitoring and end user experience.

## Virtualization
Dockers & Vagrant support environment requirement by virtualization. 

Vagrant is software product for building and maintaining portail virtual environment. It is written in ruby. 

It uses Provisioners and Providers as building blocks to manage the development environment. 

- Puppet and chef are the two most widely used provisioners in the vagrant ecosystem 
    
- Providers are the services that vagrant uses to uses to set up and create virtual environments. [supports for virtualbox, hyper-v and Docker virtualization ships while support VMware and AWS are supported via plugins] 
    
- Technically Vagrant is wrapper on virtualization and help developers to automates the configuration of virtual environment using Chef or puppet. 
    
- Machine and software requirement are written in file called "Vagrantfile" to execute necessary steps in order to create a development-ready box. 
    
- Box is format and .box is extension for vagrant

## WinOps focused tools

1. **Ansible** :
	- Ansible is automation engine that automates software provisioning , configuration management and application deployment. 
	- It is included as part of Fedora distribution and available for Redhat enterprise linux, centos and scientific linux via enterprise linux (EPEL) 
	- It is also available for other Operating system. 
	- Ansible has two types of server (Controlling machines and nodes). 
	- Nodes are managed by Controlling machines overs SSH. 
	- Controlling machines describes the location of nodes through its inventory. 
	- It deploys module to nodes over SSH. Modulle are stored in nodes and communicate with controlling machine through a JSON protocol over the standard ouput. 
	- Ansible is Agentless architecture, where agents are not required to be installed on the nodes. So no background daemons are running on node, it reduces overhead on the network by preventing the nodes from polling the controlling machines.

2. BuildMaster 

4. **Chef** 
	Chef is configuration management tool written in Ruby and Erlang.
	
	It can be used to streamline the task of configuring and maintaining persona servers, cloud based servers such as internap, Amazon EC2, Google Cloud Platform, OpenStack, Softlayer, Microsoft Azure and Rackspace.
	
	Recipes are features how chef manages server application and utilities .  This recipes guide how different servers apache http-server , mysql, hadoop, etc are configured.
	
	Recipes can be grouped in as cookbook for easier management. 
	Architecture: 
	- It can run in both standalone or client/server mode.
	- In client/server mode, client sends various attributes about the node to server. 
	- The server uses Solr to index these attributes and provides an API for clients to query this information. 
	- Recipes can query this attributes and can configure the nodes.

1. Chocolatey 
2. Docker 
3. NuGet 
4. Octopus Deploy 
5. Otter 
6. PowerShell 
7. Puppet 
8. TeamCity 
9. Team Foundation Server 
10. Vagrant 
11. Visual Studio Release Management
