# tf-nginx-module
TF skills map - 200 Terrafrom sample repo - create code that can be used as module

# Requirements
This repo assumes general knowledge about Terraform for AWS, if not, please get yourself accustomed first by going through [getting started guide](https://learn.hashicorp.com/terraform?track=getting-started#getting-started) . Please also have your AWS credentials prepared in some way, preferably environment variables. See in details here : [Section - Keeping Secrets](https://aws.amazon.com/blogs/apn/terraform-beyond-the-basics-with-aws/)

# Purpose
This repository contains the minimal code or Terrafrom v.0.12 module that provision an **AWS EC2** instance with provisioned **Nginx** web server.

To learn more about the mentioned above tools and technologies -  please check section [Technologies near the end of the README](#technologies)


# Description
A Terraform Module to create 0 or more AWS instances with Nginx web server provisioned on every of them.

## Dependencies 

Module depends on [AWS Provider](https://www.terraform.io/docs/providers/aws/index.html)

## Inputs 
- **ami**  *[String]* -  Amazon EC2 AMI id
- **vpc_security_group_id** *[String]* - [Security Group](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) that should be attached to instance on provision 
- **subnet_id** *[String]* - Amazon [subnet_id](https://docs.aws.amazon.com/vpc/latest/userguide/working-with-vpcs.html#AddaSubnet) where instance should be launched
- **instance_type** *[String]* - AWS [type of the instance](https://aws.amazon.com/ec2/instance-types/) , for example t2.micro , t3.small and etc.

### Optional Inputs
This variable has default value and don't have to be set to use this module. You still may set it to override default value. 
- **max_web_servers** *[String]* - Number of servers to deploy, default value is 3

## Outputs
- **public_dns** *[List]* - array of all DNS names associated with launched instances 
- **public_ips** *[List]* - array of all instances public IPs

## Resources

- Module creates 1 **aws_key_pair** with name **tf200-nginxweb-key**
- Module creates **max_web_servers** instances of **aws_instance** with name **nginxweb**  


# Example usage

For the example usage see the [README.md](examples/README.md) in the examples folder.

# Technologies

1. **To download the content of this repository** you will need **git command-line tools**(recommended) or **Git UI Client**. To install official command-line Git tools please [find here instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for various operating systems. 
2. **This box for virtualization** uses **AWS EC2** - Amazon Elastic Compute Cloud (Amazon EC2 for short) - a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. You can read in details and create a free try-out account if you don't have one here :  [Amazon EC2 main page](https://aws.amazon.com/ec2/) 


# Todo
- [ ] update readme


# Done
- [x] initial readme
- [x] write module code
- [x] create description for inputs/outputs
- [x] create detailed example 
- [x] test example code
