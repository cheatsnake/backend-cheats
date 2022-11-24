<a href="https://github.com/cheatsnake/backend-cheats/blob/master/README.md"><p align="center"><img src="./files/logo.png" alt="Logo"/></p></a>

This repository is a visual cheatsheet on the main topics in Backend-development. All the material is divided into topics and subtopics. The structure of the material consists of three parts:

-   **Visual part** - various images/tables/cheatsheets for better understanding (may not be available). All pictures and tables are made from scratch, specifically for this repository.
-   **Summary** - A very brief summary with a list of key terms and concepts. The terms are hyperlinked to the appropriate section on Wikipedia or a similar reference resource.
-   **References to sources** - resources where you may find complete information on a particular issue. If possible, the most authoritative sources are indicated, or those that provide information in as simple and comprehensible language as possible.

> 🛠 The repository is under active development, so it is constantly updated and supplemented

> 🤝 If you want to help the project, feel free to send your [Pull requests](https://github.com/cheatsnake/backend-cheats/pulls)

> 📝 Translation into English is in progress

<p><a name="top"></a></p>

## Contents

<details>
    <summary><a href="#network---internet">1. Network & Internet</a></summary>
    
  * [How the Internet works](#how-the-internet-works)
  * [What is a domain name](#what-is-a-domain-name)
  * [IP address](#ip-address)
  * [What is DNS](#what-is-dns)
  * [Web application design](#web-application-design)
  * [Browsers and how they work](#browsers-and-how-they-work)
  * [VPN and Proxy](#vpn-and-proxy)
  * [Hosting](#hosting)
  * [OSI network model](#osi-network-model)
  * [HTTP Protocol](#http-protocol)
  * [TCP/IP stack](#tcpip-stack)
  * [Network problems](#network-problems)
  * [Network diagnostics](#network-diagnostics)
</details>

<details>
    <summary><a href="#pc-device">2. PC device</a></summary>
    
  * [Main components (hardware)](#main-components--hardware-)
  * [Operating system design](#operating-system-design)
  * [Processes and threads](#processes-and-threads)
  * [Concurrency and parallelism](#concurrency-and-parallelism)
  * [Inter-process communication](#inter-process-communication)
</details>

<details>
    <summary><a href="#linux-basics">3. Linux Basics</a></summary>
    
  * [Working with the terminal](#working-with-the-terminal)
  * [Package manager](#package-manager)
  * [Bash scripts](#bash-scripts)
  * [Users and groups](#users-and-groups)
  * [Permissions](#permissions)
  * [Working with processes](#working-with-processes)
  * [Working with SSH](#working-with-ssh)
  * [Task Scheduler](#task-scheduler)
  * [System logs](#system-logs)
  * [Linux problems](#linux-problems)
</details>

<details>
    <summary><a href="#general-knowledge">4. General knowledge</a></summary>
    
  * [Number systems](#number-systems)
  * [Logical operations](#logical-operations)
  * [Data structures](#data-structures)
  * [Basic algorithms](#basic-algorithms)
  * [Algorithm complexity](#algorithm-complexity)
  * [Data storage formats](#data-storage-formats)
  * [Text encodings](#text-encodings)
</details>

<details>
    <summary><a href="#programming-language">5. Programming Language</a></summary>
    
  * [Classification of programming languages](#classification-of-programming-languages)
  * [Language Basics](#language-basics)
  * [Server development](#server-development)
  * [Multithreading](#multithreading)
  * [Advanced Topics](#advanced-topics)
  * [Code quality](#code-quality)
</details>

<details>
    <summary><a href="#databases">6. Databases</a></summary>
    
  * [Database classification](#database-classification)
  * [Relational database](#relational-database)
  * [MongoDB](#mongodb)
  * [Redis](#redis)
  * [ACID Requirements](#acid-requirements)
  * [Designing databases](#designing-databases)
</details>

<details>
    <summary><a href="#api-development">7. API development</a></summary>
    
  * [REST API](#rest-api)
  * [GraphQL](#graphql)
  * [WebSockets](#websockets)
  * [RPC and gRPC](#rpc-and-grpc)
  * [WebRTC](#webrtc)
</details>

<details>
    <summary><a href="#software">8. Software</a></summary>
    
  * [Git version control system](#git-version-control-system)
  * [Docker](#docker)
  * [Postman/Insomnia](#postmaninsomnia)
  * [Web servers](#web-servers)
  * [Message brokers](#message-brokers)
</details>

<details>
    <summary><a href="#security">9. Security</a></summary>
    
  * [Web application vulnerabilities](#web-application-vulnerabilities)
  * [Environment variables](#environment-variables)
  * [Hashing](#hashing)
  * [Authentication and authorization](#authentication-and-authorization)
  * [SSL/TLS](#ssltls)
</details>

<details>
    <summary><a href="#testing">10. Testing</a></summary>
    
  * [Unit Tests](#unit-tests)
  * [Integration tests](#integration-tests)
  * [E2E tests](#e2e-tests)
  * [Load testing](#load-testing)
  * [Regression testing](#regression-testing)
</details>

<details>
    <summary><a href="#optimization">11. Optimization</a></summary>

-   [Profiling](#profiling)
-   [Caching](#caching)
-   [Load balancing](#load-balancing)
</details>

<details>
    <summary><a href="#documentation">12. Documentation</a></summary>
    
  * [Markdown](#markdown)
  * [Documentation inside code](#documentation-inside-code)
  * [API Documentation](#api-documentation)
  * [Static generators](#static-generators)
</details>

<details>
    <summary><a href="#building-architecture">13. Building Architecture</a></summary>
    
  * [Architectural templates](#architectural-templates)
  * [Design patterns](#design-patterns)
  * [Monolithic and microservice architecture](#monolithic-and-microservice-architecture)
  * [Horizontal and vertical scaling](#horizontal-and-vertical-scaling)
</details>

[Additional and similar resources](#additional-and-similar-resources)

## Network & Internet

[Internet](https://en.wikipedia.org/wiki/Internet) is a worldwide system that connects computer networks from around the world into a single network for storing/transferring information. The Internet was originally developed for the military. But soon it began to be implemented in universities, and then it could be used by private companies, which began to organize networks of providers that provide Internet access services to ordinary citizens. By early 2020, the number of Internet users exceeded 4.5 billion.

-   ### How the Internet works

    <p align="center"><img src="./files/network-internet/Internet.png" alt="Internet"/></p>

    Your computer has never been directly connected to the Internet. Because it can only see its local network to which other devices are connected via wired ([Ethernet](https://en.wikipedia.org/wiki/Ethernet)) or wirelessly (Wi-Fi, Bluetooth). To communicate with the Internet, you have a special minicomputer in your local network - [router](<https://en.wikipedia.org/wiki/Router_(computing)>). It then connects you to [Internet Service Provider](https://en.wikipedia.org/wiki/Internet_service_provider) which in turn connects to other higher-level providers. Thus, your message, transits through the network of several ISPs before reaching the destination network.

    The Internet is just a long wire to which a small number of [Tier 1 providers](https://en.wikipedia.org/wiki/Tier_1_network) are directly connected. The ISPs below that are just renting access.

    -   [Host](<https://en.wikipedia.org/wiki/Host_(network)>)
        > Any device that is on any network.
    -   [Server](<https://en.wikipedia.org/wiki/Server_(computing)>)
        > A special computer on the network that serves requests from other computers.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**How does the Internet work?** – MDN](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work)
2. 📺 [**How does the internet work? (Full Course)** – YouTube](https://youtu.be/zN8YNNHcaZc)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### What is a domain name

    <p align="center"><img src="./files/network-internet/domain_eng.png" alt="Domain name"/></p>

    [Domain Names](https://en.wikipedia.org/wiki/Domain_name) are human-readable addresses of web servers available on the Internet. They consist of parts (levels) separated from each other by a dot. Each of these parts provides specific information about the domain name. For example country, service name, localization, etc.

    -   Who owns domain names
        > [The ICANN Corporation](https://en.wikipedia.org/wiki/ICANN) is the founder of the distributed domain registration system. It gives accreditations to companies that want to sell domains. In this way a competitive domain market is formed.
    -   How to buy a domain name
        > A domain name cannot be bought forever. It is leased for a certain period of time. It is better to buy domains from [accredited registrars](https://www.icann.org/en/accredited-registrars?filter-letter=a&sort-direction=asc&sort-param=name&page=1) (you can find them in almost any country).

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is a Domain Name?** – MDN](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_domain_name)
2. 📺 [**A Beginners Guide to How Domain Names Work!** – YouTube](https://youtu.be/Y4cRx19nhJk)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### IP address

    <p align="center"><img src="./files/network-internet/IPv4-IPv6.png" alt="IPv4-IPv6"/></p>

    [IP address](https://en.wikipedia.org/wiki/IP_address) is a unique numeric address that is used to recognize a particular device on the network.

    -   Levels of visibility
        > -   External and publicly accessible IP address that belongs to your ISP and is used to access the Internet by hundreds of other users.
        > -   The IP address of your router in your ISP's local network, the same IP address from which you access the Internet.
        > -   The IP address of your computer in the local (home) network created by the router, to which you can connect your devices. Typically, it looks like 192.168.XXX.XXX.
        > -   The internal IP address of the computer, inaccessible from the outside and used only for communication between the running processes. It is the same for everyone - 127.0.0.1 or just _localhost_.
    -   [Port](<https://en.wikipedia.org/wiki/Port_(computer_networking)>)
        > One device (computer) can run many applications that use the network. In order to correctly recognize where and which data coming over the network should be delivered (to which of the applications) a special numerical number - a port is used. That is, each running process on a computer which uses a network connection has its own personal port.
    -   [IPv4](https://en.wikipedia.org/wiki/IPv4)
        > Version 4 of the IP protocol. It was developed in 1981 and limits the address space to about 4.3 billion (2^32) possible unique addresses.
    -   [IPv6](https://en.wikipedia.org/wiki/IPv6)
        > Over time, the allocation of address space began to happen at a much faster rate, forcing the creation of a new version of the IP protocol to store more addresses. IPv6 is capable of issuing 2^128 (is huge number) unique addresses.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**IP addresses. Explained** – YouTube](https://youtu.be/7_-qWlvQQtY)
2. 📺 [**Public IP vs. Private IP and Port Forwarding (Explained by Example)** – YouTube](https://youtu.be/92b-jjBURkw)
3. 📺 [**What is IP address and types of IP address - IPv4 and IPv6** – YouTube](https://youtu.be/8npT9AALbrI)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### What is DNS

    <p align="center"><img src="./files/network-internet/dns.png" alt="DNS"/></p>

    [DNS (Domain Name System)](https://en.wikipedia.org/wiki/DNS) is a decentralized Internet address naming system that allows you to create human-readable alphabetic names (domain names) corresponding to the numeric [IP addresses](#ip-address) used by computers.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is DNS? Domain Name System explained** – freeCodeCamp](https://www.freecodecamp.org/news/what-is-dns/)
2. 📺 [**DNS (Domain Name System) explained. Types of Domain Name Servers** – YouTube](https://youtu.be/JkEYOt08-rU)
3. 📺 [**DNS as Fast As Possible** – YouTube](https://youtu.be/Rck3BALhI5c)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Web application design

    Modern [web applications](https://en.wikipedia.org/wiki/Web_application) consist of two parts: [Frontend and Backend](https://en.wikipedia.org/wiki/Frontend_and_backend). Thus implementing a [client-server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model).

    The tasks of the Frontend are:

    -   Implementation of the user interface (appearance of the application)
        > A special markup language [HTML](https://en.wikipedia.org/wiki/HTML) is used to create web pages. <br> > [CSS](https://en.wikipedia.org/wiki/CSS) style language is used to style fonts, layout of content, etc. <br> > [JavaScript](https://en.wikipedia.org/wiki/JavaScript) programming language is used to add dynamics and interactivity. <br>
        > As a rule, these tools are rarely used in their pure form, as so-called [frameworks](https://2020.stateofjs.com/en-US/technologies/front-end-frameworks/) and [preprocessors](https://www.freecodecamp.org/news/css-preprocessors/) exist for more convenient and faster development. <br>
    -   Creating functionality for generating requests to the server
        > These are usually different types of input forms that can be conveniently interacted with.
    -   Receives data from the server and then processes it for output to the client

    Tasks of the Backend:

    -   Handling client requests
        > Checking for permissions and access, all sorts of validations, etc.
    -   Implementing business logic
        > A wide range of tasks can be implied here: working with databases, information processing, computation, etc. This is, so to speak, the heart of the Backend world. This is where all the important and interesting stuff happens.
    -   Generating a response and sending it to the client

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Front-End vs. Back-End explained**](https://blog.teamtreehouse.com/i-dont-speak-your-language-frontend-vs-backend)
2. 📺 [**Everything You NEED to Know About WEB APP Architecture** – YouTube](https://youtu.be/sDlCSIDwpDs)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Browsers and how they work

    <p align="center"><img src="./files/network-internet/browser_eng.png" alt="Browser"/></p>

    [Browser](https://en.wikipedia.org/wiki/Web_browser) is a client which can be used to send requests to a server for files which can then be used to render web pages. In simple terms, a browser can be thought of as a program for viewing HTML files, which can also search for and download them from the Internet.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**How browsers work** – MDN](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)
2. 📄 [**How browsers work: Behind the scenes of modern web browsers** – web.dev](https://web.dev/howbrowserswork/)
3. 📺 [**What is a web browser?** – YouTube](https://youtu.be/QzohDuGk4mM)
4. 📺 [**Anatomy of the browser 101 (Chrome University 2019)** – YouTube](https://youtu.be/PzzNuCk-e0Y)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### VPN and Proxy

    <p align="center"><img src="./files/network-internet/proxy-vpn_eng.png" alt="Proxy & VPN"/></p>

    The use of VPNs and Proxy is quite common in recent years. With the help of these technologies, users can get basic anonymity when surfing the web, as well as bypass various regional blockages.

    -   [VPN (Virtual Private Network)](https://en.wikipedia.org/wiki/VPN)
        > A technology that allows you to become a member of a private network (similar to your local network), where requests from all participants go through a single public IP address. This allows you to blend in with the general mass of requests from other participants. <br>
        >
        > -   Simple procedure for connection and use. <br>
        > -   Reliable traffic encryption. <br>
        > -   There is no guarantee of 100% anonymity, because the owner of the network knows the IP-addresses of all participants. <br>
        > -   VPNs are useless for dealing with multi-accounts and some programs because all accounts operating from the same VPN are easily detected and blocked. <br>
        > -   Free VPNs tend to be heavily loaded, resulting in unstable performance and slow download speeds. <br>
    -   [Proxy (proxy server)](https://en.wikipedia.org/wiki/Proxy_server)
        > A proxy is a special server on the network that acts as an intermediary between you and the destination server you intend to reach. When you are connected to a proxy server all your requests will be performed on behalf of that server, that is, your IP address and location will be substituted. <br>
        >
        > -   The ability to use an individual IP address, which allows you to work with multi-accounts. <br>
        > -   Stability of the connection due to the absence of high loads. <br>
        > -   Connection via proxy is provided in the operating system and browser, so no additional software is required. <br>
        > -   There are proxy varieties that provide a high level of anonymity. <br>
        > -   The unreliability of free solutions, because the proxy server can see and control everything you do on the Internet. <br>

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is VPN? How It Works, Types of VPN** – kaspersky.com](https://www.kaspersky.com/resource-center/definitions/what-is-a-vpn)
2. 📺 [**What Is a Proxy and How Does It Work?** – YouTube](https://youtu.be/ayo2EUPTEkE)
3. 📺 [**Proxy vs. Reverse Proxy (Explained by Example)** – YouTube](https://youtu.be/ozhe__GdWC8)
4. 📺 [**VPN vs Proxy Explained Pros and Cons** – YouTube](https://youtu.be/npnqyRT77Zc)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Hosting

    <p align="center"><img src="./files/network-internet/Hosting.png" alt="Hosting"/></p>

    [Hosting](https://en.wikipedia.org/wiki/Web_hosting_service) is a special [service provided](https://en.wikipedia.org/wiki/Internet_hosting_service) by hosting providers, which allows you to rent space on a server (which is connected to the Internet around the clock), where your data and files can be stored. There are different options for hosting, where you can use not only the disk space of the server, but also the CPU power to run your network applications.

    -   [Virtual hosting](https://en.wikipedia.org/wiki/Virtual_hosting)
        > One physical server that distributes its resources to multiple tenants.
    -   [VPS/VDS](https://en.wikipedia.org/wiki/Virtual_private_server)
        > Virtual servers that emulate the operation of a separate physical server and are available for rent to the client with maximum privileges.
    -   [Dedicated server](https://en.wikipedia.org/wiki/Dedicated_hosting_service)
        > Renting a full physical server with full access to all resources. As a rule, this is the most expensive service.
    -   [Cloud hosting](https://en.wikipedia.org/wiki/Cloud_storage)
        > A service that uses the resources of several servers. When renting, the user pays only for the actual resources used.
    -   [Colocation](https://en.wikipedia.org/wiki/Colocation_centre)
        > A service that gives the customer the opportunity to install their equipment on the provider's premises.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is Web Hosting?** – namecheap.com](https://www.namecheap.com/hosting/what-is-web-hosting-definition/)
2. 📺 [**What is Web Hosting and How Does It Work?** – YouTube](https://youtu.be/H8oAvyqQwew)
3. 📺 [**Different Hosting Types Explained** – YouTube](https://youtu.be/CtNWVmt9U1M)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### OSI network model

    | №   | Level              | Used protocols       |
    | --- | ------------------ | -------------------- |
    | 7   | Application layer  | HTTP, DNS, FTP, POP3 |
    | 6   | Presentation layer | SSL, SSH, IMAP, JPEG |
    | 5   | Session layer      | APIs Sockets         |
    | 4   | Transport layer    | TCP, UDP             |
    | 3   | Network layer      | IP, ICMP, IGMP       |
    | 2   | Data link layer    | Ethernet, MAC, HDLC  |
    | 1   | Physical layer     | RS-232, RJ45, DSL    |

    -   [Physical layer](https://en.wikipedia.org/wiki/Physical_layer)
        > At this level, bits (ones/zeros) are encoded into physical signals (current, light, radio waves) and transmitted further by wire ([Ethernet](https://en.wikipedia.org/wiki/Ethernet)) or wirelessly ([Wi-Fi](https://en.wikipedia.org/wiki/Wi-Fi)).
    -   [Data link layer](https://en.wikipedia.org/wiki/Data_link_layer)
        > Physical signals from layer 1 are decoded back into ones and zeros, errors and defects are corrected, and the sender and receiver [MAC addresses](https://en.wikipedia.org/wiki/MAC_address) are extracted.
    -   [Network layer](https://en.wikipedia.org/wiki/Network_layer)
        > This is where traffic routing, DNS queries and [IP packet](https://en.wikipedia.org/wiki/Internet_Protocol) generation take place.
    -   [Transport layer](https://en.wikipedia.org/wiki/Transport_layer)
        > The layer responsible for data transfer. There are two important protocols: <br>
        >
        > -   [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) is a protocol that ensures reliable data transmission. TCP guarantees data delivery and preserves the order of the messages. This has an impact on the transmission speed. This protocol is used where data loss is unacceptable, such as when sending mail or loading web pages. <br>
        > -   [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol) is a simple protocol with fast data transfer. It does not use mechanisms to guarantee the delivery and ordering of data. It is used e.g. in online games where partial packet loss is not crucial, but the speed of data transfer is much more important. Also, requests to DNS servers are made through UDP protocol.
    -   [Session layer](https://en.wikipedia.org/wiki/Session_layer)
        > Responsible for opening and closing communications (sessions) between two devices. Ensures that the session stays open long enough to transfer all necessary data, and then closes quickly to avoid wasting resources.
    -   [Presentation layer](https://en.wikipedia.org/wiki/Presentation_layer)
        > Transmission, encryption/decryption and data compression. This is where data that comes in the form of zeros and ones are converted into desired formats (PNG, MP3, PDF, etc.)
    -   [Application layer](https://en.wikipedia.org/wiki/Application_layer)
        > Allows the user's applications to access network services such as database query handler, file access, email forwarding.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Layers of OSI Model** – geeksForGeeks](https://www.geeksforgeeks.org/layers-of-osi-model/)
2. 📺 [**The OSI Model - Explained by Example** – YouTube](https://youtu.be/7IS7gigunyI)
3. 📺 [**TCP vs UDP Crash Course** – YouTube](https://youtu.be/qqRYkcta6IE)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### HTTP Protocol

    [HTTP (HyperText Transport Protocol)](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) is the most important protocol on the Internet. It is used to transfer data of any format. The protocol itself works according to a simple principle: request -> response.

    -   [Structure of HTTP messages](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)
        > Start Line > Headers > Message Body

    <p align="center"><img src="./files/network-internet/http_eng.png" alt="HTTP"/></p>

    -   [Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
        > Additional service information that is sent with the request/response. <br>
        > Common headers: [Host](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Host), [User-Agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent), [If-Modified-Since](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/If-Modified-Since), [Cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cookie), [Referer](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer), [Authorization](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization), [Cache-Control](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control), [Content-Type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Type), [Content-Length](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Length), [Last-Modified](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Last-Modified), [Set-Cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie), [Content-Encoding](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Encoding).
    -   [Request methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
        > [GET](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET) - data retrieval request <br> [POST](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST) - request with data to create a new record <br> [PUT](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT) - request with data to change existing record <br> [DELETE](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE) - deletion request <br> Others: [HEAD](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD), [CONNECT](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/CONNECT), [OPTIONS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS), [TRACE](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/TRACE), [PATCH](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PATCH). <br>
    -   [Response status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
        > Each response from the server has a special numeric code that characterizes the state of the sent request. These codes are divided into 5 main classes:
        >
        > -   1хх - service information <br>
        > -   2хх - successful request <br>
        > -   3хх - redirect to another address <br>
        > -   4хх - client side error <br>
        > -   5хх - server side error <br>
    -   [HTTPS](https://developer.mozilla.org/en-US/docs/Glossary/https)
        > Same HTTP, but with encryption support
    -   [Cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
        > Because the HTTP protocol does not allow you to save any information about the status of previous requests/responses, you need to use cookies. Cookies allow the server to store various information on the client side, which the client can then send back to the server. In particular, cookies can be used for authorization or to save various settings/configurations.
    -   [CORS (Cross origin resource sharing)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
        > A technology that allows one domain to securely receive data from another domain.
    -   [CSP (Content Security Policy)](https://developer.mozilla.org/ru/docs/Web/HTTP/CSP)
        > A special header that allows you to recognize and eliminate certain types of web application vulnerabilities.
    -   [HTTP/1.0 vs HTTP/1.1 vs HTTP/2](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Persistent_connections)
        > The main innovation in version 1.1 is the permanent connection mode, which allows you to send several requests per connection. In version 2, the protocol became binary, with the ability to transmit data from multiple streams on the same channel.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**How HTTP Works and Why it's Important** – freeCodeCamp](https://www.freecodecamp.org/news/how-the-internet-works/)
2. 📄 [**Hypertext Transfer Protocol (HTTP)** – MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP)
3. 📺 [**Hyper Text Transfer Protocol Crash Course** – YouTube](https://youtu.be/0OrmKCB0UrQ)
4. 📄 [**HTTP vs HTTPS – What's the Difference?** – freeCodeCamp](https://www.freecodecamp.org/news/http-vs-https/)
5. 📺 [**HTTP Cookies Crash Course** – YouTube](https://youtu.be/sovAIX4doOE)
6. 📺 [**Cross Origin Resource Sharing (Explained by Example)** – YouTube](https://youtu.be/Ka8vG5miErk)
7. 📺 [**When to use HTTP GET vs POST?** – YouTube](https://youtu.be/K8HJ6DN23zI)
8. 📺 [**How HTTP/2 Works, Performance, Pros & Cons and More** – YouTube](https://youtu.be/fVKPrDrEwTI)
9. 📺 [**HTTP/2 Critical Limitation that led to HTTP/3 & QUIC** – YouTube](https://youtu.be/GriONb4EfPY)
10. 📺 [**304 Not Modified HTTP Status (Explained with Code Example and Pros & Cons)** – YouTube](https://youtu.be/0QHmHR55_Lo)
11. 📺 [**What is the Largest POST Request the Server can Process?** – YouTube](https://youtu.be/0QHmHR55_Lo)
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### TCP/IP stack

    <p align="center"><img src="./files/network-internet/tcp-ip_eng.png" alt="TCP/IP"/></p>

    Compared to the [OSI model](https://github.com/cheatsnake/backend-cheats/blob/master/README_ENG.md#osi-network-model), the [TCP/IP](https://en.wikipedia.org/wiki/Internet_protocol_suite) stack has a simpler architecture. It is widely used and was first used as the basis for the creation of a global network, and then to describe the workings of the Internet.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**What is the TCP/IP Model? Layers and Protocols Explained** – freeCodeCamp](https://www.freecodecamp.org/news/what-is-tcp-ip-layers-and-protocols-explained/)
2. 📺 [**What is TCP/IP?** – YouTube](https://youtu.be/PpsEaqJV_A0)
3. 📺 [**How TCP really works. Three-way handshake. TCP/IP Deep Dive** – YouTube](https://youtu.be/rmFX1V49K8U)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Network problems

    <p align="center"><img src="./files/network-internet/problems_eng.gif" alt="Problems"/></p>

    The quality of networks, much less the Internet, is far from ideal. This is due to the complex and dispersed network structure in different devices. Therefore, on the functioning of the network affects a huge number of factors. For example: the stability of the connection between the client device and its router, the quality of service of the provider, the power and performance of the server, the physical distance between the client and the server, etc.

    -   [Latency](https://developer.mozilla.org/en-US/docs/Web/Performance/Understanding_latency)
        > The time it takes for a data packet to travel from sender to receiver. It depends more on the physical distance.
    -   [Packet loss](https://en.wikipedia.org/wiki/Packet_loss)
        > Not all packets traveling over the network can reach their destination. This happens most often when using wireless networks or due to [network congestion](https://en.wikipedia.org/wiki/Network_congestion).
    -   [Round Trip Time (RTT)](https://en.wikipedia.org/wiki/Round-trip_delay)
        > The time it takes for the data packet to reach its destination + the time to respond that the packet was received successfully.
    -   [Jitter](https://www.ir.com/guides/what-is-network-jitter)
        > Delay fluctuations, unstable ping (for example, 50ms, 120ms, 35ms...).
    -   [Packet reordering](https://wiki.geant.org/display/public/EK/PacketReordering)
        > The IP protocol does not guarantee that packets are delivered in the order in which they are sent.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Understanding latency** – MDN](https://developer.mozilla.org/en-US/docs/Web/Performance/Understanding_latency)
2. 📺 [**What is latency? What affects latency?** – YouTube](https://youtu.be/epAXDsq5SbE)
3. 📺 [**Basics of network bandwidth, latency, and jitter** – YouTube](https://youtu.be/WdbJdUh6W08)
4. 📺 [**Round Trip Time (RTT)** – YouTube](https://youtu.be/nT9F-USjtBg)
5. 📺 [**What Causes Packet Loss and How to Eliminate It In Your Network** – YouTube](https://youtu.be/Cg656nGbXe4)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Network diagnostics

    <p align="center"><img src="./files/network-internet/Traceroute.png" alt="Traceroute"/></p>

    -   [Traceroute](https://en.wikipedia.org/wiki/Traceroute)
        > A procedure that allows you to trace to which nodes, with which IP addresses, a packet you send before it reaches its destination. Tracing can be used to identify computer network related problems and to examine/analyze the network.
    -   [Ping scan](<https://en.wikipedia.org/wiki/Ping_(networking_utility)>)
        > The easiest way to check the server for performance.
    -   [Checking for packet loss](https://www.dnsstuff.com/packet-loss-test)
        > Due to dropped connections, not all packets sent over the network reach their destination.
    -   [Wireshark](https://en.wikipedia.org/wiki/Wireshark)
        > A powerful program with a graphical interface for analyzing all traffic that passes through the network in real time.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📺 [**How does traceroute work?** – YouTube](https://youtu.be/G05y9UKT69s)
2. 📺 [**Traceroute (tracert) Explained - Network Troubleshooting** – YouTube](https://youtu.be/up3bcBLZS74)
3. 📺 [**Nmap - Host Discovery With Ping Sweep** – YouTube](https://youtu.be/LvCDaftsMwI)
4. 📺 [**Internet Troubleshooting - Pathping Packet Loss** – YouTube](https://youtu.be/VPdotNIXOgI)
5. 📺 [**Wireshark crash course (playlist)** – YouTube](https://youtube.com/playlist?list=PLBf0hzazHTGPgyxeEj_9LBHiqjtNEjsgt)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## PC device

-   ### Main components (hardware)

    -   [Motherboard](https://en.wikipedia.org/wiki/Motherboard)
        > The most important PC component to which all other elements are connected.
        >
        > -   [Chipset](https://en.wikipedia.org/wiki/Chipset) - set of electronic components that responsible for the communication of all motherboard components.
        > -   [CPU socket](https://en.wikipedia.org/wiki/CPU_socket) - socket for mounting the processor.
        > -   [VRM (Voltage Regulator Module)](https://en.wikipedia.org/wiki/Voltage_regulator_module) – module that converts the incoming voltage (usually 12V) to a lower voltage to run the processor, integrated graphics, memory, etc.
        > -   Slots for RAM.
        > -   Expansion slots [PCI-Express](https://en.wikipedia.org/wiki/PCI_Express) - designed for connection of video cards, external network/sound cards.
        > -   Slots [М.2](https://en.wikipedia.org/wiki/M.2) / [SATA](https://en.wikipedia.org/wiki/SATA) - designed to connect hard disks and SSDs.
    -   [CPU (Central processing unit)](https://en.wikipedia.org/wiki/Central_processing_unit)
        > The most important device that executes instructions (programme code). Processors only work with 1 and 0, so all programmes are ultimately a set of binary code.
        >
        > -   [Registers](https://en.wikipedia.org/wiki/Processor_register) - the fastest memory in a PC, has an extremely small capacity, is built into the processor and is designed to temporarily store the data being processed.
        > -   [Cache](https://en.wikipedia.org/wiki/CPU_cache) - slightly less fast memory, which is also built into the processor and is used to store a copy of data from frequently used cells in the main memory.
        > -   Processors can have different [architectures](https://en.wikipedia.org/wiki/Processor_design). Currently, the most common are the [x86](https://en.wikipedia.org/wiki/X86-64) architecture (desktop and laptop computers) and [ARM](https://en.wikipedia.org/wiki/ARM_architecture_family) (mobile devices as well as the latest Apple computers).
    -   [RAM (Random-access memory)](https://en.wikipedia.org/wiki/Random-access_memory)
        > Fast, low capacity memory (4-16GB) designed to temporarily store program code, as well as input, output and intermediate data processed by the processor.
    -   [Data storage](https://en.wikipedia.org/wiki/Data_storage)
        > Large capacity memory (256GB-1TB) designed for long-term storage of files and installed programmes.
    -   [GPU (Graphics card)](https://en.wikipedia.org/wiki/Graphics_card)
        > A separate card that translates and processes data into images for display on a monitor. This device is also called a discrete graphics card. Usually needed for those who do 3D modelling or play games. <br> > [Built-in graphics card](https://en.wikipedia.org/wiki/Graphics_processing_unit#Integrated_graphics_processing_unit) is a graphics card built into the processor. It is suitable for daily work.
    -   [Network card](https://en.wikipedia.org/wiki/Network_interface_controller)
        > A device that receives and transmits data from other devices connected to the [local network](https://en.wikipedia.org/wiki/Local_area_network).
    -   [Sound card](https://en.wikipedia.org/wiki/Sound_card)
        > A device that allows you to process sound, output it to other devices, record it with a microphone, etc.
    -   [Power supply unit](<https://en.wikipedia.org/wiki/Power_supply_unit_(computer)>)
        > A device designed to convert the AC voltage from the mains to DC voltage.

<details>
    <summary>🔗 <b>References</b></summary>

1. 📄 [**Understanding latency** – MDN](https://developer.mozilla.org/en-US/docs/Web/Performance/Understanding_latency)
2. 📺 [**What does what in your computer? Computer parts Explained** – YouTube](https://youtu.be/ExxFxD4OSZ0)
3. 📺 [**The Fetch-Execute Cycle: What's Your Computer Actually Doing?** – YouTube](https://youtu.be/Z5JC9Ve1sfI)
4. 📺 [**How a CPU Works in 100 Seconds // Apple Silicon M1 vs Intel i9** – YouTube](https://youtu.be/vqs_0W-MSB0)
5. 📺 [**Arm vs x86 - Key Differences Explained** – YouTube](https://youtu.be/AADZo73yrq4)
 </details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Operating system design

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Processes and threads

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Concurrency and parallelism

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Inter-process communication

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Linux Basics

-   ### Working with the terminal

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Package manager

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Bash scripts

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Users and groups

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Permissions

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Working with processes

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Working with SSH

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Task Scheduler

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### System logs

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Linux problems

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## General knowledge

-   ### Number systems

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Logical operations

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Data structures

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Basic algorithms

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Algorithm complexity

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Data storage formats

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Text encodings

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Programming Language

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Classification of programming languages

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Language Basics

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Server development

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Multithreading

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Advanced Topics

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Code quality

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Databases

-   ### Database classification

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Relational database

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### MongoDB

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Redis

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### ACID Requirements

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Designing databases

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## API development

-   ### REST API

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### GraphQL

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### WebSockets

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### RPC and gRPC

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### WebRTC

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Software

-   ### Git version control system

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Docker

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Postman/Insomnia

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Web servers

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Message brokers

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Security

-   ### Web application vulnerabilities

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Environment variables

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Hashing

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Authentication and authorization

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### SSL/TLS

<details>
    <summary>🔗 <b>References</b></summary>

</details>
 
<div align="right"><a href="#top">Contents ⬆️</a></div>

## Testing

-   ### Unit Tests

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Integration tests

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### E2E tests

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Load testing

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Regression testing

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Optimization

-   ### Profiling

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Caching

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Load balancing

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Documentation

-   ### Markdown

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Documentation inside code
<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### API Documentation

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Static generators

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Building architecture

-   ### Architectural templates

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Design patterns

<details>
    <summary>🔗 <b>References</b></summary>
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Monolithic and microservice architecture

<details>
    <summary>🔗 <b>References</b></summary>
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Horizontal and vertical scaling

<details>
    <summary>🔗 <b>References</b></summary>
</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## Additional and similar resources

-   [Backend Developer Roadmap: Learn to become a modern backend developer](https://roadmap.sh/backend)
-   [Hussein Nasser – YouTube channel about networking](https://www.youtube.com/c/HusseinNasser-software-engineering)
-   [CS50 2022 – Harvard University's course about programming](https://youtube.com/playlist?list=PLeLzIg9tqA3LQW-RiFA8zJUBcTKqUVLMU)
-   [A curated and opinionated list of resources (English & Russian) for Backend developers](https://github.com/zhashkevych/awesome-backend)

<div align="center">Made with &#9829;</div>
<div align="center"><a href="https://github.com/cheatsnake/backend-cheats/blob/master/LICENSE">LICENSE</a> 2022</div>
