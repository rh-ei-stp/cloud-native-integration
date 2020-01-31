# What is “Cloud Native”? 
*An Enterprise Integration Practice Perspective* 


## Common Definitions

### CLOUD
**M$**
The definition for the cloud can seem murky, but essentially, it’s a term used to describe a global network of servers, each with a unique function. The cloud is not a physical entity, but instead is a vast network of remote servers around the globe which are hooked together and meant to operate as a single ecosystem. These servers are designed to either store and manage data, run applications, or deliver content or a service such as streaming videos, web mail, office productivity software, or social media. Instead of accessing files and data from a local or personal computer, you are accessing them online from any Internet-capable device—the information will be available anywhere you go and anytime you need it.

Businesses use four different methods to deploy cloud resources. There is a public cloud that shares resources and offers services to the public over the Internet, a private cloud that isn’t shared and offers services over a private internal network typically hosted on-premises, a hybrid cloud that shares services between public and private clouds depending on their purpose, and a community cloud that shares resources only between organizations, such as with government institutions.
https://azure.microsoft.com/en-us/overview/what-is-the-cloud/

**IBM**

Cloud computing, often referred to as simply “the cloud,” is the delivery of on-demand computing resources — everything from applications to data centers — over the internet on a pay-for-use basis.

    Elastic resources: Scale up or down quickly and easily to meet changing demand.
    Metered services: Pay only for what you use.
    Self-service: Find all the IT resources you need, with self-service access.
https://www.ibm.com/cloud/learn/cloud-computing

**RedHat**
Clouds are IT environments that abstract, pool, and share scalable resources across a network. Clouds are usually created to enable cloud computing, which is the act of running workloads within that system. Neither clouds nor cloud computing are technologies unto themselves.

    Clouds are environments—places where applications run.
    Cloud computing is an act—the function of running a workload in a cloud.
    Technologies are things—software and hardware used to build and use clouds.



### CLOUD NATIVE

**CNCF**

“Cloud-native technologies empower organizations to build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds. Containers, service meshes, microservices, immutable infrastructure, and declarative APIs exemplify this approach.

These techniques enable loosely coupled systems that are resilient, manageable, and observable. Combined with robust automation, they allow engineers to make high-impact changes frequently and predictably with minimal toil.” https://github.com/cncf/foundation/blob/master/charter.md


**Pivotal**

 “Cloud-native is an approach to building and running applications that exploits the advantages of the cloud computing delivery model. Cloud-native is about how applications are created and deployed, not where.” https://pivotal.io/cloud-native

**Microsoft** 

Could not find a “definition”; however, M$ indicates cloud native is identified by the 5 pillars depicted in this schematic. https://docs.microsoft.com/en-us/dotnet/architecture/cloud-native/definition 



**VMWare** 
*Closest I could find to a definition*: “Cloud native technologies provide resiliency and auto-scaling through the use of microservices – modular applications that can be deployed, updated, scaled, and restarted without impact to the system or end users. Enterprises and service providers can deliver superior customer experiences 24x7.” https://www.vmware.com/solutions/cloud-native-apps.html

**IBM**

“Cloud native refers less to where an application resides and more to how it is built and deployed.
A cloud native application consists of discrete, reusable components known as microservices that are designed to integrate into any cloud environment.
These microservices act as building blocks and are often packaged in containers.
Microservices work together as a whole to comprise an application, yet each can be independently scaled, continuously improved, and quickly iterated through automation and orchestration processes.
The flexibility of each microservice adds to the agility and continuous improvement of cloud-native applications.” https://www.ibm.com/cloud/learn/cloud-native#toc-what-is-cl-OOTvI6Ql

**Red Hat** 
“Ideally,a cloud-native app is a collection of small, independent, and loosely coupled microservices, deployed in Linux containers, and connected through application programming interfaces (APIs) or a mesh network for message routing. Each service implements a business capability, and is developed by small teams using DevOps workflows like continuous integration and continuous deployment (CI/CD).” https://www.redhat.com/en/topics/cloud-native-apps/why-choose-red-hat-cloud-native 

**10 KEY ATTRIBUTES OF CLOUD-NATIVE APPLICATIONS**
“Cloud native is a term used to describe container-based environments. Cloud-native technologies are used to develop applications built with services packaged in containers, deployed as microservices and managed on elastic infrastructure through agile DevOps processes and continuous delivery workflows.”
https://thenewstack.io/10-key-attributes-of-cloud-native-applications/

## Cloud Characateristics 

Characteristic | Originator | Analysis 
-------------- | ---------- | --------


## Cloud Native Characteristics

Characteristic | Originator | Analysis
-------------- | ---------- | --------
Elasticity | David Gordon [Gordo](https://www.redhat.com/en/about/videos/considerations-for-migrating-cloud-native-architectures) | N/A
On Demand Scaling | David Gordon [Gordo](https://www.redhat.com/en/about/videos/considerations-for-migrating-cloud-native-architectures) | N/A
Loosely coupled | CNCF | N/A 
Resilient | CNCF | N/A
Manageable | CNCF | N/A
Observable | CNCF | N/A
Frequent Change | CNCF | N/A
Minimal Toil | CNCF | N/A
Exploits values of cloud computing delivery model | CNCF | N/A
Focus on build and deployment | Pivotal | N/A 
location agnostic | Pivotal | N/A
5 Pillars: * Microservices * Modern Design * Containers * Backing services * Automation | M$ | N/A
Deployed, updated, scaled, and restarted without impact to the system or end users. | VMWare | N/A 
Microservices that are designed to integrate into any cloud environment | IBM | N/A
Microservices deployed into containers | Red Hat | N/A
Communicate via API | Red Hat | N/A 
Mesh network for message routing | Red Hat | N/A
Elastic Infrastructure | [New Stack Article](https://thenewstack.io/10-key-attributes-of-cloud-native-applications/)|N/A

## What is Cloud Native Integration?

### Tenets of Enterprise Integration

* Service Oriented Architecture  
* MicroService Architecture 
* Usage of Enterprise Integration Patterns: [EIP](https://en.wikipedia.org/wiki/Enterprise_Integration_Patterns)

### Are Current Enterprise Integration Practices “Cloud Native”?
* Cloud Native Characteristics 
  * Event and Complex event driven behaviour 
  * MicroService decomposition fits nicely into traditional SOA concepts 
  * Single Responsibility
  * Fault isolation 
  * Domain isolation  
  * Implies loose coupling between service endpoints 
  * API oriented 
  * Patterns provide meaningful idioms to connect loosely coupled services 


* Not Cloud Native
  * Legacy tooling does not exploit platform capabilities 
  * Dependence on other tools to scale to demand
  * Dependence on other tools to scale to zero 
  * No built in notion of location transparency for components that live outside of a runtime 
  * Appliances (message broker or esb) that decouple service endpoints are not cloud native
  * Capabilities largely dependent on underlying platform
