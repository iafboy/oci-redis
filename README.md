# oci-quickstart-redis
This is a Terraform module that deploys [Redis](https://redis.io) on [Oracle Cloud Infrastructure (OCI)](https://cloud.oracle.com/en_US/cloud-infrastructure). It is developed jointly by Oracle and Redis Labs.

## Prerequisites
First off you'll need to do some pre deploy setup.  That's all detailed [here](https://github.com/oracle/oci-quickstart-prerequisites).

## Clone the module
Now, you'll want a local copy of this repo.  You can make that with the commands:

    git clone https://github.com/oracle/oci-quickstart-redis.git
    cd oci-quickstart-redis/terraform
    ls

## Initialize the deployment

NOTE: By default, a 6 node cluster is deployed. You may change the number of nodes to be deployed by changing the `instance_count` variable in `variables.tf` file. Your cluster should have a minimum of 6 nodes.

We now need to initialize the directory with the module in it.  This makes the module aware of the OCI provider.  You can do this by running:

    terraform init

This gives the following output:

![](./images/terraform-init.png)

## Deploy the module
Now for the main attraction.  Let's make sure the plan looks good:

    terraform plan

That gives:

![](./images/terraform-plan.png)