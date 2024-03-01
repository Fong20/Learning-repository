# # Transport Layer
Transport layer protocols specify how to transfer messages between hosts, and are responsible for managing reliability requirements of a conversation. 


## Responsibilities of transport layer
- Tracking Individual Conversations
- Segmenting Data and Reassembling Segments. The transport layer divides the data into smaller blocks (i.e., segments or datagrams) that are easier to manage and transport.
- Add Header Information. The transport layer protocol also adds header information containing binary data organized into several fields to each block of data.
- Identifying the applications. To pass data streams to the proper applications, the transport layer identifies the target application using an identifier called a port number. 
- Conversation Multiplexing. Sending some types of data (e.g., a streaming video) across a network, as one complete communication stream, can consume all the available bandwidth. This would prevent other communication conversations from occurring at the same time. The transport layer uses segmentation and multiplexing to enable different communication conversations to be interleaved on the same network.

## Types of transport layer protocol

The transport layer includes two protocols:
- Transmission Control Protocol (TCP)
- User Datagram Protocol (UDP)

![image](https://github.com/Fong20/Learning-repository/assets/150316121/e68ed714-2159-4b41-98db-fa81aa0d7504)

### Transmission Control Protocol (TCP)
- Unlike IP which only focuses on structuring, addressing and routing packets from source to destination, TCP is considered a reliable, full-featured transport layer protocol, which ensures that all of the data arrives at the destination. TCP includes fields which ensure the delivery of the application data. These fields require additional processing by the sending and receiving hosts. 
- TCP divides data into segments
- TCP is used in applications where it is important that all the data arrives and that it can be processed in its proper sequence such as databases, web browsers, and email clients. Any missing data could corrupt a communication, making it either incomplete or unreadable.
- **netstat** command is used to check TCP connections which are open and running on a networked host.

TCP provides reliability and flow control using these basic operations:
- Number and track data segments transmitted to a specific host from a specific application
- Acknowledge received data
- Retransmit any unacknowledged data after a certain amount of time
- Sequence data that might arrive in wrong order
- Send data at an efficient rate that is acceptable by the receiver

  ### TCP header
  - A TCP segment adds 20 bytes (i.e., 160 bits) of overhead when encapsulating the application layer data.
  - The TCP header is a **20-byte header with 10 fields.**
  
 **10 fields of the TCP header:**
 - source port
 - destination port
 - sequence number
 - acknowledgement number
 - header length
 - reserved
 - control bits
 - window size
 - checksum
 - urgent

  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/1d6d2bcc-d58f-4368-8be3-95302bd4461e)
  
  ### Applications which use TCP
  - HTTP
  - FTP
  - SMTP
  - SSH

  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/70c97d1a-2b10-4a33-9da9-f87f67d1a156)

### TCP communication process


### User Datagram Protocol (UDP)
- UDP is a simpler transport layer protocol than TCP. It does not provide reliability and flow control, which means it requires fewer header fields.
- Because the sender and the receiver UDP processes do not have to manage reliability and flow control, this means UDP datagrams can be processed faster than TCP segments.
- UDP also divides data into datagrams (segments)
- UDP is preferable for applications such as Voice over IP (VoIP), live video which requires minimal latency.  Live video and voice applications can tolerate some data loss with minimal or no noticeable effect, and are perfectly suited to UDP.
- UDP is also used by request-and-reply applications where the data is minimal, and retransmission can be done quickly such as DNS.
- UDP is also used in applications which are able to handle reliability themselves such as SNMP and TFTP.

  UDP has few characteristics which are identical to IP:
- It is connectionless protocol (stateless protocol). Because UDP does not provide reliability or flow control, it does not require an established connection.
- It is a best effort delivery protocol. There is no acknowledgment that the data is received at the destination.

  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/af8b26a0-8c94-47a8-9479-18feb0aea58c)

  ### UDP Header
  UDP header has only has **four fields and requires 8 bytes (i.e., 64 bits).**
  
  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/fb6702fc-ea2f-4b17-a1d2-99a3a360b958)
  
  **8 fields of UDP header**
  - source port
  - destinaation port
  - length
  - checksum

  ### Applications that use UDP
  - DHCP
  - DNS
  - SNMP
  - TFTP
  - VoIP
  - Video conferencing

Although DNS and SNMP use UDP by default, both can also use TCP. DNS will use TCP if the DNS request or DNS response is more than 512 bytes, such as when a DNS response includes many name resolutions.

  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/f5f92398-f600-4062-a95e-26b36d9fccdc)

## Port numbers
- As seen above, the TCP and UDP transport layer protocols use port numbers to manage multiple, simultaneous conversations.
- The source port number is associated with the originating application on the local host whereas the destination port number is associated with the destination application on the remote host.
- Each request generated by a host will use a different dynamically created source port number. This process allows multiple conversations to occur simultaneously.
- The destination port number is what identifies the type of service being requested of the destination web server.
- In otherwards, a host is able to perform multiple separate communications simultaneously using different port numbers.

### Port number groups
The 16 bits port numbers are assigned by the Internet Assigned Numbers Authority (IANA). The IANA has divided the range of numbers into the following three port groups.

![image](https://github.com/Fong20/Learning-repository/assets/150316121/167d879a-0cde-4050-9f45-79a743f3a8a6)

### Common port numbers and their applications

![image](https://github.com/Fong20/Learning-repository/assets/150316121/2028c77a-142a-4130-9421-b642c4f0c041)


## Socket and socket pairs
- A socket is known as the **combination of source IP address and the source port number** or **destination IP address and destination port number.**
- Sockets enable** multiple processes, running on a client, to distinguish themselves from each other**, and **multiple connections to a server process to be distinguished from each other.**
- A socket pair is the combination of source socket and destination socket.

Eg: 
- The client socket is 192.168.1.5:1099
- the socket on the web server is 192.168.1.7:80
- The socket pair is 192.168.1.5:1099, 192.168.1.7:80
  
![image](https://github.com/Fong20/Learning-repository/assets/150316121/16b416f9-f3d1-4e2f-8e64-01db89fdc6e8)


