# Meet7 - ELB & ASG [Mentor : Yosep Kusuma Wibawa]

## Cloud Research
## ELB Hands On 
- First, let's create 2 instances.
In the first instance, I gave the name web-server-1 and I chose Amazon Linux for the OS image I chose t2.micro for the Instance Type because it's free hehehe

![image](https://user-images.githubusercontent.com/121029600/224519760-5b8d6e48-e6d6-4465-af7d-7d8435ae509e.png)

![image](https://user-images.githubusercontent.com/121029600/224519765-dea0d6c3-ccaa-4d6a-9381-bf8f4a0abf93.png)

- In the security group, I have created a group that contains http and ssh, so I include the group in my instance
![image](https://user-images.githubusercontent.com/121029600/224519784-347cb499-5d0c-45f4-a6ad-164f3fc2af7d.png)

- On storage I leave the default
![image](https://user-images.githubusercontent.com/121029600/224519798-713b8cbd-e412-4541-8e80-fe6adffcaad7.png)

- In userdata I enter the html script then if it's finished, just launch the instance
![image](https://user-images.githubusercontent.com/121029600/224519810-1cdf310c-165d-4c2a-92d1-9a2cdcc5564c.png)

- Ok, let's create a second instance that I named web-server-2
The OS Image is the same as the previous instance, namely Amazon Linux
![image](https://user-images.githubusercontent.com/121029600/224519831-9d648697-2df0-48d5-bb4f-97b8ccb6ccc7.png)

- For Instance Type, Security group, and storage, I just matched it to the previous instance
- Userdata I fill in the html script then review the instance and if it's already Launch Instance
![image](https://user-images.githubusercontent.com/121029600/224519862-0329fb71-882b-4685-80d4-c359cacaffae.png)

- Now we just have to go to the Load Balancing tab and then create a load balancer
![image](https://user-images.githubusercontent.com/121029600/224519883-7882d19e-1745-4c8f-991d-4ccb0eee957e.png)

- For the type, I select Application Load Balancer then click Create
![image](https://user-images.githubusercontent.com/121029600/224519896-b58fe63b-6b7d-4dc7-acaa-2bbd89467cbe.png)

- I gave the Load Balancer the name ALB-1, in the scheme I chose Internet-facing, and the IP address type I chose ipv4
![image](https://user-images.githubusercontent.com/121029600/224519917-67eb08fd-443d-4ce0-89f5-e499c67c5140.png)

- VPC select according to the instance, and in Mapping I check all existing AZ
![image](https://user-images.githubusercontent.com/121029600/224519934-86445dac-89b5-4f6f-8227-16e20d4ef21c.png)

- I just equate the security group with the instance
![image](https://user-images.githubusercontent.com/121029600/224519961-c56ae81a-2e63-4c9e-9355-b0588ef40183.png)

- And in my listeners and routing create target group
![image](https://user-images.githubusercontent.com/121029600/224519980-afbda973-87be-4b88-937e-aa1351351b22.png)

- I select the target type instance
![image](https://user-images.githubusercontent.com/121029600/224519990-786ac9a2-a734-4856-8b3a-2369d84af5bc.png)

- Target name = TARGET-1
![image](https://user-images.githubusercontent.com/121029600/224520008-af6c0aaf-1203-461a-9fd7-2fdcf3e13c80.png)

- In this section I just leave the default then click next
![image](https://user-images.githubusercontent.com/121029600/224520023-5f077b5e-2c99-4654-b12d-74e54d8e795c.png)

- Select the instance you want to include in the target group then click include as pending below
![image](https://user-images.githubusercontent.com/121029600/224520092-64890896-467c-4819-a4ce-2da00d1d39b2.png)

- If you have click create target group
![image](https://user-images.githubusercontent.com/121029600/224520121-a6221c9f-82cc-4427-a1de-836319208ba7.png)

- Okay, we have succeeded in making the target group
![image](https://user-images.githubusercontent.com/121029600/224520142-85babe55-01d5-4eb1-9dc0-98596d8b09cc.png)

- Go to the load balancing maker tab earlier.. then in this section you refresh later the target group that was just created will appear and select the target
![image](https://user-images.githubusercontent.com/121029600/224520160-249efeb2-e9e7-43c5-b872-33770fa83adf.png)

- If you have checked again whether the summary is correct or not, what if you have just clicked create load balancer
![image](https://user-images.githubusercontent.com/121029600/224520178-55286b1f-4cf2-41a6-8cc5-75022cf8b575.png)

- Click View Load Balancer
![image](https://user-images.githubusercontent.com/121029600/224520211-c18503af-c260-41f2-a10f-448e16de51ff.png)

- Make sure the State is Active, if you haven't just refreshed it okay
![image](https://user-images.githubusercontent.com/121029600/224520231-8c7ca8a2-3196-45ee-b87b-c246a6813fd3.png)

- If it's Active, copy the dns load balancer that was created and then we'll test it
![image](https://user-images.githubusercontent.com/121029600/224520258-0ab1c57a-272b-472f-b943-3e260b045893.png)

- This is the first view
![image](https://user-images.githubusercontent.com/121029600/224520274-294f7f50-10eb-491a-b7dd-984a8030a49d.png)

- Then I refreshed again.. this is the second display
![image](https://user-images.githubusercontent.com/121029600/224520292-4e99e226-c304-46aa-b33c-314e3bfa2e3b.png)

It's according to what we have configured earlier... earlier we configured 2 instances.. well then we load balance these two instances.. and it will be like above... the appearance can be different because we chose the target for the two instances earlier..

## ASG Hands On 
- Go to the Auto Scaling Groups tab, then click Create Auto Scaling Group
![image](https://user-images.githubusercontent.com/121029600/224521320-7aaff799-f78d-4267-bf69-2e39738ecc7a.png)

- I named it ASG-1, on my launch template click create template.. because here I have never made a template
![image](https://user-images.githubusercontent.com/121029600/224521379-52176ff9-86cd-483f-9961-c596f7a0e555.png)

- Here I give the name first-template, I checked the auto scaling guide, yes
![image](https://user-images.githubusercontent.com/121029600/224521401-80ed394d-38c6-4cfd-bb60-1b0883678476.png)

- OS Image I choose Amazon Linux
![image](https://user-images.githubusercontent.com/121029600/224521417-cf292a73-666d-44f4-9156-633e581a47ed.png)

- Instance type I choose t2.micro
![image](https://user-images.githubusercontent.com/121029600/224521445-f4447a04-8cb3-4901-a005-db8c53edd821.png)

- My security group has a security group whose contents are HTTP and SSH, so I select that group
![image](https://user-images.githubusercontent.com/121029600/224521477-05473f05-eb8b-4395-a922-69d3b39b1e33.png)

- I just give userdata an html script then create a launch template
![image](https://user-images.githubusercontent.com/121029600/224521492-8a0d4fcb-b279-4eba-9843-8ad5e2ee2b41.png)

- Return to the page for creating an Auto Scaling Group, in the template section, try refreshing it later, the template that was just created will appear, then select the template
![image](https://user-images.githubusercontent.com/121029600/224521544-c28abefd-846f-41b6-8e4e-887d895a3545.png)

- Click next
![image](https://user-images.githubusercontent.com/121029600/224521570-bdfbd769-4ce3-4303-b6e5-75e8cda8cbc2.png)

- Default VPC only, I select all Avaibility Zone subnets
![image](https://user-images.githubusercontent.com/121029600/224521608-c083ad7d-47f4-453c-9753-13f02bd8ab1e.png)

- Then click next
![image](https://user-images.githubusercontent.com/121029600/224521623-15b11939-8037-48d9-8e80-f3165a21a469.png)

- Select Attach to an existing load balancer, and we choose from your load balancer target groups.. select the target that was created before
![image](https://user-images.githubusercontent.com/121029600/224521633-11310e6a-c9c9-458d-b967-5bc42e7eaff7.png)

- Check the health checks on your ELB, then next
![image](https://user-images.githubusercontent.com/121029600/224521647-c261d0f8-8c19-4fea-95ee-b189389dfc59.png)

- In the group size, I enter Desired capacity 2, the minimum capacity is 1, the maximum capacity is 4, In mutual policies, we just select none then next
![image](https://user-images.githubusercontent.com/121029600/224521665-24f87b4b-9bfd-4b59-838d-534c4f1e890a.png)

- In this next section only
![image](https://user-images.githubusercontent.com/121029600/224521677-e850049e-286b-4f7d-b4b6-fb71f9ce3c43.png)

- This is also next
![image](https://user-images.githubusercontent.com/121029600/224521686-c2ef8d5a-211f-4b1b-a561-cbd87e6bdd6e.png)

- Click create Auto Scaling Group
![image](https://user-images.githubusercontent.com/121029600/224521705-ed8d981d-c299-40fd-acfd-08ad2f8a8052.png)

- If we go to instance, then it will automatically create 2 instances, because we entered the desired capacity earlier, 2
![image](https://user-images.githubusercontent.com/121029600/224521725-f8089657-7f88-4fb1-b7de-ee89861ddde9.png)

- Let's take a look at the ASG... click the activity tab, it will appear like this... everything is successful, OK?
![image](https://user-images.githubusercontent.com/121029600/224521733-fffb8632-1fbc-4323-9be1-198ce704a253.png)

- Experiment here I want to terminate one of the instances that was created automatically earlier ... and we'll see what happens
![image](https://user-images.githubusercontent.com/121029600/224521751-f194a357-3534-4d8f-9113-63b66912a502.png)

- Then there will be 1 instance of lag automatically... how come there's only 1 added? yes, because we enter the desired capacity with 2, so if we delete 1 instance of A, it means that it will add 1 instance
![image](https://user-images.githubusercontent.com/121029600/224521772-72ec44c7-69fa-498e-9afc-9ded17889126.png)
