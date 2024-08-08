# Mastering AWS ECS Configuration with Terraform

TODO: Intro
- Explain prerequisites
- Tell the reader what they'll learn
- Tell the reader what we won't cover (maybe)

## Understanding Infrastructure as Code and Terraform

Whether your team is using a platform, a cloud provider, or even on-site hardware, configuring infrastructure is an unavoidable part of building software. Historically, developers and ops professionals have used user-interfaces to configure infrastructure. You can set up and make changes to AWS services using the AWS Management Console, but Infrastructure as Code (IaC) offers a better way.

[Infrastructure as Code](https://aws.amazon.com/what-is/iac/#:~:text=Infrastructure%20as%20code%20(IaC)%20is,%2C%20database%20connections%2C%20and%20storage.) refers to the practice of provisioning and managing infrastructure as text files, compared to using a UI. AWS offer Cloud Formation, its own product to manage AWS infrastructure with JSON and YAML files. While popular, a vendor-specific offering like this introduces some vendor lock-in, so some teams may wish to use a platform-independent IaC tool like Terraform.

[Terraform](https://www.terraform.io/) is a popular Infrastructure as Code tool that lets engineers manage infrastructure across many tools with the same human-readable language. With Terraform, you can provision cloud resources across all the major cloud providers (including AWS!), manage virtual machines, and even configure monitoring tools.

![The Terraform Homepage](./media/terraform-homepage.png)

The reason that Terraform is so popular is that it leans on Providers, which are written in Go and often open source, to interpret Terraform files and make API calls to the correct providers. There are thousands of providers hosted on the Terraform registry, including [a provider for AWS](https://registry.terraform.io/providers/hashicorp/aws/latest)!

## What is AWS Elastic Container Service (ECS)?

Elastic Container Service (ECS) is managed offering from AWS to orchestrate containers. Launching applications on ECS abstracts away the underlying cloud infrastructure, making managing and scaling applications easier.

You can use ECS in conjunction with EC2, another Amazon Web Services offering that lets you directly manage the underlying virtual server. This requires you to manage the EC2 instances themselves, which comes with its own complexity.

Fortunately, ECS also works with [Fargate](https://aws.amazon.com/fargate/), serverless infrastructure made to run containers without the responsibility of managing the virtual server. In this tutorial, we'll use ECS with Fargate as the compute platform for our containers.

## Creating an AWS ECS Cluster with Terraform
TODO:
- Setting up ECS Services with Fargate
- Managing IAM
- Setting up an Nginix Sidecar
- Creating Task Definitions with Terraform

## Configuring Fargate Autoscaling with Terraform
TODO:


## Autoscaling ECS with Queue Time
TODO:
- What queue time is
- Why you may want to autoscale based on queue time
- How Judoscale can help, link to https://judoscale.com/blog/request-queue-time