## What is Cloud Native Integration?

Given a definition of cloud and cloud native, and given that we can distill a set of traits that seem to flow from these definitions, does this imply a changing view for traditional enterprise integration techniques? 

While many of our traditional enterprise integration products might display some but do not meet the entire set of characteristics we define as "Cloud Native" (for instance, while an ESB likely does not promise us elasticity out of the box, it does promise us notions of location transparency (location agnostic), and likely communicates along the bus over an "API" given our loose definition of what an API is), our traditional enterprise integration patterns and idioms do apply. 

For instance, as we communicate over API's, traditional enterprise integration patterns such as enrichment and service mediation become front and center requirements as we orchestrate our feature needs across the enterprise. As we adopt architectural techniques such as decomposition into microservices that are cloud native, enterprise integration patterns become even more critical as on demand scaling, location agnostic deployment, communication via an API all imply a need for enterprise integration techniques to help orchestrate, and provide choreography for these types of deployments. 

As a result, given that we have an even greater need for integration now that we have adopted "Cloud Native" characteristics for our deployments, it seems neccessarry to introduce this integration tier as a "Cloud Native" deployment itself. 

### Tenets of Enterprise Integration

When discussing what it is we mean by "Enterprise Integration" it may be worthwhile to elaborate some of the underlying fundamentals of this discussion. 

* **Service Oriented Architecture** - Enterprise Integration really began to take hold in enterprises during the rise of Service Oriented Architecture (SOA). While describing the entirety of Service Oriented Architecture is beyond the scope of this document, it is worth noting that SOA began to propose notions of single responsibility, communication over an API, and an event based nature to deployment via message brokers and enterprise service bus capabilities. This architectural reference put enterprise integration patterns front and center in how it addressed activities across the enterprise. 
* **MicroService Architecture** - Earlier in this document we took a look at descriptions and definitions of MicroService architecture (MSA). MicroService Architecture; however, implies modernization of many of the same principles we had adopted in Service Oriented Architecture, and began to identify tooling, technique (CICD for instance), and architectural views (decomposition via a bounded context for instance) that lended themselves more neatly to further decomposition into meaningful units that imply single responsibility (and other twelve factor techniques). As a result, MicroService Architecture began to notice adoption across all modern enterprise integration tooling and techniques and moves away from monolithic deployments into large appliances (such as ESB's) began to be less favoured as much smaller deployments leveraging the same architectural techniques that were seen in traditional enteprise integration tooling (for instance, our microservices will still event driven and may have still used an API, message broker, or other appliance that was typical of traditional enterprise integration deployments). 
* **Enterprise Integration Patterns** - [EIP](https://en.wikipedia.org/wiki/Enterprise_Integration_Patterns). While fully elaborating "Enterprise Integration Patterns" is beyond the scope of this document, it is worth noting that these patterns are core to what we describe as "Enterprise Integration" or an "Integration Tier" across our enterprise. 

These techniques act as a means of enterprise orchestration to enable the many disparate things we have deployed into our enterprise; however, do not themselves address notions of "Cloud Native" deployment and how we can more properly leverage our cloud platforms to enable the enterprise to get the full value out of cloud deployments. 

### Are Current Enterprise Integration Practices “Cloud Native”?

As discussed previously in this document, enterprise integration patterns and traditional integration architectural viewpoints (such as SOA or MSA) are largely complementary to cloud native deployments. In fact these appliances, and architectural techniques display the following set of characteristics: 
  * Event and Complex event driven behaviour 
  * MicroService decomposition fits nicely into traditional SOA concepts 
  * Single Responsibility of services
  * Fault isolation 
  * Domain isolation  
  * Loose coupling between service endpoints 
  * API oriented 
  * Patterns that provide meaningful idioms to connect loosely coupled services (service mediation, message enrichment, transformation) 

Without overemphasizing the need for enterprise integration techniques as a means to support cloud native deployments, it becomes clear that not only do these techniques (and as a result, their complementary appliances) still make sense in a cloud native world, but become neccessary for us to truly meet cloud native characteristics. 

While enterprise integration appliances and techniques find themselves to be complementary to cloud native deployments, these appliances and techniques don't get us all the way there in and of themselves: 
  * Legacy tooling does not exploit platform capabilities 
  * Dependence on other tools to scale to demand
  * Dependence on other tools to scale to zero 
  * No built in notion of location transparency for components that live outside of a runtime 
  * Appliances (message broker or esb) that decouple service endpoints are not cloud native
  * Capabilities largely dependent on underlying platform (i.e. a JVM or VM)

Traditional tooling has often been monolithic, dependent on elaborate configuration, static in nature, and totally reliant on an underlying platform technology (such as a VM) to provision its runtime. This unfortunately, implies that some other tool, product, etc., must come in to bridge that gap. For instance, while historically we might have scripted some ways to deal with scaling up or down, or rolling out change, or gave ourselves other means of high availability like a load balancer, our legacy enterprise integration appliances (message brokers, large ESB's, or even more contemporary integration tiers in Microservice architecture) did not attempt to address these concerns themselves. 

### What is Needed to Consider an Enterprise Integration appliance, or tier Cloud Native?
Revisiting our *cloud native*  characteristics we assert that we require the following for an integration tier to be considered *cloud native*:
* Elasticity
* On Demand Scaling 
* Resilient  
* Manageable, Observable  
* Location agnostic 
* Event Driven 
* API Centric 