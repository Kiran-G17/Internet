# BGP Routing

##  What is BGP?

### Border Gateway Protocol 

When a user submits data via the Internet, BGP looks at all of the paths that data can travel across and decides which route is the best.
This usually means that the protocol decides to hop between autonomous systems.

This protocol enables data routing. 
> A user in the UK wants to access a website where the servers are in the USA

BGP enables the communication to happen quickly and efficiently.

## Anonymous Systems

The Internet is a network of networks. It is broken up into hundreds of thousands of smaller networks which are known as autonomous systems (ASes). 
These are essentially a large pool of routers run by a single organisation.

If the BGP is considered to be a postal service, autonomous systems are like post office branches, each AS has routers within it. they forwards their outbound transmissions to the AS it is within which then uses BGP routing to get the traffic to its desired destination.

### Routing Choices

![](https://www.cloudflare.com/img/learning/security/glossary/what-is-bgp/bgp-simplified.svg)

In the simplied diagram, a packet is destined for AS3 and is sent from AS1. The protocol has the option of either:

> Hopping to AS2 then hopping to AS3

or

> Hopping to AS6, then to AS5, then to AS4 and finally to AS3

### Which route? Why?

In the simplified model, the most obvious choice for the route for the packet to be sent over is the first as it requires the least hops for the packet to reach AS3 from AS1.

## On the scale of the Internet

The Internet is much, much larger than the one in the diagram and this could mean that there are many more hops that a packet would need to go over to reach it's destination.
It also constantly changes as systems that were previously active, shutdown and cease to respond to requests, while new systems may be introduced. 

Autonomous systems need to be kept up to date on which routes are available and which routes are no longer an option.
This is achieved by ASes connecting to neighboring ASes over a TCP/IP connection to share routing information, allowing each AS to properly route outbound data.

### Routes aren't always the most efficient

The companies and organisations that run ASes may compete with one another, resulting in ASes choosing not to route over the most efficient path, and rather the one that is favoured by a company or organisation. 
A factor that effects this is the costs that some ASes charge other ASes for routing.
BGP routes will try to be efficient but will take into account any business considerations.

### Who operates ASes?

Typically, ASes belong to ISPs or other large organisations such as tech companies, unviersities, governments and scientific instituions.

ASes must have a registered autonomous system number (ASN) which the Internet Assigned Numbers Authority assigns to Regional Internet Registries, which then assigns them to ISPs and networks.

ASNs are 16 bit numbers between 1 and 65534 or 32 bit nubmers between 131072 and 4294967294.
ASNs are only required for use in external BGP.

## External BGP and Internal BGP

External BGP is necessary for routing packets between ASes and so is consider external as it is between networks external to the AS.
Internal BGP isn't necessary for a network to be able to use external BGP as ASes can choose their own protocol for controlling the flow of packets within their network.

External BGP can be considered as international shipping as all countries have a standard way of shipping between each other. However, within the country, the country can choose their own method of routing (internal BGP is an example).

## BGP Attributes

The main goal of BGP is to find the most efficient route for a packet.
