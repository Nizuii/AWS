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

Think of a large bank with branches in many cities. Each branch is a self-contained operation with its own vault, staff, and systems. If I open an account at the Mumbai branch, my money sits in Mumbai. The Dublin branch can’t see it unless I deliberately arrange that.
