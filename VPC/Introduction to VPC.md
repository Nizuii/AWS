# VPC (Virtual Private Cloud)

VPC is an isolated network inside AWS that means VPC isolates our AWS network from other AWS customer's networks. An AWS VPC consists of subnets, availability zones, routing table and internet gateways.

## Routing Table

Our VPC has many subnets (Think of it like separate floors inside a building). When a computer in one of them sends data, the network has to decide where the data goes. The route table is the rulebook that decides. Each rule says "if the destination is X, send it to Y." A typical route table has 2 rules:

1. **Destination**: the VPC's own address range → "local". Traffic meant for another machine inside your VPC stays inside. AWS adds this rule automatically.
2. **Destination**: Internet Gateway. 0.0.0.0/0 means "everything else, i.e. the whole internet." This rule sends all other traffic out to the internet.
