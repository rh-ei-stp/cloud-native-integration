# What is “Cloud Native” Integration? 
*A Red Hat Integration Solution Technology Practice Perspective* 

The terms **"cloud"** and **"Cloud Native"** have become important in the software industry alluding, to significant change and a flurry of new techniques aimed at providing ever increasing efficiency, and efficacy for modern compute platforms. "Cloud Native", when used to describe software, implies architecture that capitalizes on the capabilities of "cloud" infrastructure, however, there is no clear consensus around which concrete architectural characteristics should be exhibited by Cloud Native deployments. Some of this ambiguity derives from inconsistent definitions of the term "cloud" itself, and the relevant context applied when cloud infrastructure is in use.

More specifically, as enterprises attempt to solve common problems using integration technologies and middleware at large, implementation teams are often left to determine for themselves how best to leverage cloud infrastructure and Cloud Native architecture for efficiency, stability, and reliability gains.

The purpose of this document is to suggest common definitions for the terms "cloud" and "Cloud Native" in order to explore how this context impacts considerations for integration tiers of enterprise software.

We intend to support a hypothesis that integration patterns in a cloud context require a new architectural approach which we have labeled **Cloud Native Integration**.


## Defining Terms

Here we suggest a definition for **"Cloud"**: [What is Cloud?](definition-cloud.md)

Here we suggest a definition for **"Cloud Native"**: [What is Cloud Native?](definition-cloudnative.md)


### Is Microservice Architecture *Cloud Native*?
Microservice architecture is complementary to Cloud Native architecture, however there are Cloud Native architectural considerations that are not necessarily relevant in all Microservices contexts. Here we discuss this in detail: [Is Microservice Architecture Cloud Native?](msa-cloudnative.md)


## **Cloud Native Integration**  
Enterprise software traditionally requires integration capabilities, and a cloud context exposes additional integration use cases. An increasing number of organizations aim to deploy software to multiple clusters and clouds, and need to support workload migrations from traditional environments to cloud environments, **integration becomes a front and center feature** of a Cloud Native enterprise architecture. 

Here we explain why a container platform is the *Cloud Native* run time of choice for **Cloud Native Integration**: [Integration and the Container Platform](cloud-native-container-platform.md)

Here we define **Cloud Native Integration** and why it is an important evolutionary leap for our modern enterprise architecture(s): [What is Cloud Native Integration?](what-is-cloud-native-integration.md) 
