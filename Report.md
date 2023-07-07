OSI MODEL
Overview:
The open systems interconnection (OSI) model is a conceptual model created by
the International Organization for Standardization which enables diverse communication systems
to communicate using standard protocols.
Layer 4. The transport layer
The Transport is responsible for transferring data across
a network and provides error-checking mechanisms and data Flow controls It determines how
much data to send, where it gets sent and at what rate. TCP within the TCP/IP suite is the best-
known example of the transport layer. This is where the communications select TCP port
numbers to categorize and organize data transmissions across a network.
CASE STUDY 2 This layer establishes a point-to-point connection between the
source and the destination, ensuring that the data is transmitted in the correct order. It also
performs flow control, error control, data reassembly, and segmentation. Transmission Control
Protocol (TCP) and User Datagram Protocol (UDP) are examples of transport layer protocols.
Attacks in this layer are often conducted through vulnerable open ports identified by port
scanning.
SYN flood attack :
This is a type of DDoS attack that exploits the TCP three-way
handshake. The attacker sends multiple synchronization (SYN) packets to every port of a
server. The server acknowledges by sending a Synchronize-Acknowledge (SYN-ACK)
message for each SYN packet. If the malicious client doesn’t send the final ACK packet as
expected, it creates “half-open” sessions on the server. As the server’s ability to process
requests becomes depleted, new requests and services to legitimate clients will be denied. If
the SYN flood continues, the server will malfunction or crash. SYN flood attacks can be
mitigated by allocating micro-blocks, as few as 16 bytes for a SYN request, and maintaining
SYN cookies and RST cookies.
Working Of SYN flood attack:
SYN flood attacks work by exploiting the handshake process of a TCP connection. Under
normal conditions, TCP connection exhibits three distinct processes in order to make a
connection.
« First, the client sends a SYN packet to the server in order to initiate the connection.
« The server then responds to that initial packet with a SYN/ACK packet, in order to
acknowledge the communication.
« Finally, the client returns an ACK packet to acknowledge the receipt of the packet from the
server. After completing this sequence of packet sending and receiving, the TCP connection
is open and able to send and receive data.
To create denial-of-service, an attacker exploits the fact that after an initial SYN packet has
been received, the server will respond back with one or more SYN/ACK packets and wait for
the final step in the handshake.
Here’s how it works:
« The attacker sends a high volume of SYN packets to the targeted server, often with spoofed
IP addresses.
« The server then responds to each one of the connection requests and leaves an open port
ready to receive the response.
« While the server waits for the final ACK packet, which never arrives, the attacker continues
to send more SYN packets. The arrival of each new SYN packet causes the server to
temporarily maintain a new open port connection for a certain length of time, and once all the
available ports have been utilized the server is unable to function normally.
Smurf attack :
Named after a popular toy figure from the 1980s that appeared to be
everywhere, the Smurf attack is also a type of a DDoS attack. This attack is carried out by
generating fake ICMP Echo request (PING) packets to an IP broadcast network using the
targeted server`s IP address as the source IP address. With so many ICMP responses, seeming
to come from everywhere, the target server becomes overwhelmed and is bought down.
Inspection of incoming, traffic and blocking illegal ICMP responses will limit the chances of
a Smurf attack.
Internet Control Message Protocol (ICMP) is a form of DDoS attack that overloads network
resources by broadcasting ICMP echo requests to devices across the network. Devices that
receive the request respond with echo replies, which creates a botnet situation that generates a
high ICMP traffic rate.
As a result, the server is flooded with data requests and ICMP packets,
which overwhelm the computer network and make it inoperable. This can be particularly
problematic for distributed computing systems, which allow devices to act as computing
environments and enable users to access resources remotely.
A smurf attack works through the following three-step process:
« The DDoS Smurf malware creates a network data packet that attaches to a false IP
address. This is known as spoofing.
« The packet contains an ICMP ping message, which commands network nodes to send a reply.
« This process, known as ICMP echoes, creates an infinite loop that overwhelms a network
with constant requests.
Prevent Smurf Attack:
References:
1. IIT Khargapur
2. Fortinet
3. Tech target
