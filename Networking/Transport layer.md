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

TCP provides reliability and flow control using these basic operations:
- Number and track data segments transmitted to a specific host from a specific application
- Acknowledge received data
- Retransmit any unacknowledged data after a certain amount of time
- Sequence data that might arrive in wrong order
- Send data at an efficient rate that is acceptable by the receiver

  ### TCP header
  - A TCP segment adds 20 bytes (i.e., 160 bits) of overhead when encapsulating the application layer data.
  - The TCP header is a **20-byte header with 10 fields.**
  
  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/1d6d2bcc-d58f-4368-8be3-95302bd4461e)

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
 
  ### Applications which use TCP
  - HTTP
  - FTP
  - SMTP
  - SSH

  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/70c97d1a-2b10-4a33-9da9-f87f67d1a156)


### User Datagram Protocol (UDP)
- UDP is a simpler transport layer protocol than TCP. It does not provide reliability and flow control, which means it requires fewer header fields.
- Because the sender and the receiver UDP processes do not have to manage reliability and flow control, this means UDP datagrams can be processed faster than TCP segments.
- UDP also divides data into datagrams (segments)
- UDP is preferable for applications such as Voice over IP (VoIP) which requires minimal latency.
- UDP is also used by request-and-reply applications where the data is minimal, and retransmission can be done quickly such as DNS.

  UDP has few characteristics which are identical to IP:
- It is connectionless protocol. Because UDP does not provide reliability or flow control, it does not require an established connection.
- It is a best effort delivery protocol. There is no acknowledgment that the data is received at the destination.

  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/af8b26a0-8c94-47a8-9479-18feb0aea58c)
