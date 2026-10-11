# Introduction to Route 53, Load Balancer and Web Application Firewall

Imagine I am running a popular restaurant. Customer needs to find my restaurant, someone has to seat them in empty available tables, and a guard has to keep troublemakers out. These four services do those jobs for a website.

## Route 53 (The phonebook)

Computers talk using IP addresses like `54.231.10.5`. Humans remember names like `website.com`. **DNS (Domain Name System)** is the internet's phonebook that turns a name into address. Route 53 is AWS’s DNS service. (The “53” is the port number DNS uses.)

When someone types myshop.com, their browser asks Route 53 where that lives. Route 53 answers with the address of my loadbalancer. It can also check whether my servers are healthy and send visitors to a backup region if my main one fails. Server addresses change, but my domain name stays the same. Route 53 keeps pointing the name at the right place.

## Loadbalancer (The receptionist)

Suppose my website is running on one server. If it crashes, the site is down. If 10,000 people arrive at once, it gets overwhelmed. The fix is several servers, plus a load balancer in front that shares visitors between them.

A load balancer also runs health checks, which means it keeps pinging each server asking “are you alive?” If a server stops answering, no more visitors are sent to it. Users never notice a server died.
