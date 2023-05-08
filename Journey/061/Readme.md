# Create Instance, Floating IP and Alert in EasyStack [ Mentor : Dea Tristianti ]

## Introduction
On this journey, we will learn to create floating IPs on the instances we have created, and later we will also alert them

## Cloud Research

## Create Network
- The first click Service Catalog then search for network then click

![image](https://user-images.githubusercontent.com/121029600/236716569-8cdb81c4-af38-4491-8feb-1603dc032394.png)

- Click Create Network

![image](https://user-images.githubusercontent.com/121029600/236716638-48b12b38-4acc-42a8-ae2d-ea57fdd2bc71.png)

- Name it

![image](https://user-images.githubusercontent.com/121029600/236716724-8edcb633-e7bd-49ce-b5d6-828805d3fdd4.png)

- Specify the IP Network, DNS Server and also fill in the Address Range then click create network

![image](https://user-images.githubusercontent.com/121029600/236717093-f8abef04-de82-47de-9b43-fd35e650bb1c.png)

- OK, it's done

![image](https://user-images.githubusercontent.com/121029600/236717237-f0f62a0f-01ba-4b3f-8835-233769ad93a5.png)

# SSH Key-Pair
- First look for the SSH To Pair service in the service catalog

![image](https://user-images.githubusercontent.com/121029600/236717645-9e9b9728-4e4b-4cb8-883b-85e47d8dbf03.png)

- Click create key pair

![image](https://user-images.githubusercontent.com/121029600/236717710-dbeb5c76-0d03-45a6-abb9-2b1c08fe97fd.png)

- Name it

![image](https://user-images.githubusercontent.com/121029600/236717769-2748b73d-c687-4941-9a99-f878be8017e6.png)

- Copy the private key and paste it into notepad then save it

![image](https://user-images.githubusercontent.com/121029600/236717812-52d2c6bc-34c7-4b63-90fd-eb9ed45b2f84.png)

# Create Instance 
- Click Service catalog and look for the instance then click it

![image](https://user-images.githubusercontent.com/121029600/236721864-b4189c27-26b3-40e7-9012-4a64c5f6d363.png)

- Click create instance

![image](https://user-images.githubusercontent.com/121029600/236722129-da92b64f-aa29-492f-870f-0c209e096f5e.png)

- Select the image

![image](https://user-images.githubusercontent.com/121029600/236722423-bd84d299-694b-40bf-a6f1-a35975cb4c68.png)

- Flavor too

![image](https://user-images.githubusercontent.com/121029600/236722545-c76da26c-3a1a-4f0b-973f-a4c3b50f3b16.png)

- Check delete with instance then click Next:Network Configuration

![image](https://user-images.githubusercontent.com/121029600/236722641-b0d2c813-d96d-49a1-ad82-ab3c712a76a7.png)

- Select the network you just created

![image](https://user-images.githubusercontent.com/121029600/236722704-61140904-b1b0-4f81-bfed-0de042d33976.png)

- Name the instance then enter the keypair you just created, click confirm

![image](https://user-images.githubusercontent.com/121029600/236722768-8c5dbc53-4a72-4be3-a4fa-1e4ef0a58bc9.png)

- Review then click create instance

![image](https://user-images.githubusercontent.com/121029600/236722833-48643ab3-a44e-47c8-9dbc-d4125a9c0ff5.png)

- It's work

![image](https://user-images.githubusercontent.com/121029600/236722987-60922fb7-5acb-4baf-8f78-f5c6df3208f7.png)

## Floating IP 
Okay, here we will create a floating IP, the goal is for us to get the internet and also a public IP
- First click service router

![image](https://user-images.githubusercontent.com/121029600/236726015-c1f844c5-c9be-40d0-9319-bcb162e5992b.png)

- Click the router that is already available

![image](https://user-images.githubusercontent.com/121029600/236726068-9f74bfca-a361-4487-98ea-3f82e89c249c.png)

- Click connect subnets

![image](https://user-images.githubusercontent.com/121029600/236726234-70f9f0f0-4f2a-4e75-b8bb-7c7d6562528f.png)

- Select the network subnet that we created earlier

![image](https://user-images.githubusercontent.com/121029600/236726300-271cf3f4-018a-4921-b567-7324a068a6e1.png)

- Click connect

![image](https://user-images.githubusercontent.com/121029600/236726400-2d5b758b-5d23-4159-9536-2bae941cc328.png)

- Move on the Floating IP tab then click Apply for IP To project

![image](https://user-images.githubusercontent.com/121029600/236726462-753ab65f-3536-403f-8466-5e74c9a06774.png)

- Set the bandwidth then click allocate

![image](https://user-images.githubusercontent.com/121029600/236726526-677bf6a7-a0fb-4826-8de4-440062e96460.png)

- OK it worked

![image](https://user-images.githubusercontent.com/121029600/236726578-f2934691-9275-459c-9c02-cf1be30fe567.png)

Then we attach the floating IP to the instance
- Click check the IP that was created, then click more and select Associate to vNIC

![image](https://user-images.githubusercontent.com/121029600/236726683-4fe6345b-828b-4e20-9263-e8ddf0b4647f.png)

- Resource select our instance vNIC also then Associate

![image](https://user-images.githubusercontent.com/121029600/236726761-e1498290-d28a-4091-a221-05347f283d29.png)

- Succeed !!

![image](https://user-images.githubusercontent.com/121029600/236726815-2eee6260-15ca-4c77-80e2-0e646e38e1a9.png)

![image](https://user-images.githubusercontent.com/121029600/236726867-30997d9a-0b1f-4677-8935-601e19c04ac3.png)

- We go to PuTTY-gen, yeah... to change the private key file where we pasted it into notepad and it will become .txt, so we change it to .ppk with putty

![image](https://user-images.githubusercontent.com/121029600/236726898-5a166ad1-74ac-452b-ae46-0aeb55e976c6.png)

- Click Generate

![image](https://user-images.githubusercontent.com/121029600/236726948-24d9d803-4af8-4004-bbd3-06a8cf9a3e7e.png)

- On the Conversions tab, click Import key

![image](https://user-images.githubusercontent.com/121029600/236727014-ceb9a3cd-3812-447b-a0aa-a6d968231b19.png)

- Select the file we created to store the private key earlier

![image](https://user-images.githubusercontent.com/121029600/236727078-c1f0588f-b6f6-497b-8750-464676f45b25.png)

- Click Save private key

![image](https://user-images.githubusercontent.com/121029600/236727169-af84104a-96e8-4a3b-9b8b-0e01aac4a35b.png)

- Click yes

![image](https://user-images.githubusercontent.com/121029600/236727213-8ebb18d6-84b6-4cdd-af94-037144481b20.png)

- Click save

![image](https://user-images.githubusercontent.com/121029600/236727263-ca0e1e17-2b13-4b52-8e83-257e187ac314.png)

- Open PuTTY

![image](https://user-images.githubusercontent.com/121029600/236727331-b0223600-9c84-4b26-a587-c9873cb54636.png)

- Click SSH - Auth - Credentials and click Browser

![image](https://user-images.githubusercontent.com/121029600/236727363-8eb78845-e462-4dd5-9dd9-74cc9884bf26.png)

- Select the file you just created to be .ppk

![image](https://user-images.githubusercontent.com/121029600/236727413-3e61cdac-c74c-44b6-b439-db7478306d6a.png)

- Enter the Public IP of the instance, click open

![image](https://user-images.githubusercontent.com/121029600/236727477-e15c5a25-c2e1-44be-b474-612988a7becb.png)

- Click Accept 

![image](https://user-images.githubusercontent.com/121029600/236727601-452fff2f-2225-496a-8eda-122fc088b582.png)

- Login using root and yeahhh it worked

![image](https://user-images.githubusercontent.com/121029600/236727680-e85e4c56-086b-4a99-976b-13949dac8747.png)

- 











