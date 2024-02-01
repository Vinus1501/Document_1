# **DOCUMENT - 1**


 ![]([RackMultipart20240201-1-xqtf3p_html_f57a01d84ad55459.png](https://community.aws/_next/image?url=https%3A%2F%2Fassets.community.aws%2Fa%2F2YnihCpaNZkmFVuxyHKWrcxDSMT.png%3FimgSize%3D919x516&w=1920&q=75))

**By: Vinus Beniwal**** (Dec. Intern)** |
| --- |

# **CONTENT**

[**What is Amazon EC2? 3**](#_y35s8wph3caz)

[**Instances 5**](#_i27j4xhntcc2)

[Steps to Launch an Instance 5](#_bvrxh7m4qh93)

[**Stop and terminate instances 14**](#_c4ml47a61zuo)

[Stop an instance 14](#_xucylldmbzkw)

[Terminate an instance 14](#_kwk3hevaqe4c)

[**Types of Instances 15**](#_m31zczanyy3d)

[1) General purpose: 15](#_t4utyyuhpqno)

[2) Compute optimized 16](#_kr4vh0ghvmfg)

[3) Memory optimized 16](#_2npdk1hiqqob)

[4) Storage optimized 16](#_bv4rqvf3gc24)

[5) Accelerated computing 16](#_7cl0ishvay98)

[6) High-performance computing (HPC) 17](#_b0uvr5kt70v6)

[**Launch Template 17**](#_fx0hazfzhue)

[**AWS Cloud EC2 Pricing 18**](#_ozv1dnnuw1bl)

[1). Savings Plans 18](#_4ersdew2br5b)

[2). Reserved Instances 18](#_ebu5o6jcbf4h)

[3). Spot Request 19](#_s5626bb41fqv)

[4). Dedicated Hosts 19](#_nf478ah7sm3w)

[**Reference Links 20**](#_xfzkok7akntr)

##
# **What is Amazon EC2?**

- EC2 stands for Elastic Cloud Compute.

- Amazon EC2 is a web service provided by Amazon Web Services (AWS) that enables users to rent virtual servers in the cloud.

- It reduces hardware costs so you can develop and deploy applications faster.

- EC2 instances are essentially virtual machines (VMs) that you can run in the AWS cloud. These instances can be easily scaled up or down based on your computing requirements. It means that you can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage.

- You can launch 20 instances per region.

![](RackMultipart20240201-1-xqtf3p_html_817b7344832fa8a.png)

# **Features of Amazon EC2**

Amazon EC2 provides the following high-level features:

1. Instances

1. Images

1. Elastic Book Store

1. Network and Security

1. Load Balancing

1. Auto Scaling

## ![](RackMultipart20240201-1-xqtf3p_html_d7e5cb69adc7aad2.png)

##
# **Instances**

- You can run multiple virtual machines on a single computer, but when you run virtual machines in the cloud environment, they are known as instances.

##
## **Steps to Launch an Instance**

**Step 1:** Firstly, login to your account.

Then go to the search bar, search for EC2 and click on EC2.

![](RackMultipart20240201-1-xqtf3p_html_b1e7642b6f4a0596.png)

**Step 2:**

After that you will get the interface as shown below. Then, you have to click on the Instance (running) option or simply on Instance option.

![](RackMultipart20240201-1-xqtf3p_html_d68aa48afa828f97.png)

**Step 3** :

On clicking on the instance (running) option, you will get the Launch Instance option on your screen as shown below.

![](RackMultipart20240201-1-xqtf3p_html_eee09093fa6118c3.png)

Then click on the Launch Instance box.

**Step 4** :

After clicking on Launch Instance, you will go to Launch an instance named screen where you have to make your virtual machine.

**a).** You will see the Name and Tags box there, where you have to give the name of your machine you are making.

![](RackMultipart20240201-1-xqtf3p_html_dd5dc19419f85684.png)

**b).** After this you will see the Application and OS Images ( Amazon Machine Image) option, from where you have to select the image of the machine, like you want to make which type of machine ( Amazon Linux, macOS, Ubuntu,Windows,Suse and so on).

![](RackMultipart20240201-1-xqtf3p_html_f84e8fe66f5791e3.png)

**c).** On scrolling down, you will find an option of Instance type, from where you have to select which type of instance you want. t2.micro instance is the one which is freely available but the rest are chargeable. So, it is by default selected.

![](RackMultipart20240201-1-xqtf3p_html_eaea2d6033990e69.png)

**Instance types** comprise varying combinations of CPU, memory, storage, and networking capacity and give you the flexibility to choose the appropriate mix of resources for your applications.

**d).** After this you will see the Key Pair (login) option, from where you have to create a key for your machine.

There will be an option of "Create new key pair" from where you will make the key. After clicking on that option, you have to enter the name of the key you want to give in the "Key pair name" box. After this, you will find the "Key pair type" option, where you have to select the RSA type instead of ED25519 if you have selected the Windows image.

ED25519 keys are not supported for Windows instances on Amazon EC2. This means that if you intend to use key pairs to access Windows-based EC2 instances, you should use RSA key pairs. RSA keys are supported for both Windows and Linux instances on the EC2 platform.

![](RackMultipart20240201-1-xqtf3p_html_15d9259a415f3d7f.png)

After this you will find "Private key file format" from where you have two options .pem and .ppk.

If you choose .pem , then you have to decrypt the password which will be a longer process than .ppk. And .pem

If you choose .ppk, then you will connect the machine without decrypting the key password.

- pem= Privacy Enhanced Mail

- ppk= Process Performance Index

- A key pair is a combination of a public key that is used to encrypt data and a private key that is used to decrypt data.

**e).** On scrolling down, you will find Networking settings, from where you have to modify the network configuration.

![](RackMultipart20240201-1-xqtf3p_html_109370fd9fdf9560.png)

By clicking on "edit" you will get the complete information about the network settings where you have to fill some information.

![](RackMultipart20240201-1-xqtf3p_html_483f0c48a8ebf95e.png)

- Firstly you will find a VPC- required option, which you don't need to modify, keep it default.
- Next you will see a Subnet option, you have to choose a subnet among three or four, which varies only in Availability Zones (1a,1b,1c) for Mumbai Region.

{Subnet= Sub Network}

- Then the third option is Auto-assign public IP. If you want to change the security group rules, then you have to enable it. And if you want your system to assign IP to your machine automatically, then you have to keep it disabled.
- In the next part, Firewall (security group) is there, from where you have to specify whether you want to create your own security group or you want to use an existing security group (default).
- In the next option, the Security group name is there, in which the name is given by default. If you want to change it, then you can.

![](RackMultipart20240201-1-xqtf3p_html_d708aa22e77bfa47.png)

- In the next option, Inbound Security Group Rules option is there, where you find two options, "Type" and "Source Type".

If you are making a Windows machine, then you will find "rdp type" by default and source type "anywhere".

But if you are making any machine other than Windows (like Red Hat or ubuntu), then you find "ssh type" and Source type will remain same i.e. "Anywhere".

- After all these steps, you have to simply click on "Launch Instance".

![](RackMultipart20240201-1-xqtf3p_html_b932ee03f98e5139.png)

This shows your machine is ready.

**Step 5:** Then you simply need to select the created machine and click on connect option.

![](RackMultipart20240201-1-xqtf3p_html_405f3a76260faea5.png)

**Step 6:** Now simply connect the machine by clicking on connect.

![](RackMultipart20240201-1-xqtf3p_html_37951a7f03886640.png)

**Step 7:** Now simply connect to your machine by clicking on "connect".

And you will see the interface of CLI mode as shown below.

The machine shown below is Amazon Linux.

![](RackMultipart20240201-1-xqtf3p_html_1b35da4a4789fe44.png)

##
# **Stop and terminate instances**

You can stop or terminate a running instance at any time.

##
## **Stop an instance**

When an instance is stopped, the instance performs a normal shutdown, and the machine will be stopped. All of its Amazon EBS volumes remain attached, and you can start the instance again at a later time.

##
## **Terminate an instance**

When an instance is terminated, the instance performs a normal shutdown. The root device volume is deleted by default, but any attached Amazon EBS volumes are preserved by default, you have to delete these volumes separately. You can't start the instance again after terminating.

![](RackMultipart20240201-1-xqtf3p_html_1b517d7ddf7d7ab.png)

##
# **Types of Instances**

The types of instances are categorized on the basis of the requirements of services provided by EC2.

## **TYPES**

##

1. General purpose
2. Compute optimized
3. Memory optimized
4. Storage optimized
5. Accelerated computing
6. High-performance computing (HPC) optimized

1.
##
## **General purpose:**

The General Purpose Instance balances computing, memory, and networking resources.

These are cost effective and best in the use where you need less processing.

1.
##
## **Compute optimized**

The Compute Optimized Instances are best when there is a need for high computation.

The main difference is that this type is ideal for high-performance and compute-intensive needs.

1.
##
## **Memory optimized**

This type can deliver large dataset workloads fast.

It loads from storage, holds the data, and processes it before the computer can run it. It requires a lot of RAM.

It is mainly used in applications that need multi-tasking.

1.
##
## **Storage optimized**

This type is best when you have large datasets on local storage and requires a lot of space.

Some examples:

- Large size applications.
- Online transaction systems.

The Storage Optimized Instances are designed to deliver many inputs as fast as possible.

1.
##
## **Accelerated computing**

This type uses hardware accelerators.

The accelerators boost the data processing.

The Accelerated Computing Instances are best for graphics applications and streaming.

1.
##
## **High-performance computing (HPC)**

HPC is technology that uses clusters of powerful processors, working in parallel, to process massive multi-dimensional datasets (big data) and solve complex problems at extremely high speeds.

HPC systems typically perform at speeds more than one million times faster than the fastest commodity desktop, laptop or server systems

##
# **Launch Template**

Imagine you need to create virtual computers in the cloud using Amazon EC2. Instead of configuring each computer manually every time, a launch template allows you to create a blueprint or a template with all the settings you want for your virtual machines.

In the launch template, you decide things like which type of virtual machine you want, what operating system it should use, how much memory and processing power it should have, and so on.

## **Reusability**

## :

Once you've set up your launch template, you can reuse it over and over again. This makes it easy to create multiple virtual machines with the same configurations without having to go through all the settings each time.

##
# **AWS Cloud EC2 Pricing**

1). Savings Plan

2). Reserved Instances

3). Spot Request

4). Dedicated Hosts

##
## **1). Savings Plans**

You can reduce your Amazon EC2 costs by making a commitment to a consistent amount of usage, for a term of 1 or 3 years.

Committing to a period gives a discounted price.

If you increase the budget, the cost goes to normal (on-demand) prices.

##
## **2). Reserved Instances**

You can reduce your Amazon EC2 costs by making a commitment to use a specific instance for specific time. It means that you are reserving the service by giving a commitment.

The Reserved Instances are used to reserve instances for an agreed period.

The options are for 1-year or 3-years. The latter one gives the highest discount.

##
## **3). Spot Request**

A Spot Request is a user's bid for EC2 instances at a specified maximum price per hour.

When you submit a Spot Request, you specify details such as the instance type, the maximum bid price, the number of instances you need, and other specifications.

A Spot Request represents your interest in obtaining capacity at a particular bid price. It's the mechanism through which you express your desire to launch Spot Instances.

##
## **4). Dedicated Hosts**

Dedicated hosts are physical servers fully dedicated to you.

It is given to a particular organization for security purposes who wants to purchase it.

The Dedicated Host is the expensive model.

##


##


##


##


##
# **Reference Links**

- [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html)

- [https://ap-south-1.console.aws.amazon.com/ec2/home?region=ap-south-1#Home](https://ap-south-1.console.aws.amazon.com/ec2/home?region=ap-south-1#Home):

- [https://aws.amazon.com/ec2/instance-types/](https://aws.amazon.com/ec2/instance-types/)

- [https://www.youtube.com/watch?v=k1RI5locZE4](https://www.youtube.com/watch?v=k1RI5locZE4)

- [https://www.w3schools.com/aws/aws\_cloudessentials\_ec2instancetypes.php](https://www.w3schools.com/aws/aws_cloudessentials_ec2instancetypes.php)

17
