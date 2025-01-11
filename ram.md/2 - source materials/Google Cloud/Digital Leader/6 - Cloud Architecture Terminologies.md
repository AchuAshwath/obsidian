02-01-2025 12:05:18

Status : #baby 

Tags : [[Digital Leader]]

All though Google won't ask you terminologies just like that, but they would play into terminologies so it is good to know them.
# Cloud Architecture Terminologies

## **Availability** 
*Highly Availability*
#### Your ability to ensure a service remains available 
by ensuring there is **no single point of failure** and/or ensure certain level of performance.

**Cloud Load Balancing**
A load balancer allow you to evenly distribute traffic to multiple servers in  one or more data center. if a data center or server becomes unavailable(unhealthy) the load balancer will rout the traffic to only available datacenters with servers.

> Running you workload across multiple Zones ensures that if 1 or 2 Zones become unavailable yous service/applications remain available.

![](https://cloud.google.com/static/sql/images/ha-config.png)
## **Scalability** 
#### Your ability to grow rapidly or unimpeded
*High Scalability* - ability to increase your capacity based on the increasing demand of traffic, memory and computing power.

1. Vertical Scaling - increasing size of the single machine like the storage, compute etc.
2. Horizontal Scaling - Adding additional servers of the same size and distributing workload across them.
## **Elasticity** 
#### Your ability to shrink and grow to meet the demand
*High Elasticity* - ability to **automatically** increase or decrease your capacity based on the current demand of traffic, memory and computing power.

> similar to scalability but the key difference is that Elasticity is automated and has the ability to decrease.

1. Horizontal Scaling
	1. Scaling **out** - add more server of the same size.
	2. Scaling **in** - removing more server of the same size.
2. Vertical Scaling is generally hard for traditional architecture we usually see horizontal scaling described with Elasticity.

**Managed instance groups (MIGs)** - Automatically increase or decrease in response to demand or a  defined schedule.
## **Fault Tolerance**
#### Your ability to prevent failure.
*High Fault Tolerant* - ability for your service to ensure there is no single point of failure. Prevent the chance of failure.

> similar to high availability but its focus is to highly preventing the chance of failure.

A common example is having a copy of you database where all ongoing changes are synced. The secondary system is not in-use  until a fail occurs and becomes the primary database.

You can use **Cloud DNS**, which is a DNS service that can detect a failing primary system and fail-over to a stand-by secondary system.

*Fail-over* is when you have a plan to shit traffic to a redundant system in case the primary system fails.
## **Disaster Recovery**
#### Your ability to recover from a failure.
*High Durability* - ability to recover frm a disaster and to prevent the loss of data, Solutions that recover from a disaster ks know as Disaster Recovery (DR)
- do you have backup?
- how fast can you restore that backup?
- does you backup still work?
- how do you ensure current live data is not corrupt?

	## *References*

[About high Availability](https://cloud.google.com/sql/docs/mysql/high-availability)
[Design for Scale and High Availability](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://cloud.google.com/architecture/framework/reliability/design-scale-high-availability&ved=2ahUKEwisraXJ9NaKAxXJRmwGHYHIChQQFnoECBkQAQ&usg=AOvVaw3RhDn2JbSyS2xIU3N_f8-l)
[Instance Groups](https://cloud.google.com/compute/docs/instance-groups)