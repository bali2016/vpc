---

copyright:
  years: 2018, 2020
lastupdated: "2020-02-03"

keywords: Virtual Private Cloud, permissions, infrastructure, VPC, SSH key, CLI, API, console, public gateway, floating IP, IP ranges, BYoIP, generation 2, gen 2 

subcollection: vpc


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}
{:download: .download}

# Getting started with Virtual Private Cloud
{: #getting-started}

With {{site.data.keyword.vpc_full}} (VPC), you can use the UI, CLI, and API to quickly provision generation 2 virtual server instances with high network performance.
{:shortdesc}

## Before you begin
{: #prereqs}

1. Set up your account to access VPC. Make sure that your account is [upgraded to a paid account](/docs/account?topic=account-accountfaqs#changeacct){: new_window}. 

2. Make sure that you have a public SSH key, which is used to connect to the virtual server instance. For example, generate an SSH key on your Linux server by running the following command:

    ```
    ssh-keygen -t rsa
    ``` 
    {: pre}

   This command generates two files, `id_rsa` and `id_rsa.pub`. The generated public key is in the `id_rsa.pub` file under an ``.ssh`` directory in your home directory, for example, ``.../.ssh/id_rsa.pub``.

For a complete list of prerequisites for using the API and CLI, see [Setting up your API and CLI environment](/docs/vpc?topic=vpc-set-up-environment).

## Creating and configuring a VPC
{: #create-and-configure-vpc}

To create and configure your VPC and other attached resources:

1. Create a VPC.
2. Create subnets in one or more zones. You can create subnets in suggested prefix ranges or in your own IP ranges that you bring to IBM Cloud.
3. Attach a public gateway if you want to allow all resources in a subnet to communicate with the public internet.
1. Configure an access control list (ACL) to limit the subnet's inbound and outbound traffic.
4. Create generation 2 virtual server instances with the core and RAM configuration that's right for your workload. By default, a 100 GB boot volume is attached to each instance.
5. If you want more storage, create block storage volumes and attach them to your instances.
1. To define the inbound and outbound traffic that's allowed for instances, configure their security groups.
1. If you want instances to be reachable from the internet, reserve and associate floating IP addresses.
5. Deploy your service or applications across the instances.
1. To distribute requests over multiple instances, create a load balancer.
1. To enable your VPC to connect securely to another private network, such as your on-premises network or another VPC, create a virtual private network (VPN).

## Next steps
{: #getting-started-next-steps}

To learn how to create VPC resources, see these tutorials:

* [Using the {{site.data.keyword.cloud_notm}} console to create VPC resources](/docs/vpc?topic=vpc-creating-a-vpc-using-the-ibm-cloud-console)
* [Using the CLI to create VPC resources](/docs/vpc?topic=vpc-creating-a-vpc-using-cli)
* [Using the REST APIs to create VPC resources](/docs/vpc?topic=vpc-creating-a-vpc-using-the-rest-apis)

For a general overview of the VPC infrastructure and related compute, networking and storage concepts, see the following topics:

* [About Virtual Private Cloud](/docs/vpc?topic=vpc-about-vpc#about-vpc)
* [About networking for VPC](/docs/vpc?topic=vpc-about-networking-for-vpc)
* [About instances for VPC](/docs/vpc?topic=vpc-about-advanced-virtual-servers)
* [About storage for VPC](/docs/vpc?topic=vpc-block-storage-about)
