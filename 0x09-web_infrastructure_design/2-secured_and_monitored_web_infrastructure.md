# Secured and Monitored Web Infrastructure

![Image of a secured and monitored infrastructure](2-secured_and_monitored_web_infrastructure.jpg)


## Description
A setup for a 3-server web. The data is served via secured and encrypted HTTPS. Monitoring is
also being done.

## Details About This Infrastructure

#### The purpose of the firewalls.
The primary purpose of firewalls is to establish a barrier between a secure internal network and untrusted external networks, such as the internet. Firewalls are essential network security devices that monitor and control incoming and outgoing network traffic based on predetermined security rules. 

#### The purpose of the SSL certificate.
SSL (Secure Sockets Layer) certificates serve the primary purpose of securing the communication between a user's web browser and a website's server. SSL certificates provide encryption and authentication, contributing to a more secure and trustworthy online experience. 

#### The purpose of the monitoring clients.
Monitoring clients, also known as monitoring agents or monitoring software installed on client devices, serve the purpose of collecting and reporting data about the performance, health, and status of those devices. These monitoring clients play a crucial role in overall IT infrastructure monitoring, providing insights into the condition of individual devices and helping to ensure the reliability and efficiency of the entire network. 

## Issues With This Infrastructure

+ Terminating SSL at the load balancer level would leave the traffic between the load balancer and the web servers unencrypted.
+ Having one MySQL server is an issue because it is not scalable and can act as a single point of failure for the web infrastructure.
+ Having servers with all the same components would make the components contend for resources on the server like CPU, Memory, I/O, etc., which can lead to poor performance and also make it difficult to locate the source of the problem. A setup such as this is not easily scalable. 
