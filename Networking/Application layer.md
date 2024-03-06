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
