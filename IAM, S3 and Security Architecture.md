# Introduction to AWS IAM, S3 and Security.

Imagine I just rented a huge office building (my AWS Account). The questions are: who gets a key, which rooms can they enter, where do I keep documents, and how do I stop strangers walking in? IAM, S3 and security answer those four questions.

## 1. IAM (Identity and Access Management)

IAM is AWS’s system for deciding who can do what on which resources. Without it, everyone would log in with one all-powerful account (root account). If that password leaks, the attacker owns everything. IAM lets me give each person or program only the access they need. The four building blocks of IAM:

1. **User**: a specific person or application with its own login. Example: nizam.
2. **Group**: a collection of users that share permissions. Put 10 developers in a Developers group and attach permissions once.
3. **Role**: an identity that is assumed temporarily, not tied to one person. Think of it as a visitor badge that works for a few hours and then expires. AWS services (like EC2) and other accounts use roles.
4. **Policy**: a JSON document that lists the permissions. It is the rulebook attached to users, groups or roles.

A policy looks like this:
```
{
  "Effect": "Allow",
  "Action": "s3:GetObject",
  "Resource": "arn:aws:s3:::my-bucket/*"
}
```
