# AWS DevOps engineer evaluation

## Objective

Evaluate your knowledge/experience in two key areas: AWS and Terraform.

## Asumptions

We assume that you have a working AWS account where you can test the infrastructure you're developing. If you don't have a personal account, you can create one and make use of the [AWS free tier](https://aws.amazon.com/free/).

## Topics

- AWS.
- Infrastructure as code (terraform).

## Details

### Terraform

#### AWS Resources

You'll need to create (at least) the following resources:
- A VPC.
- One or more subnets (depending on your design).
- One or more security groups (depending on your design).
- One ELB.
- One or more EC2 (depending on your design)
- Add an EC2 Bootstrap Script for Apache, where you will install apache and echo "Hello Auxis" in index.html file

The following diagram can give you a better idea of what you should code in terraform:

```
                        .───────.                  
                      ,'         `.                
                     ;             :               
                     :   ┌─────┐   ;               
                      ╲  │Users│  ╱                
                       `.└─────┘,'                 
                         `──┬──'                   
                            │                      
                            │                      
    ┌─┬────┬────────────────┼─────────────────────┐
    │ │AWS │                │                     │
    │ └────┘                │                     │
    │     ┌─┬────┬──────────▼──────────────────┐  │
    │     │ │VPC │   ┌──────────┐TCP           │  │
    │     │ └────┘   │  ┌────┐  │80            │  │
    │     │          │  │ELB │  │              │  │
    │     │          └──┴────┴──┘              │  │
    │     │                │                   │  │
    │     │                │                   │  │
    │     │                │                   │  │
    │     │         ┌──────▼───────┐TCP        │  │
    │     │         │┌────────────┐│8080       │  │
    │     │         ││EC2 Instance││           │  │
    │     │         └┴────────────┴┘           │  │
    │     └────────────────────────────────────┘  │
    │                                             │
    └─────────────────────────────────────────────┘
```              

## Deliverables

### Instructions

You must provide instructions to reproduce your infrastructure, it can be a regular README file. 
### Code

You have to ship your code to us, please create a pull request against the upstream repo.

