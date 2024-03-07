# Application layer

Web client software is used to access the web server
Email client software is used to access the email server
File client software is used to access the file server.

## Uniform Resource Identifier (URI)
A URI is a string of characters that identifies a specific network resource.

### Types URI Specializations:
- Uniform Resource Name (URN). This **identifies only the namespace of the resource** (web page, document, image, etc.) without reference to the protocol.
- Uniform Resource Locator (URL). This defines the **network location of a specific resource on the network.** HTTP or HTTPS URLs are typically used with web browsers. Other protocols such as FTP, SFTP, SSH, and others can be used as a URL. A URL using SFTP might look like: sftp://sftp.example.com.

- Components of a URI
- - Protocol
  - Hostname
  - Path and file name
  - Fragment

  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/892df7cb-31fe-4aa2-acbb-41d4f74c4ab1)

## Application layer protocols
![image](https://github.com/Fong20/Learning-repository/assets/150316121/f242962c-a44c-4acf-944d-4d6bd120e75d)

### Hypertext Transfer Protocol (HTTP)
Hypertext transfer protocol is a type of application layer protocol that is used for web services. It handles the how data is transferred between the web client and the web server.

### How it works?
- When a web client receives the IP address of a web server, the client browser uses that IP address and port 80 to request web services. This request is sent to the server using the Hypertext Transfer Protocol (HTTP).
- When the server receives a port 80 request, the server responds to the client request and sends the information of the web page to the client in the form of specialized 'mark-up' languages known as the HyperText Markup Language (HTML). The HTML coding tells the browser how to format the web page and what graphics and fonts to use.
- The browser then interprets the HTML code and displays the appropriate webpage.

### File Transfer Protocol (FTP)
The File Transfer Protocol (FTP) provides an easy method to transfer files from one computer to another. A host running FTP client software can access an FTP server to perform various file management functions including file uploads and downloads.

### Telnet
- Telnet was developed for people to remotely access the servers. This is done by using a software which creates a virtual device that provides same command line interface functionality of the server.
- Telnet servers listen for client requests on TCP port 23.
- Aconnection using Telnet is called a virtual terminal (vty) session

### Security issues with Telnet
- After a Telnet connection is established, users can perform any authorized function on the server, just as if they were using a command line session on the server itself. They can start and stop processes, configure the device, and even shut down the system.
- Although the Telnet protocol can require a user to login, it does not support transporting encrypted data. All data exchanged during Telnet sessions is transported as plaintext across the network. This means that the data can be easily intercepted and understood.
- Thus, SSH protocol is used instead which provides the same functionality as Telnet but with stronger authentication and encryption of transporting data.

## DNS
- In data networks, devices are labeled with numeric IP addresses to send and receive data over networks. Domain names were created to convert the numeric address into a simple, recognizable name.
- DNS basically acts like the phonebook for the Internet so DNS translates names to numbers. The numbers can be either IPv4 or IPv6.
- The domain name remains the same although the ip address changes which makes it convenient for the user to locate the required website.

### DNS Message Format
The DNS server stores different types of resource records that are used to resolve names. These records contain the name, address, and type of record.

- A = An end device IPv4 address
- NS = An authoritative name server
- AAAA = An end device IPv6 address (pronounced quad-A)
- MX = A mail exchange record

### DNS hierachy
- The DNS protocol uses a hierarchical system to create a database to provide name resolution, as shown in the figure. DNS uses domain names to form the hierarchy.
- The naming structure is broken down into small, manageable zones. Each DNS server maintains a specific database file and is only responsible for managing name-to-IP mappings for that small portion of the entire DNS structure.
- When a DNS server receives a request for a name translation that is not within its DNS zone, the DNS server forwards the request to another DNS server within the proper zone for translation. 

### nslookup command
the nslookup command is issued, the default DNS server configured for your host is displayed. The name of a host or domain can be entered at the nslookup prompt.

### Servers used to find the ip address of the domain name 
- local dns server
- root name server
- top-level domain servers (TLD) = follows the last . of the domain name
  .com - a business or industry
  .org - a non-profit organization
  .au - Australia
  .co - Colombia
authoritative name server = contains all the ip address for the websites ending with a specific domain name (.com, .net etc) It is managed by the domain owner or third parties.

### How it works
- Generally, the ip address of the website is stored in th DNS cache. 
- When the device does not have the ip address of the website in its dns cache, it will send a query to the local dns and the local dns will search for the ip address in its dns cache address as well. If the ip address is found, it will send back a response to the client. Otherwise, it will send a request to the root name server.
- The root name servers will then refer to the top-level domain server based on the domain name.
- The root name server will then send the ip address of the specific top-level domain server to the local dns server.
- The local DNS server will now ask the top-level domain server for the ip address of the authoritative name server which holds the domain name the client is looking for.
- The authoritative name server will then provide the local dns with the require IP address of the website.
- The local dns stores the information in its dns cache and will send back the ip address of the website to the client and the client will store the information in its dns cache.
- Packets can now be sent to the required destination as we now have the required destination ip address.

## DHCP
- The **Dynamic Host Configuration Protocol (DHCP)** for IPv4 service automates the assignment of IPv4 addresses, subnet masks, gateways, and other IPv4 networking parameters. This is also known as dynamic addressing.
- It is uusally the preferred choice on larger networks, or where the user population changes frequently. New users may arrive and need connections; others may have new computers that must be connected. Rather than use static addressing for each connection, it is more efficient to have IPv4 addresses assigned automatically using DHCP.
- Various types of devices can be DHCP servers. The DHCP server in most medium-to-large networks is usually a local, dedicated PC-based server. With home networks, the DHCP server is usually located on the local router that connects the home network to the ISP.
- DHCP is also used for IPv6. It is known as DHCPv6 and it provides services for IPv6 clients. One important difference is that DHCPv6 does not provide a default gateway address. This can only be obtained dynamically from the Router Advertisement message of the router.

  ![image](https://github.com/Fong20/Learning-repository/assets/150316121/ca5e1bea-2e25-450c-9827-4fbac0bf6f76)


### DHCP lease period
- DHCP addresses are not permanent. It can allocate IP addresses for a configurable period of time, called a lease period.
- The lease period is an important DHCP setting, When the lease period expires or the DHCP server gets a DHCPRELEASE message the address is returned to the DHCP pool for reuse.
- Thus, Users can freely move from location to location and easily re-establish network connections through DHCP.

### How it works
- Device requests for an IP address through DHCP settings and it will send an ethernet broadcast (DHCPDISCOVER) to the DHCP server. In the case of a home network, the router is the DHCP server.
- The router will provide a reply (DHCPOFFER) by assigning an appropriate IP address, subnet mask, default gateway and DNS server information based on its pool.
- The client may receive multiple DHCPOFFER messages if there is more than one DHCP server on the local network. Therefore, it must choose between them, and sends a DHCP request (DHCPREQUEST) message that identifies the explicit server and lease offer that the client is accepting.
- Assuming that the IPv4 address requested by the client, or offered by the server, is still available, the server returns a DHCP acknowledgment (DHCPACK) message that acknowledges to the client that the lease has been finalized.
- If the offer is no longer valid, then the selected server responds wi

### Email protocols

### Simple Mail Transfer Protocol (SMTP)
- SMTP is used by an email client to send messages to its local email server. The local server then decides if the message is destined for a local mailbox or if the message is addressed to a mailbox on another server.
- If the server has to send the message to a different server, SMTP is used between those two servers as well.
- SMTP requests are sent to TCP port 25.

### Post Office Protocol (POP3)
- Post Office Protocol is used in a server that supports POP clients. It receives and stores messages addressed to its users. When the client connects to the email server, the messages are downloaded to the client.
- By default, messages are not kept on the server after they have been accessed by the client.
- Clients contact POP3 Servers on port 110.

### Internet Message Access Protocol (IMAP)
- A server that supports IMAP clients also receives and stores messages addressed to its users.
- However, unlike POP, IMAP keeps the messages in the mailboxes on the server, unless they are deleted by the user.
- The most current version of IMAP is IMAP4 which listens for client requests on port 143.
