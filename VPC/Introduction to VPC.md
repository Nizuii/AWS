# VPC (Virtual Private Cloud)

VPC is an isolated network inside AWS that means VPC isolates our AWS network from other AWS customer's networks. An AWS VPC consists of subnets, availability zones, routing table and internet gateways.

## Routing Table

Our VPC has many subnets (Think of it like separate floors inside a building). When a computer in one of them sends data, the network has to decide where the data goes. The route table is the rulebook that decides. Each rule says "if the destination is X, send it to Y." A typical route table has 2 rules:

1. **Destination**: the VPC's own address range → "local". Traffic meant for another machine inside your VPC stays inside. AWS adds this rule automatically.
2. **Destination**: Internet Gateway. 0.0.0.0/0 means "everything else, i.e. the whole internet." This rule sends all other traffic out to the internet.

**Purpose**: without a route table, the network wouldn't know where to send anything. It also controls how exposed a subnet is. A subnet whose route table has the internet rule is called a public subnet. A subnet without that rule is a private subnet, so it has no path to the internet at all. This is why route tables matter so much for security. One missing or extra rule changes what the outside world can reach.

## Internet Gateway (IGW)

A VPC is isolated by default, like a building with no doors to the outside world (internet). Nothing goes in or out. The **Internet Gateway** is the main gate that connects our VPC to the public internet. Two things are needed before a server can talk to the internet:

- The IGW is attached to your VPC (the gate exists).
- The subnet's route table has a rule pointing to it (the signboard tells traffic to use the gate).

The server also needs a public IP address, like a house needing a postal address to receive mail. The IGW does the translation between that public address and the server's private one.

**Purpose**: it is the single, controlled doorway between our private network and the internet. Our database servers can sit on streets with no route to this gate, while our web server sits on a street that does have one.

## Availability Zone (AZ)

AWS runs its infrastructure in physical data centers. A Region (for example, Mumbai) is a geographic area, and inside it AWS has several Availability Zones. That means AWS has data centers in the region Mumbai. It doesn't mean AWS have only one data center in Mumbai. AWS have 3 AZ (availability zones) in Mumbai itself. Even if one AZ is down due to natural disaster or power failure the other 2 AZ's will be running. Each AZ is one or more separate data centers with their own power, cooling and networking. They are far enough apart that a fire, flood or power cut in one is unlikely to affect the others, but close enough to be connected by very fast links.
