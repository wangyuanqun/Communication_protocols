- Read through lecture slides and do the tutorials is enough for the quiz.

Quiz 1: 20 questions in 1 hour. It is mainly on application layer. 

**IP address quiz worth 20% and ask Leo help!**

**Do the labs week by week on hands**

**the 3 quiz and ip address will be multiple choice and ==text== question**

=================================================================================================================================================================================================================================================================================================================



Local area network: in our home network, it is a Ethernet network/ Wi-Fi network in these days.

The purpose of local area network is to allow differnet nodes within a single network to communicate with each other.



**Layer 1(physical)**. The physical layer' job is to represent the 1s and 0s as some kind of physical quantity that can be transmitted. It also interprets the incoming data and then transmit it to layer 2 which is data link. The physical layer specifies standards for how to interpret that information. It defines the size of wire, plugs etc.

For example, Ethernet II which is a layer 1&2 standard for a type of wired network, this defines the characteristics of the physical cables.

**Layer 2(data link)**. And at this layer the chunk of information is called **frame**. The frame' head has destination address(used to decide the recipe ) and source address(copy it to send back information).

==And an extra information, Error correction is used to detect whether the payload and the head have been correctly received. Checksum is designed to allow these errors to be detected.== (Error correction not always done in data link refer module2).

***(these 2 are enough for local area network to let devices communicate with each other, and also they generally come as a pair.)***

**Layer 3(internet)**. routers are network-layer devices(for interconnecting separate physical networks). The IP address is inpected to determine whether an incoming packet is processed locally or forwarded to a different router. We do that by checking the ==routing table==, each row is checked 

1. by doing a **bitwise**
2. between the destination IP address of the incoming packet and the netmask in that row
3. if the result matches the network address in the same row

after that, using the most specific match(the one with longest netmask) to decide how to process the packet.

==routing table==

- network address
- netmask
- egress interface(进出口)
- next-hop IP address

(the last two are null if it is a local address)

**Layer 4(transport)**. The data is called Segment. Some transports do disassembly/reassembly(like TCP), and some (like UDP) do not. A UDP-based application **can** do segmentation/reassembly at the application layer, and the application layer can add its own sequence number for this purpose. But TCP has both sequence number and ACK number.

TCP utilizes a number of flags, or 1-bit boolean fields, in its header to control the state of connection. For example,

- SYN - (Synchronize) initiates a connection
- FIN - (Final) cleanly terminates a connection
- ACK - Acknowledge the received data





What is internet?



what are the main components of internet?



how it works?



the five layers of TCP/IP stack.