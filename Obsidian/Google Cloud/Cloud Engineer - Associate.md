# Chapter 1
## Overview of GCP

1. Typical services provided by any cloud service.
	1. Compute
	2. Storage
	3. Networking
2. What is a google **Project**?
	1. it is a logical grouping of Google Cloud resources
3. Different Compute resources in Google Cloud
	1. **Virtual Machines (VMs)**
	2. **Managed Kubernetes Clusters**
		1. On managed clusters, applications run inside the containers. 
		2. Health, Networking, Monitoring and Auto-scaling of containers will be taken care by Cluster Management services.
	3. **Serverless Computing**
		1. There are 3 options available
			1. **App Engine** - used for apps and containers that runs for extended period of time
			2. **Cloud Run** 
				1. used for app and containers when full Kubernetes engine is not needed
				2. apps and containers should be stateless
				3. when rapid auto-scaling is needed
			3. **Cloud Functions**
				1. these will be run when you want to respond to an event. like a file upload, message received etc
4. Different Storage options in Google Cloud
	1. Object Store (aka. Google's *Cloud Storage*)
		1. data is stored in the form of *objects* or *blobs*
		2. these objects are *files* and are grouped into *buckets*
	2. File Store (aka. Google's *Cloud Filestore*) 
		1. it is a hierarchical storage system for files
	3. Block Store
		1. uses fixed size data structure called *block* to organize data
	4. Cache
		1. data should be stored in cache to achieve a sub-millisecond latency.
		2. a careful Cache-Invalidation mechanism should be designed to properly use the cache DB.
5. Networking in Google Cloud
	1. Each Google Cloud resource is identified with an IP address
	2. It will have an *Internal IP* and *External IP*
	3. Internal IP is used to access resource with in the GCP network (a VPC)
	4. External IP is used for clients to communicate with the GCP resource.
	5. External IP addresses can be either static or ephemeral
		1. *Static IP* address do not change often
		2. *Ephemeral IP* address change/gets unavailable when the resource shuts down
	6. *Firewall rules* can be applied to IP addresses to make sure only intended clients can access resources with in the VPC.
	7. *Peering* is used to connect resource between your on-prem and VPC in the Google cloud. GCP offers following 6 ways of peering.
		1. VPNs
		2. Interconnects
		3. Shared VPC
		4. VPC Network Peering
		5. Direct Peering
		6. Carrier Peering

### Review
1. Which of the following is an option for choosing a computing resource in Google Cloud?
	- [ ] A.Cache
	- [x] B.Virtual machine (VM)
	- [ ] C.Block
	- [ ] D.Subnet

2. If you use a cluster that is managed by a cloud provider, which of these will be managed for you by the cloud provider?
	- [ ] A.Monitoring
	- [ ] B.Networking
	- [ ] C.Some security management tasks
	- [x] D.All of the above

3. You need serverless computing for file processing and running the back end of a website; which two products can you choose from Google Cloud?
	- [ ] A. Kubernetes Engine and Compute Engine
	- [ ] B. Cloud Run and Cloud Functions (*CORRECT*)
	- [x] C.Cloud Functions and Compute Engine
	- [ ] D.Cloud Functions and Kubernetes Engine

4. You have been asked to design a storage system for a web application that allows users to upload large data files to be analyzed by a data analytics workflow. The files should be stored in a high-­availability storage system. Filesystem functionality is not required. Which storage system in Google Cloud should be used?
	- [ ] A.Block storage
	- [x] B.Object storage
	- [ ] C.Cache
	- [ ] D.Network File System

5. All block storage systems use what block size?
	- [x] A.4 KB.
	- [ ] B.8 KB.
	- [ ] C.16 KB.
	- [ ] D.Block size can vary.  (*CORRECT*)

6. You have been asked to set up network security in a virtual private cloud. Your company wants to have multiple subnetworks and limit traffic between the subnetworks. Which net-work security control would you use to control the flow of traffic between subnets?
	- [ ] A.Identity access management
	- [ ] B.Router
	- [x] C.Firewall
	- [ ] D.IP address table
	
7. When you create a machine learning service to learn how to classify objects using tabular data, what type of servers should you choose to manage compute resources?
	- [ ] A.Virtual machines (VMs).
	- [ ] B.Clusters of VMs.
	- [x] C.No servers; you should use specialized services, which are serverless.
	- [ ] D.VMs running Linux only.
	
8. When does investing in servers for extended periods of time, such as committing to use servers for three to five years, work well?
	- [ ] A.When a company is just starting up
	- [x] B.When a company can accurately predict server need for an extended period of time
	- [ ] C.When a company has a fixed IT budget
	- [ ] D.When a company has a variable IT budget
	
9. Your company is based in North America and will be running a virtual server for batch processing invoices. What factor determines the unit per minute cost?
	- [ ] A.The time of day the virtual machine (VM) is run
	- [x] B.The characteristics of the server
	- [ ] C.The application you run
	- [ ] D.None of the above 
	
10. You plan to use AutoML to analyze sales data and predict product demand in the near future. You plan to analyze between 1,000 and 2,500 products per hour. How many VMs should you allocate to meet peak demand?
	- [ ] A.1.
	- [ ] B.10.
	- [ ] C.25.
	- [x] D.None; AutoML is a serverless service.

11. You have to run a number of services to support an application. Which of the following is a good deployment model?
	- [ ] A.Run on a large, single VM.
	- [x] B.Use containers in a managed cluster.
	- [ ] C.Use two large VMs, making one of them read only.
	- [ ] D.Use a small VM for all services and increase the size of the VM when CPU utilization exceeds 90 percent.
12. You have created a VM. Which of the following system administration operations are you allowed to perform on it?
	- [ ] A.Configure the filesystem.
	- [ ] B.Patch operating system software.
	- [ ] C.Change file and directory permissions.
	- [x] D.All of the above.
13. Cloud Filestore is based on what filesystem technology?
	- [x] A.Network File System (NFS)
	- [ ] B.XFS
	- [ ] C.EXT4
	- [ ] D.ReiserFS
14. When creating resources in Google Cloud, those resources are always part of what?
	- [x] A.Virtual private cloud
	- [ ] B.Subdomain
	- [ ] C.Cluster
	- [ ] D.None of the above
15. You need to store data for an application and are using a cache. How will the cache affect data retrieval?
	- [ ] A.A cache improves the execution of client-­side JavaScript.
	- [ ] B.A cache will continue to store data even if power is lost, improving availability.
	- [x] C.Caches can get out of sync with the system of truth.
	- [ ] D.Using a cache will reduce latency, since retrieving from a cache is faster than retrieving from SSDs or HDDs.  (*CORRECT*)
16. Why can cloud providers offer elastic resource allocation?
	- [ ] A.Cloud providers can take resources from lower-­priority customers and give them to higher-­priority customers.
	- [x] B.Extensive resources and the ability to quickly shift resources between customers enables public cloud providers to offer elastic resource allocation more efficiently than can be done in smaller data centers.
	- [ ] C.They charge more the more resources you use.
	- [ ] D.They don’t.
17. What is not a characteristic of specialized services in Google Cloud?
	- [ ] A.They are serverless; you do not need to configure servers or clusters.
	- [ ] B.They provide a specific function, such as translating text or analyzing images.
	- [x] C.They require monitoring by the user.
	- [ ] D.They provide an API to access the functionality of the service.
18. Your client’s transactions must access a drive attached to a VM that allows for random access to parts of files. What kind of storage does the attached drive provide?
	- [x] A.Object storage
	- [ ] B.Block storage  (*CORRECT*)
	- [ ] C.NoSQL storage
	- [ ] D.SQL storage
19. You are deploying a new relational database to support a web application. Which type of storage system would you use to store data files of the database?
	- [x] A.Object storage
	- [ ] B.Data storage
	- [ ] C.Block storage  (*CORRECT*)
	- [ ] D.Cache
20. A user prefers services that require minimal setup; why would you recommend Cloud Storage, Cloud Run, and Cloud Functions?
	- [ ] A.They are charged only by time.
	- [x] B.They are serverless.
	- [ ] C.They require a user to configure VMs.
	- [ ] D.They can only run applications written in Go.

# Chapter 2
## Google Cloud Compute Services

1. 