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

1. B
2. D
3. C - X
4. B
5. A - X
6. C
7. C
8. B
9. B
10. D ?
11. B
12. D
13. A
14. A
15. D
16. B
17. C
18. A - X
19. A - X
20. B
# Chapter 2
## Google Cloud Compute Services

1. 