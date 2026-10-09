# VPC and Networking

## What is AWS region?

**AWS Region** is a real, physical location in the world where amazon has built a cluster of data centers. When we use AWS, we aren't running things in the cloud in some vague senses. Our servers, databases and files live inside actual buildings full of computers, and a Region tells AWS which part of the world those buildings are in. Each region has a name and a code:

<table>
  <tr>
    <th><strong>Region Name</strong></th>
    <th><strong>Code</strong></th>
  </tr>
  <tr>
    <td>Asia Pacific (Mumbai)</td>
    <td>ap-south-1</td>
  </tr>
  <tr>
    <td>Asia Pacific (Hyderabad)</td>
    <td>ap-south-2</td>
  </tr>
  <tr>
    <td>Europe (Ireland)</td>
    <td>eu-west-1</td>
  </tr>
  <tr>
    <td>Europe (London)</td>
    <td>eu-west-2</td>
  </tr>
</table>

Think of a large bank with branches in many cities. Each branch is a self-contained operation with its own vault, staff, and systems. If I open an account at the Mumbai branch, my money sits in Mumbai. The Dublin branch can’t see it unless I deliberately arrange that. AWS works the same way. Each Region is a separate, independent branch. What we create in one Region does not automatically exist in another.

### Why does AWS have multiple regions?

The four main reasons for AWS having multiple regions is because:

1. **Speed (Latency)**: Data travels fast, but distance still matters. If my users are in India and my servers are in US, every request makes a long trip. Putting my application in Mumbai makes it feel faster for Indian users.
2. **Laws and compliance**: Many countries and industries require data to stay within certain borders. A company handling European customer data may need to keep it in Europe. Regions let us choose exactly where our data lives and be confident it stays there. AWS doesn’t move our data out of a Region unless we tell it to.
3. **Resilience**: Floods, power failures, or outages can hit a whole area. Because Regions are isolated from each other, a problem in one Region normally doesn’t affect another. Companies that can’t afford downtime run their systems in two Regions as a safety net.
4. **Availability and Cost**: Not every AWS service launches in every Region at the same time, and prices differ between Regions. The same server can cost different amounts in Mumbai and in N. Virginia.

Each Region contains multiple Availability Zones (AZs), which are separate data center locations within that Region: **Region → Availability Zones → Data centers**

### What is Availability Zone

A Region is not a single building. Inside each Region, AWS builds multiple separate data center locations, and each one is an Availability Zone. Each AZ has its own power, cooling, and networking, so a failure in one is unlikely to take down the others. They sit far enough apart to avoid sharing the same disaster, such as a fire or flood, but close enough to be connected by very fast, low-latency links. The hierarchy is:
> Region → Availability Zones → Data centers

AZs are named by adding a letter to the Region code. In Mumbai you’ll see ap-south-1a, ap-south-1b, and ap-south-1c. Most Regions have three AZs, and some have more.

So inorder to understand why AZ's exist lets head back to our bank analogy. A Region is the city’s branch, and the AZs are separate vaults in different parts of that city. If one vault loses power, the others keep working. If we put our application in one AZ and that AZ has a problem, our application goes down. If you spread it across two or more AZs, the others keep serving users. This is called high availability, and it is the main reason AZs exist.
