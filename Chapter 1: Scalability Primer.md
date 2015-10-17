# *Scalability Primer*
## *Scalability Defined*
  * scalability of an application is the measure of the number of users it can support at the same time.
  * the point at which an application cannot handle additional uses effectively is the limit of its scalability. Scalability reaches its limit when a critical hardware resources runs out.
  * Vertically scale up:
	- is to increase overall application capacity by increasing the resources within existing nodes
	- limited by the extent to which your software is able to take advantage of the hardware.
	- usually involved downtime
	- is hardware and infrastructure focses
  * Horizontally scale out
	- is to increase overall application capacity by adding nodes
	- tend to me more complex then vertical scaling and has more fundamental influence on application architecture.
	- is software and architecture focused
	- generally have nodes allocated for specific functions. 
	- a nodes is homogeneous when all the nodes supporting a specific function has the same hardware, OS, and software function. 
	- horizontal scaling is more efficient with homogeneous nodes
	- when nodes are homogenous, round-robin load balancing works, capacity planning is easier, and auto scale rules are easier to write
	- within homogenous function group, nodes are operate autnomously, one nodes does not need to know another node of the same type.
	- the best outcome is when each additional nodes add the same incremental usable capacity
  * Describing Scalability
	- useful definition of scalability
	  * Concurrent user : the number of users with activity within a specific time interval 
	  * Response time : the elapse time between a user initiating request and receiving a round-trip response
	  * combining concurrent users and response time to make a more meaningful definition: with 100 concurrent users, under 2 seconds for 60% of the users, 2-5 secs for 38%, >5 sec for 2%
  * Scale Unit
	- the combination of resources that can be added together to support specific application functionality
	- Ex: for every 100 users, we may need 2 webs, 1 app and 100 MB disk space. 

## *Resource Contention Limits Scalability*
	* scalability problem is resource contention problem. The competing demand for critical resources such as CPU, memory, and network bandwidth.
	* resources bottleneck is the condition in which not enough resources to share among concurrent users; the result is users experience slowed down or blocked.
	* Easing Resource Contention
		- don't use them up so fast
		- adding more of them
		- efficiency is often come at a trade-off; compressing data with increase network efficiency but use more CPU and memory
## *Scalability is a Business Concern*
	* 1 second delay in page load will reduce conversion by 7%
	* Comparing performance and scalability
		- performance is what an individual experience
			- the most important performance related metris is response time
		- scalability is how many users get to experience it. The number of users who has a positive experience. If the application sustain consistent performance for individual users as the number of concurrent users grow, that is scaling
## *Cloud-Native Application*
	* Cloud Platform Defined
		- enabled by the illusion of infinite resources and limited by the maximum capacity of individual virtual machine, cloud scaling is horizontal
		- enabled by short-term resource rental model, it can release resources as easily as add resources
		- enabled by pay per used model, application only pay for currently allocated resources and all usage cost are transparent
		- enabled by self-service, on-demand, programmic visioning and releasing resources, cloud scaling is automatable
		- enabled and constrainted by multitenant services running on commodity hardware, cloud application is optimized for cost rather than reliability; failure is routine but downtime is rare
		- enabled by rich ecosystem of managed platform services, cloud application deployment is simplified.
	* Cloud-Native Application Defined
		- Leveraged cloud platform services for reliable, scalable infrastructure
		- uses non-blocking asynchronous communication in a loosely coupled architecture 
		- scales horizontally, adding resources as demand increase, and release as demand decreases
		- cost-optimize to run efficiently, not wasting resources
		- handles scaling events without downtime or user experience degradation
		- handles nodes failure without downtime 
		- uses geographically distribution to minimize netowrk latency
		- upgrades without downtime
		- scales automatically using proactive and reactive actions
		- monitors and manages application logs even as nodes come and go
		- it is the application architecture that makes an application cloud-native, not the choice of platform
		 
		 		
		  