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

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### VPN and Proxy

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Hosting

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### OSI network model

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### HTTP Protocol

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### TCP/IP stack

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Network problems

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

-   ### Network diagnostics

<details>
    <summary>🔗 <b>References</b></summary>

</details>

<div align="right"><a href="#top">Contents ⬆️</a></div>

## PC device

-   ### Main components (hardware)

<details>
    <summary>🔗 <b>References</b></summary>

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
-   [A curated and opinionated list of resources (English & Russian) for Backend developers](https://github.com/zhashkevych/awesome-backend)
-   [Hussein Nasser – YouTube channel about networking](https://www.youtube.com/c/HusseinNasser-software-engineering)

<div align="center">Made with &#9829;</div>
<div align="center"><a href="https://github.com/cheatsnake/backend-cheats/blob/master/LICENSE">LICENSE</a> 2022</div>
