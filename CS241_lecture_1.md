# CS241 lecture 1
*2/10/2018*
---
### What is a Computer Network?
> An interconnected collection of two or more autonomous computers.

A network can be implemented as a [client-server model](), a popular example is a webserver, or as a [peer-to-peer model](), a popular example being email.

### Classifying Networks
Common ways to classify networks are by:
1. Transmission Technology
1. Scale

**Transmission Technology**

There are two main classifications of transmission technology.
* broadcast links (generally for localised networks)
 * a single, shared communication channel
 * short messages (packets) are recieved by all but are ignored by everyone except the user to which they are addressed
 * This is [multicasting](https://en.wikipedia.org/wiki/Multicast) by appropriate addressing
* point-to-point links (generally for larger networks)
 * connections between individual machines
 * This is [unicasting](https://en.wikipedia.org/wiki/Unicast)
 * routing algorithms required

**Scale**

There are five main classifications of network scale.
* Personal Area Network (PANs)
  * A network that covers a very small area of under a metre squared
  * an example of this would be a short range wireless network such as blutooth
* Local Area Network (LANs)
  * A network that covers anywhere from a room to a campus
  * An example of this would be wifi
* Metropolitan Area Network (MANs)
  * A network that covers a city
  * An example of this would be a cable tv network
* Wide Area Network (WANs)
  * A network that covers anywhere from a country or a continent
  * This is often done by connecting many LANs to a subnet
