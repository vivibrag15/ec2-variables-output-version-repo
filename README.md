provider "aws" {
    region = "us-east-1"
  
}


resource "aws_vpc" "demo-vpc" {
  cidr_block = "10.0.0.0/16"

  tags = {
    Name = "My-vpc"
    
  }

}


variable "region" {
    description = "this is the region"
    default = "us-east-1"
  
}

variable "cblock" {
    default = "10.0.0.0/16"
  
}

output "vpc-id"  {
    value = aws_vpc.demo-vpc.id
  
}# ec2-variables-output-version-repo
