#### **OFFENSIVE**

**Gobuster** : Gobuster is a tool used to discover hidden directories, files, or subdomains on a website by brute-forcing URL paths or DNS entries using a word-list.
- **HTTP Status Codes (MDN Web Docs)**
- **Reconnaissance (Recon)**
Recon is the ==first phase== of ethical hacking, focused on gathering as much information about the target as possible.

#### **DEFENSIVE**

**To exploit**: To take advantage of a vulnerability in a system to perform unauthorized actions.

1. Preventing intrusions from occurring
2. Detecting intrusions when they occur and responding properly

***WHAT THEY DO :*** 
-  **User cyber security awareness**: Training users about cyber security helps protect against attacks targeting their systems.
-  **Documenting and managing assets**: We need to know the systems and devices we must manage and protect adequately.
-  **Updating and patching systems**: Ensuring that computers, servers, and network devices are correctly updated and patched against any known vulnerability.
-  **Setting up preventative security devices**: Firewall and intrusion prevention systems (IPS) are critical components of preventative security. Firewalls control what network traffic can go inside and what can leave the system or network. IPS blocks any network traffic that matches present rules and attack signatures.
-  **Setting up logging and monitoring devices**: Proper network logging and monitoring are essential for detecting malicious activities and intrusions. If a new unauthorized device appears on our network, we should be able to detect it.

***A SECURITY OPERATIONS CENTER (SOC)*** is a team of cyber security professionals that monitors the network and its systems to detect malicious cyber security events. **Vulnerabilities - Policy Violations - Unauthorized Activity - Network Intrusions**

***Threat Intelligence***

Digital Forensics and Incident Response (==DFIR==)
Digital Forensics > File System - System memory - System logs - Network logs

Incident Response > Preparation - Detection and Analysis - Containment, Eradication, and Recovery - Post-Incident Activity

Malware Analysis > Virus - Trojan Horse - Ransomware > Static Analysis - Dynamic Analysis

Security Information and Event Management (==SIEM==)

IP Scanners! (AbuseIPDB, Cisco Talos Intelligence)

***Networking*** : It is the practice of connecting computers and other devices together to share data and resources.

**The Internet** is a global network of networks that allows computers and devices around the world to communicate and share data.

The ARPANET project in the late 1960s - Tim Berners-Lee / The creation of the World Wide Web 1989

An ***IP address*** (Internet Protocol address) is a unique number assigned to every device connected to a network. It allows devices to identify and communicate with each other.
**Private IP** Used within local networks (e.g. 192.168.x.x, 10.x.x.x). Not accessible from the internet.
**Public IP**	Used on the internet. Assigned by the ISP to identify the network externally.
Public IPv4: 86.157.52.21  
Public IPv6: 2a00:22c4:a531:c500:425f:cce6:c36b:f64d

**MAC (Media Access Control)** address is a 12-digit hexadecimal number assigned to each network interface card.
Format: aa:bb:cc:dd:ee:ff
First 6 digits = manufacturer (e.g., Intel)
Last 6 digits = unique to the device

**MAC Spoofing** 
- Faking a device’s MAC address to pretend to be another device.  
- Used to bypass MAC filters (e.g., in firewalls, cafes, captive portals).
- ip a
- ipconfig /all
Ping - ICMP (Internet Control Message Protocol) : ICMP is a protocol used to send control and error messages in a network.
  
#### **Local Area Network (LAN)**
**Star Topology** : All devices (computers, phones, etc.) are individually connected to a central networking device — usually a switch or hub.
All communication between devices goes through this central device.
**Bus Topology** : This type of connection relies upon a single connection which is known as a backbone cable.
**The Ring Topology** (also known as token topology) : Devices such as computers are connected directly to each other to form a loop.

**Switches** are dedicated devices within a network that are designed to aggregate multiple other devices such as computers, printers, or any other networking-capable device using ethernet.

**Router** : It's a router's job to connect networks and pass data between them.

**Subnetting** means splitting a large network into smaller sections (called subnets).
- What is a Subnet Mask? It shows which part of the IP address is for the network and which is for devices (hosts).
Examples: /24 = 255.255.255.0 = allows 254 usable devices - /16 = 255.255.0.0 = allows 65,534 usable devices

**Network Address**
     Identifies the whole network
     Cannot be assigned to a device
     Like the apartment building’s address
     Example: 192.168.1.0
**Host Address**
     Assigned to a specific device (computer, phone, etc.)
     Like a flat number in the building
     Examples: 192.168.1.10, 192.168.1.42, 192.168.1.100
**Default Gateway (ip route)**
     Used to exit the network (to access the internet)
     Like the main door of the building
     Often: 192.168.1.1 or 192.168.1.254

**ARP (Address Resolution Protocol)** is used to map an IP address to a MAC address in a local network. (arp -a) It helps devices find out "Who has this IP address?" and get the corresponding MAC address.
- ARP Request > ARP Reply > Caching
DHCP – Dynamic Host Configuration Protocol - DHCP Discover > DHCP Offer > DHCP Request > DHCP ACK
- DNS – Domain Name System - DNS translates domain names into IP addresses.

==Ethernet== is a networking technology used to connect devices in a local area network.
It typically uses cables (like RJ-45) to allow data to be transferred between devices.

The ***OSI*** model (or ***Open Systems Interconnection Model***) provides a framework dictating how all networked devices will send, receive and interpret data. This process is called ==encapsulation==.

1. **Physical** : Devices use electrical signals or radio waves to transfer data between each other in a binary numbering system (1's and 0's).
  
2. **Data Link** : The data link layer focuses on the physical addressing of the transmission. It receives a packet from the network layer (including the IP address for the remote computer) and adds in the physical MAC (Media Access Control) address of the receiving endpoint.
- Inside every network-enabled computer is a Network Interface Card (NIC) which comes with a unique MAC address to identify it. 
- It’s also the job of the data link layer to present the data in a format suitable for transmission.
  
3. **Network** : The Network Layer is responsible for routing and delivering data across different networks. It determines the most efficient path for data to travel using IP addresses. It works with protocols like OSPF and RIP.
==OSPF== (Open Shortest Path First) and ==RIP== (Routing Information Protocol). Devices like routers operate at this layer. (Also called Layer 3 devices)
  
4. **Transport** : The Transport Layer is responsible for reliable or fast delivery of data across a network. The Transport Layer is responsible for breaking data into segments, delivering it across networks, and reassembling it on the other side. It handles reliability, order, and speed of communication between devices.
  - ==TCP== – ==Transmission Control Protocol==: Connection-oriented.
    Ensures data is delivered completely, in order, and without errors. Uses acknowledgements (ACKs) and re-transmission if data is lost. Slower but highly reliable.
    Used in: Web traffic (HTTP/HTTPS), Email, File Transfers
  - ==UDP== – ==User Datagram Protocol==: Connectionless. Sends data without ensuring delivery or order. Very fast but not reliable.
  Used in: Video/audio streaming, online games, DNS queries
  - ==QUIC== – Quick UDP Internet Connections: Developed by Google. Combines UDP's speed with TCP-like reliability.
Built-in encryption and connection management. Basis of HTTP/3.
Used in Chrome, YouTube, Google services.
  
5. **Session** : Manages creation, maintenance, and termination of communication sessions between devices.
A session is a temporary connection between two systems for data exchange.
Responsible for starting, controlling, and ending communication.
Can include checkpoints: if data is lost, only the latest parts are resent instead of restarting everything.
Ensures unique sessions – data sent in one session can’t “leak” into another.
  
6. **Presentation** : Acts as a translator or converter for the data.
Ensures that data sent by one device can be understood by another, even if they use different formats. Standardizes data formats between different systems.
Responsible for data encryption, compression, and formatting.
Helps translate between application formats like text, images, videos, etc.
  
7. **Application** : The Application Layer is the topmost layer of the OSI model.
It’s the layer that users interact with directly through software such as browsers, email clients, or FTP programs.
It defines the protocols and rules that applications use to communicate over a network.
When you type a website URL into your browser, the HTTP protocol (Application Layer) manages that request.

##### ***What are Packets and Frames?***
- Packets and frames are small pieces of data that, when forming together, make a larger piece of information or message.
- However, they are two different things in the OSI model. A frame is at layer 2 - the data link layer, meaning there is no such information as IP addresses. Think of this as putting an envelope within an envelope and sending it away. The first envelope will be the packet that you mail, but once it is opened, the envelope within still exists and contains data (this is a frame). (IP - Yes/No)
  **Header**	     -                **Description**
==Time to Live==    -     This field sets an expiry timer for the packet to not clog up your network if it never manages to reach a host or escape!
==Checksum==     -      This field provides integrity checking for protocols such as TCP/IP. If any data is changed, this value will be different from what was expected and therefore corrupt.
==Source Address==	    -     The IP address of the device that the packet is being sent from so that data knows where to return to.
==Destination Address==     -     The device's IP address the packet is being sent to so that data knows where to travel next.

***TCP (Transmission Control Protocol)*** is a connection-oriented protocol used in networking. It ensures reliable and ordered delivery of data between devices. TCP/IP is a simplified model similar to the OSI model. It has four layers:
    Application
    Transport
    Internet
    Network Interface

**Key Features**:
    TCP uses a Three-Way Handshake to establish a connection before sending data.
    Each data packet includes a header with important control information.
    The process of adding headers is called encapsulation; removing them is decapsulation.
**TCP Header Fields**:
    Source Port / Destination Port – Sender and receiver port numbers
    Source IP / Destination IP – Sender and receiver IP addresses
    Sequence Number – Keeps track of the order of data
    Acknowledgement Number – Confirms receipt of data
    Checksum – Verifies data integrity
    Data – The actual payload being sent
    Flags – Controls how the connection is managed (e.g., SYN, ACK, FIN)
**Three-Way Handshake Steps**:
    SYN – Client sends a connection request
    SYN/ACK – Server acknowledges and agrees
    ACK – Client confirms and connection is established
- After that, data (e.g., file contents) can be transferred.
Connection Termination:
    The connection is closed cleanly using FIN → ACK exchange from both sides.
    If an error occurs, RST is used to abruptly terminate the session.

***UDP is a stateless transport protocol.***
It allows data to be sent between two devices without establishing a connection or synchronizing them.  
- UDP is used when:
    Speed is more important than reliability
    Some data loss is acceptable (e.g., live streams, VoIP)
  **Advantages**:
    Faster than TCP
    No connection setup required
    Lower overhead (fewer headers)
    Leaves timing control to the application layer
  **Disadvantages**:
    No delivery guarantee
    No error checking or re-transmission
    Bad on unstable connections
    Packets may arrive out of order or be dropped
  **UDP Packet Headers**:
    TTL: Prevents packets from looping forever
    Source & Destination Address – IP info
    Source & Destination Port – Port numbers
    Data: Payload of the packet
  **Key Concept:**
    Unlike TCP, UDP does not use a handshake or acknowledgements.
    It simply sends data – whether it arrives or not, it doesn't care.

##### ***Ports 101 – Understanding Port Numbers***
Ports are numerical identifiers used to direct traffic to the correct application on a device.
- Think of ports like harbor docking points: ships (data) can only dock where the port fits their purpose.
- Each port is a number between 0 and 65535. Ports allow operating systems to keep track of which data belongs to which application.
Why Are They Important?
    Applications use specific port numbers to communicate.
    Without consistent port assignments, data confusion and failure can happen.
    For example, web browsers use port 80 by default for HTTP.

- Common Port Numbers and Protocols: (https://www.vmaxx.net/techinfo/ports.htm)
**Protocol**	                 ==Port==	                       **Use**
FTP (File Transfer Protocol)	==21==	File transfers from a central server
SSH (Secure Shell)	==22==	Secure command-line access to remote systems
HTTP (HyperText Transfer Protocol)	==80==	Unsecured web traffic
HTTPS (Secure HTTP)	==443==	Encrypted web traffic
SMB (Server Message Block)	==445==	File and printer sharing across a network
RDP (Remote Desktop Protocol)	==3389==	Remote desktop access with GUI
- Ports 0–1023 are known as common ports or well-known ports.
- Services can use non-standard ports (e.g., HTTP on port 8080), but must be specified like http://example.com:8080.

    **IP + Port = full address for a specific task on a specific machine.**
Example:
    142.250.185.14:80 → Connects to Google’s web server (HTTP)
    142.250.185.14:22 → Connects to Google’s SSH service (if allowed)
Summary:
    Ports are like the service-specific addresses attached to an IP.
    Without knowing the correct port, the device won’t know which application should handle your request.

***Port forwarding*** is a router configuration that allows external devices (from the internet) to access services hosted inside a private network. It is set up inside the router/modem settings.
The router listens on a public IP and a specific port (e.g., 82.62.51.70:80) and forwards the request to a local IP and port (e.g., 192.168.1.10:80).
Example:
    Public IP: 82.62.51.70
    Local Server IP: 192.168.1.10
    Service Port: 80 (HTTP)
 Incoming request to 82.62.51.70:80 is forwarded to 192.168.1.10:80 inside the network.

Why use Port Forwarding?
    To host a website/server/game from home
    To allow access to SSH, HTTP, FTP etc. remotely
    To make a local service publicly accessible
Things to remember:
    The local device should have a static IP
    The port must be open and listening
    Firewalls must allow the connection
Summary:
    Port Forwarding = Public IP + Port → Forward → Private IP + Port

***A firewall*** is a device or software in a network that permits or denies traffic based on set rules. Think of it as a security guard deciding who gets in and who doesn't.
Factors firewalls consider:
    Where the traffic is coming from (source IP or network)
    Where the traffic is going to (destination IP or network)
    What port is used (e.g. port 80 = web traffic)
    What protocol is used (TCP, UDP, etc.)
They inspect packets and decide to allow or block based on these.

Two Main Types of Firewalls:
**Type**	           **Description**
==Stateful==	       Tracks the entire connection, not just one packet. Smart, dynamic, and uses more resources. Blocks full sessions if needed.
==Stateless==	   Checks each packet individually. Uses fewer resources but is simpler. Good for handling large attacks (like ==DDoS==).

##### ***VPN (Virtual Private Network):***
A VPN creates a secure "tunnel" over the internet, allowing devices in different physical locations to act like they're on the same private network.
Main Benefits:
- Connects networks across locations
- Encrypts traffic (offers privacy)
- Hides your identity (offers anonymity)
VPN Protocols:
- PPP: Provides authentication & encryption, cannot leave network alone.
- PPTP: Sends PPP data over internet, easy but weak.
- IPSec: Strong encryption using IP framework, harder to configure.

**Router**
    A router connects different networks and decides the best path for data to travel.
    Operates at Layer 3 (Network layer) of the OSI model.
  Factors routers consider:
        Which path is shortest?
        Which is most reliable?
        Which uses faster medium (e.g. fiber)?
        Verb: A router routes data.
**Switch**
    A switch connects multiple devices within the same network.
    Forwards data based on MAC addresses.
    Works mainly at Layer 2, but some advanced switches can also work at Layer 3.
Two types of switches:
    Layer 2 Switch (uses MAC)
    Layer 3 Switch (uses IP + MAC, does routing too)
**VLAN (Virtual LAN)**
    A VLAN separates devices logically, even if they're physically on the same switch.
    Example: Sales department and Accounting department can’t talk to each other, even if they're on the same physical switch.
    VLANs increase security and traffic organization.


***DNS (Domain Name System)*** provides a simple way for us to communicate with devices on the internet without remembering complex numbers. 

**Domain Hierarchy (DNS Structure)**
Root Domain
Represented as a dot . (invisible in browsers)
The top of the DNS hierarchy
Example: tryhackme.com is technically tryhackme.com.

**Top-Level Domain (TLD)**
The rightmost part of a domain name
Examples: .com, .org, .edu, .gov, .mil, .uk
TLD Types:
gTLD (Generic): .com, .org, .edu, etc.
ccTLD (Country Code): .uk, .de, .tr, etc.
There are over 2000 TLDs today, including .tech, .club, .shop, etc.

**Second-Level Domain**
Comes before the TLD
Example: tryhackme.com → "tryhackme" is the second-level domain
Restrictions:
Up to 63 characters
Only a–z, 0–9, and hyphens (-)
Cannot start/end with a hyphen or have double hyphens

**Subdomain**
Comes before the second-level domain, separated by a dot
Example: admin.tryhackme.com → subdomain = admin
Facts:
Same character rules as 2nd level
Up to 253 characters
You can have multiple levels (e.g., jupiter.servers.tryhackme.com)
No limit to how many subdomains you create

***DNS Record Types***
==A Record==
Resolves a domain name to an IPv4 address.
Example: 104.26.10.229
Most common record type for basic website access.

==AAAA Record==
Resolves to an IPv6 address.
Example: 2606:4700:20::681a:be5
“Four A’s” → For longer IPs.

==CNAME Record (Canonical Name)==
Points one domain to another domain.
Example:
store.tryhackme.com → CNAME → shops.shopify.com
Useful for aliasing subdomains to services.

==MX Record (Mail Exchange)==
Specifies mail servers for the domain.
Comes with a priority flag to set backup servers.
Example:
tryhackme.com → alt1.aspmx.l.google.com

==TXT Record==
Holds free text-based data.
Uses:
Email security (SPF, DKIM)
Domain ownership verification
Third-party service authentication

***DNS Request Process***
What happens when you type a domain name into your browser? This is the DNS resolution journey!

1. **Local Cache Check**
Your computer first checks its local cache to see if the domain has been resolved before.
If yes → use it.
If no → move to Recursive DNS Server.

2. **Recursive DNS Server**
Usually provided by your ISP or can be custom (e.g. Google DNS 8.8.8.8).
It checks its own cache.
If cached → returns IP address
If not → starts querying the internet starting with Root DNS Server

3. **Root DNS Server**
Acts as the backbone of DNS.
It identifies the correct TLD server based on the domain suffix (e.g. .com, .org, .uk), and refers the query there.

4. **TLD (Top-Level Domain) Server**
This server holds records pointing to the Authoritative DNS Server for that domain.
Example: For tryhackme.com, it may return kip.ns.cloudflare.com as the authoritative name server.

5. **Authoritative DNS Server**
This is the final stop. It stores the actual DNS records (A, CNAME, MX, etc.) for the domain.
It responds with the final answer, which is sent back to:
Recursive DNS Server
Your system
Your browser

- **TTL (Time To Live)**
Every DNS response includes a TTL.
It tells how long the response can be cached before a new lookup is required.
Caching saves time and reduces DNS traffic.

- **HTTP (HyperText Transfer Protocol)**
HTTP is the set of rules used to communicate with web servers.
It is how web-page data (HTML, images, videos, etc.) is sent and received between your browser and a website.
Developed by Tim Berners-Lee between 1989–1991.

- **HTTPS (HyperText Transfer Protocol Secure)**
HTTPS is the secure version of HTTP.
All data transferred is encrypted, meaning:
Hackers cannot see what you send or receive
You are really connected to the correct server, not an impersonator
Extra Tip: HTTPS uses TLS (Transport Layer Security) to encrypt the connection. SSL is outdated.

***What is a URL? (Uniform Resource Locator)***
A URL tells the browser how and where to access a resource on the internet. A full URL can include:

http://user:password@tryhackme.com:80/view-room?id=1#task3
URL Breakdown:
==Part==             	==Meaning==
Scheme        	Protocol to use → http, https, ftp
User         	    Optional login credentials
Host	            Domain name or IP address of the server
Port	                Connection port (default: 80 for HTTP, 443 for HTTPS)
Path	            Resource location on the server (like /view-room)
Query String	Additional data sent in the URL (e.g., ?id=1)
Fragment	    Jump to a specific section on the page (e.g., #task3)

**Making an HTTP Request**
An HTTP request line looks like:
GET / HTTP/1.1
**3 Main Parts:**
Request Method: e.g., GET, POST, PUT, DELETE
Requested Path: the page you want to access (e.g., /)
Protocol Version: e.g., HTTP/1.1, HTTP/2

Example HTTP Request
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referrer: https://tryhackme.com/
- Explanation by Line:
Line 1: GET request for the homepage using HTTP/1.1
Line 2: Tells the server which domain is being requested
Line 3: User-Agent = browser + version
Line 4: Referer = where the user came from
Line 5: Ends with a blank line = end of request

HTTP Response Example
HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98

<html>
<head><title>TryHackMe</title></head>
<body>Welcome To TryHackMe.com</body>
</html>
- Explanation by Line:
Line 1: Protocol version + Status Code (200 OK)
Line 2: Web server info (nginx/1.15.8)
Line 3: Server's current date and time
Line 4: Type of content (text/html, image/png, application/json, etc.)
Line 5: Length of the content in bytes
Line 6: Blank line = end of headers
Line 7–X: Actual response content (HTML in this case)

- Status Codes Reminder:
Code	Meaning
200	OK (Success)
301	Moved Permanently
403	Forbidden
404	Not Found
500	Server Error

**HTTP Methods**
**GET**
Used to retrieve information from a web server.
It doesn’t change anything on the server.
Example: Viewing a blog post or a public profile.

**POST**
Used to send data to the web server.
Commonly used to create new records.
Example: Registering a new user account, submitting a form.

**PUT**
Used to update existing data on the web server.
Example: Updating your email address or profile info.

**DELETE**
Used to remove information from the web server.
Example: Deleting a post or account.

**HTTP Status Codes**
Status Code Ranges:
==Code range==	                          ==Meaning==
100–199	Informational: Request accepted, continue (rare today)
200–299	Success: Request was successful
300–399	Redirection: Client is redirected elsewhere
400–499	Client Errors: Problem from the client's side
500–599	Server Errors: Problem on the server side

**Common Status Codes**
==Code==	                                      ==Meaning==
==200== OK	Everything went well
==201== Created	A new resource (e.g., user/blog post) was created
==301== Moved Permanently	Page has moved, use new address
==302== Found	Temporary redirect
==400== Bad Request	Client sent something invalid or incomplete
==401== Not Authorized	Not logged in or missing credentials
==403== Forbidden	Logged in, but not allowed to view resource
==404== Not Found	Page/resource doesn’t exist
==405== Method Not Allowed	Wrong request method used (e.g., GET instead of POST)
==500== Internal Server Error	Server had a problem it couldn’t handle
==503== Service Unavailable	Server is down or overloaded

**HTTP Headers**
Headers = extra info sent with HTTP requests or responses.
They’re not required… but super important for modern websites!

- Common Request Headers
(Sent from browser to server)
==Header==                                 	==Description==
**Host**	Tells the server which domain you want (in case it hosts multiple sites)
**User-Agent**	Tells server your browser and version, so it can format content correctly
**Content-Length**	Indicates the size of the data being sent (e.g., form data)
**Accept-Encoding**	Tells the server which compression types your browser supports (gzip, deflate, etc.)
**Cookie**	Sends saved cookies (session info, login, preferences) to the server

- Common Response Headers
(Sent from server to browser)
==Header==                                	==Description==
**Set-Cookie**	Tells browser to store a cookie (e.g., session ID)
**Cache-Control**	Controls how long the browser should cache the response
**Content-Type**	Describes the type of content (HTML, CSS, JSON, images, etc.)
**Content-Encoding**	Tells which compression method was used (gzip, br, etc.)

- Simple Example:
When you visit a site, your browser says:
“Hey, I’m Firefox 87 (User-Agent), I want this host (Host), I accept gzip (Accept-Encoding)...”
Then the server replies:
“Cool, here’s some HTML (Content-Type: text/html), compressed with gzip (Content-Encoding), and save this cookie.”

Bonus: These headers also help with performance, security, caching, and user session management.

##### ***What is a Cookie?***
A cookie is a small piece of data stored on your computer by a website.
It is saved when a server sends a Set-Cookie header in an HTTP response.
Every future request to that website includes the cookie data automatically.
This helps identify users, remember preferences, or maintain login sessions.

**Why Are Cookies Needed?**
Because HTTP is stateless — it doesn't remember previous requests.
Cookies allow the server to recognize returning users or keep track of who you are.

- Example Cookie Exchange (Step-by-Step)
Client requests a web-page:
→ GET / HTTP/1.1
Server responds with a form (e.g., asking for your name)
Client sends form back:
→ POST / with name=adam
Server replies with a cookie:
→ Set-Cookie: name=adam
Next time, browser includes cookie in the request:
→ Cookie: name=adam
Server reads the cookie and responds differently:
→ Example: Displays "Welcome back, Adam" instead of the form

- Use Cases for Cookies:
Authentication (e.g., staying logged in)
Remembering preferences
Tracking returning visitors
Often stores a token, not raw credentials

- Viewing Cookies in Browser:
Open DevTools (F12)
Go to Network tab
Click on a request
Check the Cookies section to see sent or received cookies

##### ***How websites work:***
When you visit a website, your browser sends a request to a web server.
The server processes the request and sends back a response.
The browser then displays the page to you using that response.

**Basic Flow:**
Browser → Internet → Server → Response → Back to Browser
Main components:
Front End (Client-side) – How the browser renders the page.
Back End (Server-side) – Where the request is processed and response generated.

#### ***HTML***
Websites use:
HTML – for structure
CSS – for styling
JavaScript – for interactivity

- Basic HTML Example:
  <head>
    <title>Page Title</title>
  </head>
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Example Heading</h1>
    <p>Example paragraph.</p>
  </body>
</html>
``` 
- Key Elements:
```
<!DOCTYPE html> → Declares HTML5 document
<html> → Root element
<head> → Metadata (e.g., title)
<body> → Main content
<h1> → Heading
<p> → Paragraph
```
- Right-click any web-page and choose "View Page Source" to see the HTML.

***JavaScript (JS):***
Makes websites interactive
HTML = structure / JS = behavior
Without JS, pages are static and cannot respond to user actions

How to add JS:
```JS
<script src="/location/of/javascript_file.js"></script>

```

**What is Sensitive Data Exposure?**
When a website exposes sensitive information (e.g., passwords, hidden links) in clear text to the user.
Usually found in the HTML source code.
Websites are built using HTML, which users can inspect via “View Page Source”.

- A developer may accidentally leave sensitive data like:
Temporary login credentials
Hidden internal links
API keys, etc.
==Security tip:== Always inspect the page source when auditing a website to look for:
Exposed login data
Comments that contain secrets

***What is HTML Injection?***
Happens when user input is placed directly into HTML without sanitization.
User can inject custom HTML/JavaScript into the page.
- Example:
User types into a text field.
JavaScript function inserts that value into the page.
If input is not sanitized, custom code is executed/displayed.
- Example function:
```
function sayHi() {
  const name = document.getElementById("name").value;
  document.getElementById("welcome-msg").innerHTML = "Welcome " + name;
}
    Risk: <h1>, <script>, etc. will work if not filtered.
    Solution: Always sanitize user input before inserting it into HTML/JS.
```

***Steps when you access a website:***
1. Browser sends request to visit a site.
2. DNS resolves the domain to an IP address.
3. Your computer connects to the web server.
4. Uses HTTP protocol to talk to the server.
5. Server sends HTML, CSS, JS, images, etc.
6. Browser renders the page for you.
- This entire flow makes websites work behind the scenes.

**Load Balancer**
Distributes traffic to multiple servers.
Uses algorithms like:
- Round-robin – sends requests in order.
- Weighted – sends to least busy server.
Performs health checks on servers.

**CDN (Content Delivery Network)**
Hosts static files (JS, CSS, images, videos) on global servers.
Delivers from nearest location to reduce latency.

**Databases**
Store and retrieve user data.
Examples: MySQL, MongoDB, PostgreSQL, MSSQL, etc.

**WAF (Web Application Firewall)**
Filters and inspects requests before reaching server.
Blocks suspicious or high-volume requests (e.g. bots, attacks).
Implements rate limiting and attack detection.

**What is a Web Server?**
Software that handles incoming HTTP requests and delivers content.
Examples: Apache, Nginx, IIS, NodeJS
Serves files from a root directory (e.g., /var/www/html)

**Virtual Hosts**
Allow multiple domains on a single server.
Direct traffic based on host-name.
Example:
one.com → /var/www/website_one
two.com → /var/www/website_two

**Static vs. Dynamic Content**
==Static:== Files that never change (HTML, CSS, images).
==Dynamic:== Content changes based on data or user input.
Dynamic content is created by the Back-end and shown by the Front-end.

**Back-end Languages**
Used for dynamic content and interactivity.
Examples: PHP, Python, NodeJS, Ruby, Perl

***WEBSITE EXAMPLE:***
1. Request tryhackme.com in your browser
2. Check Local Cache for IP Address
3. Check your recursive DNS Server for Address
4. Query root server to find authoritative DNS Server
5. Authoritative DNS server advises the IP address for the website
6. Request passes through a Web Application Firewall
7. Request passes through a Load Balancer
8. Connect to Web-server on port 80 or 443
9. Web server receives the GET request
10. Web Application talks to Database
11. Your Browser renders the HTML into a viewable website


























































































































































































































