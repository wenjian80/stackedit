

# 0. Things to remember
1. Open a note pad and jot down the below

> Cloud Tenancy: [Fill in later]

> Cloud username/password: [Fill in later]

> Oracle account username/password: [Fill in later]

> Location of private and public key: [Fill in later]

> Master ip: [Fill in> later]

> Worker ip: [Fill in later]

> Database private ip: [Fill in later]

> Database subnet: [Fill in later] 

> NFS ip: [Fill in later]

# 1. Oracle account

 1. An oracle account need to be created. https://profile.oracle.com/myprofile/account/create-account.jspx
 2. Login to https://container-registry.oracle.com, 
 3. Click on middleware->soasuite and  accept the agreement. You have to see the green tick shown below.
 ![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/registry.JPG)

4. You should have put the "Oracle account username/password" detail in the notepad.

# 2. Oracle cloud account

1.You will be using oracle cloud account for the labs.

2. You use will the Oracle cloud account create 2 compute (1 for master 1 for worker), database, and oracle file system as the nfs.

3. 4. You should have put the "Cloud Tenancy" and  "Cloud username/password" detail in the notepad.

# 3. Create 2 compute, Dbaas and Oracle File system

## 3.1 Login to oracle cloud

1. Login to [http://cloud.oracle.com/](http://cloud.oracle.com/)

2. Enter your cloud tenancy name

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/oracelcloud_1.JPG)

3. Login using your using name and password

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/oracelcloud_2.JPG)

## 3.2 Provision Master Compute

1. Go to Compute -> Instance

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/compute_1.JPG)

2. Click on "Create Instance"

3. Select the name as "soak8master" under "root" compartment

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/compute_2.JPG)

4. Select the shape as "2.4". Select "Create a new virtual Network". Name the vcn as "soak8vcn" under "root" compartment. Name the subnet as "soak8subnet". And "assign a public ip"

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/compute_3.JPG)

5. **PLEASE CLICK ON "Save private key" and "Save public key".** Save your private key name as "private.ppk" and save your public key as "public.pub". You need these key to login to the compute as well as later steps.

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/compute_4.JPG)

6. Click on "compute" and jot down the public ip of your master node.

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/compute5.jpg)

## 3.3 Provision Worker Compute

1. Do the same steps as step 3.2. 

2. Instead of naming as soak8master, name it as "soak8worker"

3. instead of creating a new vcn and subnet, reused the same subnet and vcn created earlier.

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/compute6.JPG)

4. Instead of creating a new private and public key. use back the key you have created previously. Drag and drop your "public.pub" into the public key.

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/compute7.JPG)


## 3.4 Provision Database


## 3.5 Create OFS


## 3.6 Configure network rules


## 3.7 ValidateCheck all information

1. you should have all these in place in your notepad by now. Below is a example of information you should already have jot down.

Below Sample that you shoould have in your notepad.
> Cloud Tenancy: mycloud

> Cloud username/password: abc@gmail.com/welcome1

> Oracle account username/password: xyz@gmail.com/welcome1

> Location of private and public key: c:\mykeys\public.pub c:\mykeys\private.ppk

> Master ip: 158.101.19.11

> Worker ip: 158.102.19.11

> Database private ip: 10.0.0.23

> Database subnet: subnet11251534.vcn11251534.oraclevcn.com

> NFS ip: 10.0.0.4

# 4. Tools
1. [Download Notepad++](https://portableapps.com/apps/development/notepadpp_portable)
2. [Download Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
3. [Download Winscp](https://portableapps.com/apps/internet/winscp_portable)

## 4.1 Putty timeout and ssh key

1. Set the private key for your putty

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/putty_key.JPG)

2. Set the time out for your session

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/putty_timeout.JPG)

3. Login to the server

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/putty_login.JPG)

## 4.2 Winscp timeout and ssh key

1. Click on Advanced->Ssh->Autentication and input your private key

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/winscp_key.JPG)

2. Set the keep alive settings.

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/winscpkeepalive.JPG)

## 4.3 Notepad++ Perferences

1. Set your notepad++ for yaml file perferences.
2. Set yaml files tab to 2 spaces under Setting->Perferences->Langauages
3. Yaml require 2 space, any tab or escape will cause the whole yaml synatax to go haywire.

![enter image description here](https://github.com/wenjian80/soak8_labs/blob/main/img/notepadyaml.jpg)

<!--stackedit_data:
eyJoaXN0b3J5IjpbODkyMzY1NjkxLDg2NDQ2Njc1XX0=
-->