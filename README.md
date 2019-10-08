# tf-nginx-module
TF skills map - 200 Terrafrom sample repo - create code that can be used as module

# Requirements
This repo assumes general knowledge about Terraform for AWS, if not, please get yourself accustomed first by going through [getting started guide](https://learn.hashicorp.com/terraform?track=getting-started#getting-started) . Please also have your AWS credentials prepared in some way, preferably environment variables. See in details here : [Section - Keeping Secrets](https://aws.amazon.com/blogs/apn/terraform-beyond-the-basics-with-aws/)

# Purpose
This repository contains the minimal code or Terrafrom v.0.12 module that provision an **AWS EC2** instance with provisioned **Nginx** web server.

To learn more about the mentioned above tools and technologies -  please check section [Technologies near the end of the README](#technologies)


# Technologies

1. **To download the content of this repository** you will need **git command-line tools**(recommended) or **Git UI Client**. To install official command-line Git tools please [find here instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for various operating systems. 
2. **This box for virtualization** uses **AWS EC2** - Amazon Elastic Compute Cloud (Amazon EC2 for short) - a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. You can read in details and create a free try-out account if you don't have one here :  [Amazon EC2 main page](https://aws.amazon.com/ec2/) 


# Todo
- [ ] wrie module code
- [ ] create description for inputs/outputs
- [ ] create detailed example 
- [ ] test example code
- [ ] update readme


# Done
- [x] initial readme
