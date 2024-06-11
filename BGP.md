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
