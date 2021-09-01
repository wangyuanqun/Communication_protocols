The application Layer



Why do we have layered protocols stack in the first place?(**Exam**)

They are similar to operating systems(unix,linux), operating systems are sitting between applications and hardwares, and they manages resources that are used by muliple programmers running at the same time so that users do not affect others and avoiding the conflicts between resources.

One of benefits of using protocols is **code reuse**. If there existing a Ethernet network, it should not matter whether it is running a browser or an email account. Even we have two seperate transport layers and many different application layer protocols, they can share the same IP address, because TCP/UDP are above internet layer. And also devices like computers can have multiple network interfaces.

when lower layers changes, upper layers are not affected usually.



Autonomous system is like a large entity(county). 

Autonomoue system is a collection of local area networks joined by a backbone. Automous system is a single network in an administrative sense, as it is managed by a single management entity. Such as UTS, it has a unique AS number to identify. One autonomous system has one or more well-defined interfaces to other systems, such as Telestra(also an automous system).



Routing is a process about making decisions on how to afford a message.

Flow control is about the maximum amount data that can be sent to receiver.

Congession control is about reduce the rate of transmission to the point that stops overflowigng the buffers in the network.

*TCP has both above control built in. UDP does not have both.*

==**tx** is short for transmission==. 



Error correction is not always in layer 2 data link, but also in layer 4(transport) why? (**Exam**) 

If transport layer does error correction, what is the point of doing it at layer 2?(**Exam**)

It is about time. 

Firstly, if the error happens at physical layer



Why error correction is on both data link layer and transport layer?(**Exam**)

On the sending side of transport layer, segments are separate into packets and the receiving side of transport layer reassemble them, but some frames may be discarded on some data link layer, and some protocols, for example ethernet, do not do the retransmissions, just discard the damaged frames. So some packets may be lost and discarded when travelling through routers, and transport layer has the obligation to check errors and ask for retransmissions.
