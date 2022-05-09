# class 16

## **Serverless**

Serverless is a cloud computing execution model that

- Automatically provisions the computing resources required to run application code on demand, or in response to a specific event;
- Automatically scales those resources up or down in response to increased or decreased demand;
- Automatically scales resources to zero when the application stops running.

Serverless computing offloads all management responsibility for backend cloud infrastructure and operations tasks - provisioning, scheduling, scaling, patching and more - to the cloud provider

The term 'serverless' describes the customer's experience with those servers: they are invisible to the customer

Amazon Web Services introduced serverless in 2014 with AWS Lambda; today every leading cloud service provider offers a serverless platform including Microsoft Azure (Azure Functions), Google Cloud (Google Cloud Functions) and IBM Cloud (IBM Cloud Code Engine)

## **Serverless pros and cons**

### PROS

- Serverless enables development teams to focus on writing code, not managing infrastructure
- Serverless customers pay for execution only. The meter starts when the request is made, and ends when execution finishes. In the infrastructure as a service (IaaS) compute model customers pay for the virtual machines (VMs) and other resources required to run applications, from the time they provision those resources until the time the customer explicitly decommissions those resources.
- Serverless is a polyglot environment, enabling developers to code in any language or framework with which they're comfortable.
- Serverless simplifies deployment and, in a larger sense, simplifies [DevOps](https://www.ibm.com/cloud/learn/devops-a-complete-guide) cycles, because developers don't have to describe infrastructure needed integrate, test, deliver and deploy code builds into production.
- For certain workloads, such as ones that require parallel processing, serverless can be both faster and more cost-effective than other forms of compute.
- Serverless application development platforms provide near-total visibility into system and user times, and can aggregate that information systematically.

### CONS

There are certain applications for which serverless is not favorable from a business prospective:

- **Stable or predictable workloads**: Because serverless scales up and down on demand in response to workload, it offers significant cost savings for spiky workloads. **But it does not offer the same savings for workloads characterized by predictable, steady or long-running processes; in these cases a traditional server environment might be simpler and more cost-effective.**
- **Cold starts:** Because serverless architectures forgo long-running processes in favor of scaling up and down to zero, they also sometimes need to start up from zero to serve a new request. For certain applications, this startup latency isn’t noticeable or detrimental to users. **But for others - for example, financial trading application - the delay is unacceptable.**
- **Monitoring and debugging:** These operational tasks are challenging in any distributed system, but a move serverless architecture (or microservices architecture, or a combination of the two) only exacerbates the complexity. For example, **teams may find it difficult or impossible to monitor or debug serverless functions using existing tools or processes.**
- **Vendor lock-in:** Serverless architectures are designed to take advantage of an ecosystem of managed cloud services and, in terms of architectural models, go the furthest to decouple a workload from something more portable, like a [virtual machine (VM)](https://www.ibm.com/cloud/learn/virtual-machines) or [Docker](https://www.ibm.com/cloud/learn/docker) container. For some companies, **deeply integrating with the native managed services of a specific cloud platform is where much of the value of cloud can be found; for others, this cloud lead to material lock-in risks that need to be mitigated.**

All Notes take from:

[https://www.ibm.com/cloud/learn/serverless](https://www.ibm.com/cloud/learn/serverless)