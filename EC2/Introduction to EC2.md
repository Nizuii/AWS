# What is EC2?

Imagine I want to host a website to run a program that must be available 24/7. Traditionally I would buy a physical computer (a server), find a room with reliable power, cooling, and internet, and maintain it when it breaks. That costs a lot upfront, and if I guess wrong about how much power I need, I either waste money or run out of capacity.

AWS (Amazon Web Services) solves this by owning huge data centers full of servers around the world and letting me rent pieces of them over the internet. EC2 stands for Elastic Compute Cloud. It is the AWS service that lets me rent virtual computers. In AWS language, each one is called an instance.

- Compute means processing power (CPU and memory), the “brain” of a computer.
- Cloud means you use it over the internet instead of owning it.
- Elastic means you can grow or shrink what you use quickly, in minutes.

An EC2 instance behaves like a normal computer. I choose an operating system (Linux or Windows), log in remotely, install software, and run whatever I want. The only difference is that it lives in an Amazon data center, not on my desk.

**A simple Analogy**: renting a car instead of buying one. I pick the size I need, pay only while I use it, return it when I am done and never worry about maintenance.
