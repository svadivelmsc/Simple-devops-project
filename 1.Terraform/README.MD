•	The private subnet is inaccessible to the internet (both in and out).
•	The public subnet is accessible; just dependent on the configuration of the security groups. Elastic IPs can be associated with instances in here.
•	Instances in the public subnet can access instances in the private subnet (also dependent on security groups) because they’re in the same VPC (this is enabled by the route tables).
•	Routing is handled like this:
o	Private subnet is routed through the NAT instance.
o	Public subnet is routed directly to the internet gateway.
