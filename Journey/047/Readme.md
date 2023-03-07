# Meet6 - EBS & AMI [Mentor : Yosep Kusuma Wibawa]

## Cloud Research
## EBS ( Elastic Block Store )
- First, here I have prepared 1 instance with the name webserver-1 and with the us-east-1a availability zone

![image](https://user-images.githubusercontent.com/121029600/223319358-6e8444da-05eb-49ca-9763-cdba155a3927.png)
- Then click volume and click create volume

![image](https://user-images.githubusercontent.com/121029600/223319827-f72e5e9d-93fa-47cb-9040-7f096950e66b.png)
- Select the volume type, volume size, and availability zone for the EC2 instance that was created (MUST BE CAREFUL, BECAUSE IT IS VERY IMPORTANT)

![image](https://user-images.githubusercontent.com/121029600/223320521-80d6d45b-9d48-43d8-b5e8-fb41f035e4a0.png)
- And click Create volume 

![image](https://user-images.githubusercontent.com/121029600/223320637-d0fb391c-0132-4a9f-8f06-03f8eb8ba679.png)
- Select the volume that was created, click Action, and click attach volume

![image](https://user-images.githubusercontent.com/121029600/223320909-73405c44-beb1-47c0-ad61-9f2c3ca26426.png)
- Select your instance and click attach volume

![image](https://user-images.githubusercontent.com/121029600/223321161-9cdf8713-f3a7-4b4c-9e22-a8c3a07599d1.png)
- Okay we managed to attach the volume

![image](https://user-images.githubusercontent.com/121029600/223321423-6a716d05-88fd-4e80-8874-6fddce2d6505.png)
- Look at the storage instance, and up there is already the volume that we have attached

![image](https://user-images.githubusercontent.com/121029600/223321861-d0189011-d09c-4799-a6c3-fff53abdb8b2.png)
- Next here we create another instance with the name webserver-2

![image](https://user-images.githubusercontent.com/121029600/223322199-0b288b71-f8a1-4984-bbfa-5e92ce466682.png)
- And on the subnet, choose a different availability zone, so on the webserver-1 instance I chose us-east-1a, then on the webserver2 instance here I chose us-east-1b, then click launch instance

![image](https://user-images.githubusercontent.com/121029600/223322451-ad283984-0b40-437c-8596-ad6d070dc753.png)
- If you have checked the Availability Zone again, here it is correct... I chose us-east-1b earlier

![image](https://user-images.githubusercontent.com/121029600/223323012-52aa06ed-6abe-4df0-92fd-363307c811a3.png)
- Go to volume and detach the previously attached volume

![image](https://user-images.githubusercontent.com/121029600/223323595-c45faa66-7a4f-4553-9cac-fe1c403abe0b.png)
- If so, select the volume that was detached earlier and click Action, then select create snapshot

![image](https://user-images.githubusercontent.com/121029600/223323943-ab3319a9-afe2-41de-99ba-e7d144ae95c2.png)
- Fill in the desctiptoin, it's up to you, then click create snapshot

![image](https://user-images.githubusercontent.com/121029600/223324247-618c5b54-34d6-412c-afa5-2e0fcfd71f81.png)
- Go to the Snapshots tab, then select the snapshot that was created earlier, click Action and click Create volume from snapshot

![image](https://user-images.githubusercontent.com/121029600/223324595-9521fb2b-794a-4ee3-9f39-8f177a12edd6.png)
- Select the availability zone [same as the instance we just created, i.e. us-east-1b] then, click Create volume 

![image](https://user-images.githubusercontent.com/121029600/223324876-2e72e1bd-019a-49bd-8252-375e30d9c99d.png)
- Okey, already done yes

![image](https://user-images.githubusercontent.com/121029600/223325255-0c9d210a-88c1-4bac-9c49-76edae52cab1.png)
- Select the volume you just created then click action and click attach volume

![image](https://user-images.githubusercontent.com/121029600/223325529-6178cfa6-49a6-4489-a091-e4a8e6adbac6.png)
- Select the instance then click attach volume

![image](https://user-images.githubusercontent.com/121029600/223325660-8df66cfd-f198-458a-bba9-218ee13e3e95.png)
- Okay, it worked

![image](https://user-images.githubusercontent.com/121029600/223325751-6f3b59f8-73ce-41d2-b4ee-f14d8a8cb32e.png)

![image](https://user-images.githubusercontent.com/121029600/223325823-e0b43af9-8024-4b20-bcd0-021da7e1d474.png)

## AMI ( Amazon Machine Image )
- First Create a new Instance and also in security group Allow traffic from http (or use your security group in same rules)
![image](https://user-images.githubusercontent.com/121029600/223326213-474f86ce-fd7c-4c94-a07e-57bab6600591.png)
![image](https://user-images.githubusercontent.com/121029600/223326240-947828a0-5331-46d6-8940-ccb2f0a2ce9b.png)

- In your user data, use the script to start your web server application and click launch instance
![image](https://user-images.githubusercontent.com/121029600/223326576-cdd8f4eb-f275-488c-8aef-c9c840797155.png)

- Once done, copy your instance's public ip and paste it in your browser to confirm 
![image](https://user-images.githubusercontent.com/121029600/223326771-45f37f86-5376-452a-a7fc-3129f66f0430.png)

- Then it will look like this
![image](https://user-images.githubusercontent.com/121029600/223326878-1cc2cbd0-ea93-4377-b914-7b061e817a0c.png)

- Select your instance, click Action and select an image and template, click Create Image
![image](https://user-images.githubusercontent.com/121029600/223327115-db965006-8786-4378-b132-c006a65ea7bd.png)

- Enter name for image & click create image
![image](https://user-images.githubusercontent.com/121029600/223327245-497d675d-2943-4670-b782-313c3501b8d6.png)

![image](https://user-images.githubusercontent.com/121029600/223327280-76862b5f-eba0-4f46-bbcb-5f3a3ad2cb2c.png)

- Go to AMIs, select the AMI that was created earlier, then click Launch instance from AMI
![image](https://user-images.githubusercontent.com/121029600/223327680-3721365e-5caa-42a0-989d-134be2599b2f.png)

- In application and OS images, they will be addressed by default in your AMI
![image](https://user-images.githubusercontent.com/121029600/223328078-9f715264-3a42-4e8e-b41f-48acbe78ebec.png)

- Select your security group to allow http traffic
![image](https://user-images.githubusercontent.com/121029600/223328234-d7c9a598-10b8-4909-8a50-fc9ffa742c18.png)

-On user data, Add script to create html file & click launch instance
![image](https://user-images.githubusercontent.com/121029600/223328481-03068ad2-fc07-4df2-8ed0-4dcbdc8aea3b.png)

- Copy your Instance public IP and paste it in your browser
![image](https://user-images.githubusercontent.com/121029600/223328958-41224119-c1f0-4123-b6c9-a40acf424468.png)

Yeayyy done !!! 
