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

#### Arriving at a definition of "Cloud" 

Given the set of definitions from around the industry, and some of the characteristics that we've distilled from these industry definitions. It seems apropos to assert that a cloud should be
```java
A network of servers that live in different geo's and are connected by an overlay network. This collection of compute should have a common API from which to provision, scale, and communicate with resources across a common network overlay. 

This definition would then imply anything from an industry leader such as AWS, Azure, or GCP would likely meet the definition of a cloud; however, so could a multi-datacenter set of compute as long as it presented an API from which to provision, scale, and communicate across network resources. 
```

