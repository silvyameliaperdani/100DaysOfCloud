# Meet11 - Upload Image, Computing, Network, and Alert in EasyStack [Mentor : Dea Tristianti]

## Introduction
In this journey, we will study the services available on EasyStack. EasyStack is a cloud computing service based on OpenStack, and EasyStack provides cloud platform solutions during the current hybrid cloud era in Asia. And at this time we will learn Upload Image, computing, network and alerts

## Cloud Research
- The first step here we will try to upload the Image first
- Go to Service Catalog and click Instance Image

![image](https://user-images.githubusercontent.com/121029600/235563814-6fef5e26-d1dd-4fc9-8eff-ccdc2970ae06.png)

- Then click Create Image

![image](https://user-images.githubusercontent.com/121029600/235563917-4e824f8f-9120-4f79-aac3-84b814192fae.png)

- Give it a name and click Upload File then select ISO, here I'm using Debian 11

![image](https://user-images.githubusercontent.com/121029600/235564345-2747459a-6e6f-41af-8a92-84b2e22b8d7a.png)

- Then select the operating system, CPU, and Hypervisor. Also fill in Minimum Root and Minimum RAM, then click Create

![image](https://user-images.githubusercontent.com/121029600/235565903-25c1ab51-753e-40c3-a097-f75eef362027.png)

- Okay now we enter the Network section, click Service Catalog then click network

![image](https://user-images.githubusercontent.com/121029600/235565062-2d680e57-40d4-4922-b243-a98f7ab111ca.png)

- Click Create Network

![image](https://user-images.githubusercontent.com/121029600/235565961-d9c03d0c-3796-47f5-b992-b505731f6ea8.png)

- Give it a name and IPv4 subnets and click create network

![image](https://user-images.githubusercontent.com/121029600/235568056-f13d212d-fee7-474b-9741-8bc32f08084c.png)

- Then here we will create a subnet, move to the subnet tab then click create subnet

![image](https://user-images.githubusercontent.com/121029600/235567535-c4ba06a5-1011-40c9-9523-47c14c7f5928.png)

- Then select the newly created network

![image](https://user-images.githubusercontent.com/121029600/235567780-dc17fabe-dc23-47c4-8ce3-53d30788cc9e.png)

- Click Advanced Configuration then give DNS Server and give Address Pool Range and click create subnet

![image](https://user-images.githubusercontent.com/121029600/235568214-112cf2cb-62e4-491b-b591-5f57d8f96b19.png)

- Ok, now let's create an Instance, click Service Catalog then select Instance

![image](https://user-images.githubusercontent.com/121029600/235570800-261fcdbf-e8b0-465e-b20c-9d26af0cc3c2.png)

- Click Create Instance 

![image](https://user-images.githubusercontent.com/121029600/235570867-19fa230d-7a7d-4fdc-94b5-91c77cdd725c.png)

- Select the image you want to attach

![image](https://user-images.githubusercontent.com/121029600/235571111-a9ecca7f-6f61-4f3e-ab48-be4d4de21885.png)

![image](https://user-images.githubusercontent.com/121029600/235571220-c1cb3b01-7d89-44c9-9345-bc11823a8159.png)

- Check Delete with Instance, then click network configuration

![image](https://user-images.githubusercontent.com/121029600/235571353-0bfb47f6-b007-4c29-8895-aa130e083e57.png)

- Choose network and klik next

![image](https://user-images.githubusercontent.com/121029600/235571506-dd0c72d9-8abc-4e67-8322-86ad9319073f.png)

- We're going to pair it, so we're going to go back to e service catalog again, then click SSH To Pair

![image](https://user-images.githubusercontent.com/121029600/235571852-99241a61-8f69-4945-adac-49da1db956f0.png)

- Click create key pair

![image](https://user-images.githubusercontent.com/121029600/235571978-99d8a3e6-3569-499c-8545-89277a01c308.png)

- Give it a name then click create

![image](https://user-images.githubusercontent.com/121029600/235572208-44e24c0a-7786-45b1-aedf-ce6467042aec.png)

- Copy public key and save

![image](https://user-images.githubusercontent.com/121029600/235572330-8db8bcc1-cab9-446d-adec-fe11c3e06598.png)

- Enter the key you just created

![image](https://user-images.githubusercontent.com/121029600/235572558-c2560c63-0383-4fb0-abef-bda436c95394.png)

- Check it and click create instance

![image](https://user-images.githubusercontent.com/121029600/235572776-5137763f-e5d5-48e4-b1a7-47509dfa80ce.png)

- And yes it works

![image](https://user-images.githubusercontent.com/121029600/235572911-d9e67247-71d2-49c9-a7da-3d6f954c2d48.png)

- Okay, we'll try alerts, go to the service catalog and select alert management

![image](https://user-images.githubusercontent.com/121029600/235573112-b6e31824-ef66-4633-ae7f-e19d1820f09e.png)

- Click create Alert

![image](https://user-images.githubusercontent.com/121029600/235573168-a42eaad0-094e-4fc8-a373-28bba2aed8b9.png)

- Select the selected instance

![image](https://user-images.githubusercontent.com/121029600/235573483-2898e4c0-197d-4a68-926d-36e689386ec0.png)

- Give it a name and click Automatically fill in the description

![image](https://user-images.githubusercontent.com/121029600/235573644-c2aa058a-2369-41e7-b371-ae603c5b7751.png)

![image](https://user-images.githubusercontent.com/121029600/235573681-1448ac65-090b-41bf-97d5-647bad3c8ac9.png)

- And Done 

![image](https://user-images.githubusercontent.com/121029600/235573786-d44560ea-eaed-4219-9989-f6e494388f05.png)


