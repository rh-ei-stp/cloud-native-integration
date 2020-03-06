# What is “Cloud Native”? 
*An Enterprise Integration Practice Perspective* 

The terms "Cloud" and "Cloud Native" have become two pivotal terms in the software industry implying significant change and a flurry of new techniques aimed at providing ever increasing efficiency, and efficacy 
for modern compute platforms. These terms; however, are not often well defined and it is often unclear what the implications of the use of a new "cloud" or "cloud native" model might imply for applications and architecture delivered to this platform. 

More specifically, as enterprises attempt to solve common problems solved by integration technologies and middleware at large, what if any difference is implied by this technique is often left up to implementers who may or may not be leveraging this new found compute platform for its efficiency, stability, and reliability gains. 

The purpose of this document is to come to a common understanding of what these terms mean and what this might all means for traditional enterprise software and their integration tiers. 

## Common Definitions

Let's look at some common definitions of these terms. 

### CLOUD

#### Cloud Definitions 
Some industry leading organizations define the term "cloud" in the following ways: 

**Microsoft**
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



#### Cloud Characateristics 

Characteristic | Originator | Analysis 
-------------- | ---------- | --------
A Global network of servers as a single ecosystem| Microsoft | If we can assume the term "global" can be applicable to a reduced set of geo's (i.e. it implies more than one geo), this characteristic seems apropos. 
Delivery of on-demand computing resources | IBM | This is the most conventional description of a cloud, and implies an API like view towards resource provisioning 
Elastic resources | IBM | This implies a request/response like API for resource provisioning 
Self Service | IBM | This implies again an API like contract.
IT environments that abstract, pool, and share scalable resources across a network | Red Hat | This characteristic implies a central contorl plane, and central network overlay
Not a Technology Unto Itself | Red Hat | Worth noting, but, not a meaningful enough characteristic to consider 

#### Digesting the term "Cloud" 

Given the set of definitions from around the industry, and some of the characteristics that we've distilled from these industry definitions. It seems apropos to assert that a cloud should be
```java
A network of servers that live in different geo's and are connected by an overlay network. This collection of compute should have a common API from which to provision, scale, and communicate with resources across a common network overlay. 

This definition would then imply anything from an industry leader such as AWS, Azure, or GCP would likely meet the definition of a cloud; however, so could a multi-datacenter set of compute as long as it presented an API from which to provision, scale, and communicate across network resources. 
```

### CLOUD NATIVE


#### Cloud Native Definitions 
Here is a sample of some definitions used by leaders across the software industry: 

**CNCF**

“Cloud-native technologies empower organizations to build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds. Containers, service meshes, microservices, immutable infrastructure, and declarative APIs exemplify this approach.

These techniques enable loosely coupled systems that are resilient, manageable, and observable. Combined with robust automation, they allow engineers to make high-impact changes frequently and predictably with minimal toil.” https://github.com/cncf/foundation/blob/master/charter.md


**Pivotal**

 “Cloud-native is an approach to building and running applications that exploits the advantages of the cloud computing delivery model. Cloud-native is about how applications are created and deployed, not where.” https://pivotal.io/cloud-native

**Microsoft** 

Microsoft indicates cloud native is identified by the 5 pillars depicted in this schematic. 
![Microsfot's 5 Pillars](https://docs.microsoft.com/en-us/dotnet/architecture/cloud-native/media/cloud-native-foundational-pillars.png)
 https://docs.microsoft.com/en-us/dotnet/architecture/cloud-native/definition
 
**VMWare** 

*Closest to a definition*: “Cloud native technologies provide resiliency and auto-scaling through the use of microservices – modular applications that can be deployed, updated, scaled, and restarted without impact to the system or end users. Enterprises and service providers can deliver superior customer experiences 24x7.” https://www.vmware.com/solutions/cloud-native-apps.html

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



#### Cloud Native Characteristics

Characteristic | Originator | Analysis
-------------- | ---------- | --------
Elasticity | Red Hat (https://www.redhat.com/en/about/videos/considerations-for-migrating-cloud-native-architectures) | As the underlying platform features resource elasticity, this characteristic seems key
On Demand Scaling | Red Hat (https://www.redhat.com/en/about/videos/considerations-for-migrating-cloud-native-architectures) | As this is a feature of an underlying platform, it would seem workloads must approximate notions of on-demand scaling as well 
Loosely coupled | CNCF | As workloads deploy to elastic, API driven clouds that are connected by network overlays, this characteristic seems apropos to achieve other objectives such as HA, etc., but does not seem a prioiri 
Resilient | CNCF | Given an ephemeral notion of compute provided by a cloud, it seems critical that workload deployments be resilient 
Manageable | CNCF | This seems acceptable as a characteristic of software in general, and likely required to exploit underlying cloud characteristics 
Observable | CNCF | If the underlying platform is ephemeral and elastic, observability raises in importance 
Frequent Change | CNCF | This is one of the often marketed advantages of cloud computing technology; however, it is unclear that this is more than a nice to have. For instance, could a deployment be static and not incur frequent change, but still be "cloud native"?
Minimal Toil | CNCF | It is unclear if this is a nice to have as much as it is a requirement of a deployment to be native to cloud deployment capabilities 
Exploits values of cloud computing delivery model | CNCF | This seems clear and perhaps some other CNCF characteristics should be nestled under this statement 
Focus on build and deployment | Pivotal | Isn't this true of any enterprise software deployment? 
Location agnostic | Pivotal | This characteristic seems critical to notions of being ready for cloud deployments
5 Pillars: * Microservices * Modern Design * Containers * Backing services * Automation | Microsoft | Unfortunately, it is difficult to assert "modern design" and other pillars of cloud native deployment as depicted by these characteristics 
Deployed, updated, scaled, and restarted without impact to the system or end users. | VMWare | To take advantage of underlying elasticity, and provisioning capabilities, this characteristic seems of critical importance 
Microservices that are designed to integrate into any cloud environment | IBM | Deployment into any cloud environment seems mandatory; however, the analysis as to why these deployments can only be microservices seems inadequate. 
Microservices deployed into containers | Red Hat | While it may be possible that containers lend themselves towards cloud native deployments, it is unclear that containers must be the deployment target to be cloud native themselves 
Communicate via API | Red Hat | This implies a request/response pattern must be followed for deployments into the cloud to be native to it. While API driven deployments do seem apropos for cloud environments, the absence of this communication strategy does not seem like a requirement to be native to cloud deployments (for instance, cloud native deployments may be event driven via messaging appliances) 
Mesh network for message routing | Red Hat | While this seems apropos, and might ensure messaging appliance viability in a cloud deployment, the absence of this should not preclude deployments being labeled "cloud native"  
Elastic Infrastructure | [New Stack Article](https://thenewstack.io/10-key-attributes-of-cloud-native-applications/)| While being capable of exploiting underlying platform capabilities categorically is required of cloud native deployments, this characteristic seems more descriptive of the underlying platform than deployments that sit on top of it 

#### Digesting "Cloud Native" Definitions and Characteristics 

While many industry leaders define the term "cloud native", many of these definitions depend on product tooling or architectural concerns that the company advocates as opposed to defining the term more generally without speaking directly to product or architectural technique. It is the opinion of the Enterprise Integration Practice, that (for instance, in the case of the use of microservices) some of these products and techniques are adequate architectural techniques, and are "cloud native" in an of themselves, but are not required to label a deployment "cloud native" (to reiterate, the use of microservices may imply a "cloud native" deployment, but the absence of microservices does not imply that a deployment is not "cloud native" per se). 

This begs the question, then, what are the minimum set of characteristics to determine a technology choice, architectural concern, or deployment "cloud native"?

Characteristic | Why is this "Cloud Native"?
-------------- | --------------------------
Elasticity | As this is a core characteristic of underlying cloud platforms, any workload that sits on top of a "cloud" must be capable of exploiting this capability as a core technology feature
On Demand Scaling | As this is a core characteristic of underlying cloud platforms, this should be a core feature of any "cloud native" technology, architectural approach or deployment 
Resilient | High Availability should be a core concern of any technology or deployment. This implies both meainingful availability in calm and turbulent waters (i.e. outage of an availability zone, data center, etc.).  
Manageable, Observable | As the nature of a cloud platform provides some control plane (likely API based) to provision, manage and observe infrastructure deployments from the platform, these seems like core characteristics of any technology or deployment that is meant to be native to that platform 
Location agnostic | To be able to be effective in a cloud environment, it is critical that the underlying details of said cloud be abstracted away from technologies and deployments. This loose coupling of technology to platform implies an abstraction that allows the technology to be native to cloud as an architectural concept as opposed to a product. For instance, if something only works in a single compute deployment due to tight coupling to a proprietary platform it would only be useful to declare something native to that cloud
Communicates via an "API" | We use "API" here loosely, as we define loosely define this term to include events, event streams, as well as more standard API taxonomy such as REST, SOAP, etc.

Now that we have established a core set of characteristics, it worthwhile to take a peak at our current set of architectural prescriptions, products, and rules of thumb to determine if this implies a greater enterprise software impact (and more specifically how we integrate our enterprise) to applications and workloads that we run on the "cloud" in a "cloud native" way.  

## What is Cloud Native Integration?

Given a definition of cloud and cloud native, and given that we can distill a set of traits that seem to follow for these definitions, does this imply a changing view for traditional enterprise integration techniques? 

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
