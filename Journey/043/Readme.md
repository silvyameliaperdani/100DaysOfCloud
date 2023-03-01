# Meet5 - Amazon EC2 [Mentor : Yosep Kusuma Wibawa]

## Introduction
Amazon Elastic Compute Cloud [Amazon EC2] can be said to be a core service, yes, a web service that provides secure and flexible-sized computing capacity in the cloud. Amazon EC2 is designed to make web-scale cloud computing easier for developers. at this time we will create an EC2 instance..

lets gooo !!

## Cloud Research
- Search for EC2 in the search field

![image](https://user-images.githubusercontent.com/121029600/222036361-ee4969c3-b7cf-4fb8-a873-4aa093e995e3.png)
- Then on the EC2 dashboard click on the Launch Instance section
![image](https://user-images.githubusercontent.com/121029600/222042598-081315d7-0cd2-4306-a816-3b015cd01f2f.png)
- After that fill in the name of the instance, and in the Application and OS Images section I select Amazon Linux
![image](https://user-images.githubusercontent.com/121029600/222042928-e6558a4c-43ab-4ad7-97f9-cec87078de9b.png)
- On the instance type I choose t2.micro because it's free hehe
![image](https://user-images.githubusercontent.com/121029600/222042983-ba897052-f16a-4bd5-916b-823698dc2ef1.png)
- And on the key pair, here just click create new key pair
![image](https://user-images.githubusercontent.com/121029600/222043029-f64d3f1a-e25f-4ef8-b050-3e25b385647e.png)
- Here enter the name of the key pair, for the type you can choose RSA and for the private key file format you can choose:
.pem = for OpenSSH
.ppk = for PuTTY
here I use .pem, then click create key pair
![image](https://user-images.githubusercontent.com/121029600/222043114-0b93fec6-bb39-44b4-9864-fffa3844c9df.png)
- In the network settings here we click edit

![image](https://user-images.githubusercontent.com/121029600/222043323-803f0dc6-5888-42e0-8f8b-1f56315c184d.png)
- For my VPC just leave the default and on my subnet select Avaibility Zone: us-east-1a
![image](https://user-images.githubusercontent.com/121029600/222043470-367bd3d9-66fd-46fa-9d50-0ecdbaf0e642.png)
- Here we create a security group, so we can remotely use this web server later using cmd and can be accessed using a web browser
for the ssh security group, it's default, so we just need to add the HTTP security group, just click add security group rule, then add the HTTP protocol.

![image](https://user-images.githubusercontent.com/121029600/222043656-8e424bde-5015-46bc-b01b-29f78a5aa3c1.png)
![image](https://user-images.githubusercontent.com/121029600/222043714-0e0d3ce9-4252-4b22-8559-ebccc1338d41.png)
![image](https://user-images.githubusercontent.com/121029600/222043783-8985a81f-4032-4772-a1ee-3166f65a3958.png)
- If so, in the Configure Storage section here I just leave it as default
![image](https://user-images.githubusercontent.com/121029600/222043847-289ddb5d-9877-4e19-8c55-d8b25ab91d8c.png)
- Click Addtional info (optional) then scroll down until you find Userdata, enter the userdata script as drawn then if you have just clicked launch instance

![image](https://user-images.githubusercontent.com/121029600/222043903-b2501f10-b034-4e73-985d-45df3559bbe8.png)
- SUCCESS !!

![image](https://user-images.githubusercontent.com/121029600/222044002-b3998571-79ef-47d1-8585-e060aa595010.png)
- The instances already exist, yes, the instance that was created earlier, make sure the instance is running and the Status Check has passed 2/2 checks
- For testing here I want to access the web browser, okay, you just have to copy the public IP then access it in the web browser here I tried it on Firefox

![image](https://user-images.githubusercontent.com/121029600/222044112-883fae93-27ba-4a00-8eb0-d2087c57e945.png)
- And it worked

![image](https://user-images.githubusercontent.com/121029600/222044325-563f21c8-bf09-48d4-99ae-048efc68a5dc.png)
- Then here I want to SSH from my Windows CMD, click the instance then click connect

![image](https://user-images.githubusercontent.com/121029600/222044416-ef8d215b-05d3-4854-b9f4-eca5813abe43.png)
- Select the SSH Client tab, copy the example ssh command

![image](https://user-images.githubusercontent.com/121029600/222044509-29f1556e-bf0a-41b5-8e15-45aed0a9a425.png)
- Then go to cmd enter in the directory where the key pair is stored, if you have just pasted the command that was copied earlier, and yeahh the result is successful, we can ssh instance from CMD

![image](https://user-images.githubusercontent.com/121029600/222044574-a6c51f6e-3978-4786-a225-1b5693ffeb50.png)

