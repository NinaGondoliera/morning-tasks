# NAT, routes, Internet Gateway
​
Answer the following questions
​
1. What do you think the purpose of an internet gateway is? What would we not be able to do without one?

1.a. Every VPC needs an Internet Gateway. Without the IgW the VPC would not be able to access the wider Internet. IgW allows both incoming and outgoing Internet traffic, but has not physical resource attached to it.
​
2. Thinking back to a previous session, where do you think you might be using a NAT gateway right now?

2.a. In my home setup, the router is acting like the NAT gateway, since all my devices have a private IP address, when they access the Internet they get the public IP addrees of my router. 
​
3. What IP addresses will be matched by the CIDR block of `0.0.0.0/0`?

3.a. That CIDR range would matc every possible IP address, since none of the octets are specified, each of their values can be between 0 and 255. that means addresses between 0.0.0.0 and 255.255.255.255. /0 means no bits are to be matched so totally inclusive of all possible variations. 
   - for bonus points, explain why?
​
4. In your own words, what is the difference between a NAT gateway and an Internet Gateway? When would you want one over the other?

4.a. 
* IgW is a necessary part of VPC, each VPC has one IgW - NAT gateway is a part of an AZ, one NAT Gw per AZ
* IgW allows inboubd and outbound Internet traffic - NAT Gw allows only outgoing traffic when it assigns a public IP to a device from the Private subnet
* IgW needs a route from the NAT Gw created by the Route Table, to properly direct traffic. 

