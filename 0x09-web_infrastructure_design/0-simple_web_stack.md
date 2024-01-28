# A Simple Web Stack

![Image of a simple web stack](0-simple_web_stack.jpg)

[Visit Board](https://miro.com/app/board/uXjVOfJwct0=/)

## Project Description
A simple web server that servers the website under domain `www.foobar.com`. This server has no firewall set up. No SSL certificates have been set up. All the server componeents have been bundleed together. This includes database and web application. 

## Details abou this infrastructure setup

#### What a server
A server is a computer or system that is dedicated to managing network resources and providing services to other computers, known as clients, in the same network or over the internet. Servers are designed to handle specific tasks and functions, such as hosting websites, managing email communications, storing and retrieving files, running applications, or providing access to databases.

#### What is the role of the domain name.
Domains a human-friendly alias for an IP Address. For example, the domain name `www.wikipedia.org` is easier to recognize and remember than `91.198.174.192`. The IP address and domain name alias is mapped in the **Domain Name System (DNS)**

#### What type of DNS record www is in www.foobar.com?
In the domain name `www.foobar.com`, the `www` is typically a subdomain, and it is commonly associated with a CNAME (Canonical Name) DNS record. The CNAME record is used to alias one domain to another.

For example, the DNS records for `www.foobar.com` might include a CNAME record pointing to the main domain `foobar.com`

#### The role of the web server.
A web server is software or hardware that stores, processes, and serves website content to users over the internet. It handles requests from web clients (typically browsers) and responds by delivering web pages, files, or other resources. The primary function of a web server is to host websites and make them accessible to users.

#### The role of the application server.
To install, operate and host applications and associated services for end users, IT services and organizations and facilitates the hosting and delivery of high-end consumer or business applications
#### The role of the database.
To maintain a collection of organized information that can easily be accessed, managed and updated. There are two types of Databases namely, Relational Database such Postgres and MYSQl and Non-Relational Database such as MongoDB

#### What the server uses to communicate with the client (computer of the user requesting the website).
Communication between the client and the server occurs over the internet network through the TCP/IP protocol suite.

## Issues With This Infrastructure

+ There are multiple SPOF (Single Point Of Failure) in this infrastructure.<br/>For example, if the MySQL database server is down, the entire site would be down.

+ Downtime when maintenance needed.<br/>When we need to run some maintenance checks on any component, they have to be put down or the server has to be turned off. Since there's only one server, the website would be experiencing a downtime.

+ Cannot scale if there's too much incoming traffic.<br/>It would be hard to scale this infrastructure becauses one server contains the required components. The server can quickly run out of resources or slow down when it starts receiving a lot of requests.
