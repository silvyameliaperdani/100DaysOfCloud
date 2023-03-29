

# Meet9 - VPC Hands On [Mentor : Yosep Kusuma Wibawa]

## Cloud Research

# Create VPC & Subnets 
- First on AWS search look for VPC
![image](https://user-images.githubusercontent.com/121029600/228491473-c0ebc9c2-c7fc-4491-875d-f580990c7ad4.png)

- Go to the Your VPCs tab then click create VPC
![image](https://user-images.githubusercontent.com/121029600/228491828-59bfe03e-fc78-4b1d-a4d7-a8da534046e4.png)

- Select VPC Only, give your VPC name, enter IPV4 CIDR
![image](https://user-images.githubusercontent.com/121029600/228492083-2d6a442b-a75b-4751-b700-a90cbb725b6a.png)

- Click Create VPC
![image](https://user-images.githubusercontent.com/121029600/228492295-82ffb50a-3ab6-49da-9807-9f14560156b9.png)

- Go to the Subnets tab then click create subnet
![image](https://user-images.githubusercontent.com/121029600/228492445-720a4517-3abf-49be-bf87-2b94852d49db.png)

- Select the VPC you just created
![image](https://user-images.githubusercontent.com/121029600/228492609-84418100-046e-43b0-a465-6c105c846e18.png)

- Here we will load 2 subnets namely public-subnet and private-subnet
- First we load the public-subnet.. name your subnet, select AZ, and enter the IPV4 CIDR, if so click Add new subnet
![image](https://user-images.githubusercontent.com/121029600/228492777-067a9e0c-f0d9-41f1-8ed6-ded84e201152.png)

- Next, we will create a second subnet, namely a private subnet, name your subnet, select AZ, and enter IPV4 CIDR, and when it's finished, click create subnet
![image](https://user-images.githubusercontent.com/121029600/228494168-972bfd34-dee0-4c35-91ca-9d0258f66a18.png)

- OK, it worked, friends
![image](https://user-images.githubusercontent.com/121029600/228494806-3c7db2ee-1267-435c-a536-0b799fc7707e.png)

# Launch instance
Here we will create 2 instances, provided that the first instance is a public instance and uses a public subnet, while the second private instance uses a private subnet
- Duplicate the tab in the browser, then find EC2 and click on EC2
![image](https://user-images.githubusercontent.com/121029600/228494986-f8bb7f27-9e78-469e-a89a-0acf3e4d4d25.png)

- On the instances tab click Launch Instance
![image](https://user-images.githubusercontent.com/121029600/228495411-f4f217ec-9356-4f23-8ffb-9524c665e0f8.png)

# Public Instance
- Here we will create a public-instance first, name the instance up to you
![image](https://user-images.githubusercontent.com/121029600/228498495-65862c92-a814-46e5-a7dd-6cbe07048065.png)

- In the key pair section, let's make it here first... let's click create new key pair
![image](https://user-images.githubusercontent.com/121029600/228499062-e340b975-4899-4717-b1ad-315978de0ec8.png)

- Give the key pair a name, then my type selects RSA, and the format is .pem , then click Create key pair
![image](https://user-images.githubusercontent.com/121029600/228499601-41d1d418-d954-4373-81d2-65c73d7ab2d2.png)

- Select the Key Pair you just created
![image](https://user-images.githubusercontent.com/121029600/228500054-2eba3e12-191e-4fa6-aed1-a0564cd01724.png)

- In the network section we click edit
![image](https://user-images.githubusercontent.com/121029600/228500188-07daf1ee-a6fb-4770-9e5f-f981c8392bd2.png)

- VPC we select the VPC we just created, then on the subnet we select public-subnet, why do we choose public-subnet because the instance we created now is a public instance
![image](https://user-images.githubusercontent.com/121029600/228500324-5c1ac03d-dda9-42c9-8d06-01ff33a0cdf7.png)
![image](https://user-images.githubusercontent.com/121029600/228500739-47727556-e3e7-429a-bc04-a446b6d11d1d.png)

-See in the image below, that public IP auto-assignment is disabled because we haven't enabled it yet, so we have to enable it first
![image](https://user-images.githubusercontent.com/121029600/228500843-cdc91617-a9de-4d91-9f32-578a9d0aaf70.png)

- We switch to VPC first, select the subnets tab and select Public-subnet then click Action and click Edit subnet settings
![image](https://user-images.githubusercontent.com/121029600/228501353-3cc9895c-4e18-4e42-b75e-df43e203ec8b.png)

- Check/enable auto-assign public IPV4, if you have clicked save
![image](https://user-images.githubusercontent.com/121029600/228501971-2da819c2-f13c-4eaa-b264-0e275f62c615.png)

- Switch to EC2 and refresh the subnet, then automatic assignment will be enabled
![image](https://user-images.githubusercontent.com/121029600/228502353-0def1a27-bb5f-460b-ae45-559d0eb357e6.png)

- Create a new sg, create rules where instances can SSH anywhere, click launch instance
![image](https://user-images.githubusercontent.com/121029600/228502868-481b3654-f145-4c6b-afa3-cdb0da0eccb1.png)

- Refresh until the instance is running, select the instance we just created and click connect
![image](https://user-images.githubusercontent.com/121029600/228503115-71000d72-2fba-41c1-b742-86eda388e5f0.png)

- Copy the example, and paste it in cmd, it can be seen that the instance cannot remote yet
![image](https://user-images.githubusercontent.com/121029600/228506324-3dfb0f70-78a1-4ad1-9b61-e200c8dfecd8.png)

# Create igw & route table
If we want our instance to be able to access the internet and be remote, we must first set the internet gateway and route table

# Internet gateway
- On the VPC open the internet gateway tab, click create internet gateway
![image](https://user-images.githubusercontent.com/121029600/228506616-e5595a29-5a4d-4a7d-862f-7ad1d4cda66b.png)

- Give it a name, it's up to you what name you want to give it, then click Create internet gateway
![image](https://user-images.githubusercontent.com/121029600/228506781-e6adb2dd-4b64-479d-90af-3908080edc9a.png)

- In this section, click Actions, then select Attach to VPC
![image](https://user-images.githubusercontent.com/121029600/228507143-9bee9ae9-09ed-4ef2-997e-ee54ef1956a6.png)

- Select the VPC that we created then click Attach internet gateway
![image](https://user-images.githubusercontent.com/121029600/228508041-083f698f-f977-42af-a7b6-ef9cb49adee4.png)
![image](https://user-images.githubusercontent.com/121029600/228508305-3a2e2956-a756-4e39-9e44-1a1c950f663c.png)

# Route table
- Move to the Route tables tab, then click Create route table
![image](https://user-images.githubusercontent.com/121029600/228508436-91457d56-2e8d-46da-a9dd-97a4943412d7.png)

Here we create 2 route tables, namely public-rt and private-rt
# Public 
- Name and select the VPC that we created then click create route table
![image](https://user-images.githubusercontent.com/121029600/228530340-a34ebfa3-94be-49ad-98d5-2b48d6e9b06e.png)

# Private 
- Name and select the VPC that we created then click create route table
![image](https://user-images.githubusercontent.com/121029600/228530517-28498fb9-47a1-4503-bb69-3864402c847d.png)

# Associate subnets to the route table
- Select public-rt, go to the subnet associations tab and click edit subnet associations
![image](https://user-images.githubusercontent.com/121029600/228530650-532cdfae-ce83-4371-98e2-054550100de5.png)

- Select public-subnet and click save association
![image](https://user-images.githubusercontent.com/121029600/228530776-2b213e5b-f946-4bb0-bf2d-8c76eba64b4d.png)

- Select private-rt, open subnet associations and click edit subnet associations
![image](https://user-images.githubusercontent.com/121029600/228530903-8668062b-061c-48cf-a327-ebda6db094a3.png)

- Select private-subnet and click save association
![image](https://user-images.githubusercontent.com/121029600/228531505-c63e6000-9526-45a0-886e-2b09422b6abc.png)

- Select public-rt, open the route and click edit route
![image](https://user-images.githubusercontent.com/121029600/228531715-f6d566e3-1078-4659-96e6-9bfd0ca3ba2b.png)

- Click add route, enter the IP destination for anywhere, on the internet gateway click target
  ![image](https://user-images.githubusercontent.com/121029600/228540358-a55108c1-08aa-4c2a-8f06-4c86cfca2edc.png)

- Select the internet gateway that was created earlier, then click save changes
![image](https://user-images.githubusercontent.com/121029600/228540737-4d575d02-731f-49bd-8c69-2381e216dc81.png)

# Verify
- SSH into the instance again
![image](https://user-images.githubusercontent.com/121029600/228540882-e00a8bcb-3a8b-4fe2-a03d-5d0cbcd2862f.png)

- Ping google.com, and yeah it worked ttl
![image](https://user-images.githubusercontent.com/121029600/228541273-6f9439a3-c30a-427d-a887-af55abe23606.png)


# Private instances
- On EC2 click Launch instance
![image](https://user-images.githubusercontent.com/121029600/228541407-6674c640-721e-46ad-a9f9-4b6da60adacb.png)

- Name it
![image](https://user-images.githubusercontent.com/121029600/228542435-30c53004-96e8-430b-b8cb-0f16c758f5b9.png)

- In our key pair, create a new keypair, click create new key pair
![image](https://user-images.githubusercontent.com/121029600/228542674-5c234d63-807c-466a-b1ab-6e4e4512033d.png)

- Give it a name and for the type I choose RSA and the format is .pem , if it's already click create key pair
![image](https://user-images.githubusercontent.com/121029600/228542761-2fafdc62-eb6d-4d68-82a3-0bf6f5dcd07c.png)

- Select the key pair that was just created
![image](https://user-images.githubusercontent.com/121029600/228543403-61744c6b-40de-4c09-a73e-5311cd8c74ae.png)

- In the network section, click edit 
![image](https://user-images.githubusercontent.com/121029600/228543732-8ffa7451-88fc-4c7e-87f5-e4539e883f46.png)

- Select the VPC and subnet that we have created
![image](https://user-images.githubusercontent.com/121029600/228543809-b59b7438-a613-4793-99cf-e928b0b79ad3.png)

- Create new sg, select custom and change target for igw from public instance, click launch instance
![image](https://user-images.githubusercontent.com/121029600/228550397-87301b70-601c-4ef4-b16f-dec64ccda46d.png)


# Testing
- Create a key pair file
![image](https://user-images.githubusercontent.com/121029600/228550934-1887fba8-4e3a-44cc-a5b0-b00da8250700.png)

- Unlock your key pair from laptop, and copy then paste in this file
![image](https://user-images.githubusercontent.com/121029600/228552876-a53abb06-5065-4af8-bf6d-2fd3eb61cde8.png)

- Give execute permission to privateinstance.pem and try ssh
![image](https://user-images.githubusercontent.com/121029600/228552970-d08d1352-1c9c-4f1f-978a-ba68b90e1726.png)

- AND YEAH SUCCESS !!!
![image](https://user-images.githubusercontent.com/121029600/228556613-27fbab18-e845-45a8-9676-2856f4dbf7c8.png)







