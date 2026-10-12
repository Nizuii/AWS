# Introduction to AWS IAM, S3 and Security.

Imagine I just rented a huge office building (my AWS Account). The questions are: who gets a key, which rooms can they enter, where do I keep documents, and how do I stop strangers walking in? IAM, S3 and security answer those four questions.

## 1. IAM (Identity and Access Management)

IAM is AWS’s system for deciding who can do what on which resources. Without it, everyone would log in with one all-powerful account (root account). If that password leaks, the attacker owns everything. IAM lets me give each person or program only the access they need.
