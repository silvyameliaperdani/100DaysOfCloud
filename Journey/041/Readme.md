# Meet4 - IAM [ Create User & Group ]

## Introduction
IAM Hands On 

## Cloud Research
We will create a user and group according to the image below : 
![image](https://user-images.githubusercontent.com/121029600/221402604-1c62836d-f8fb-40df-86d8-a29f93541ec4.png)
## Create Groups 
#	Group EC2-monitoring 
- Go to search, find and click on IAM
![image](https://user-images.githubusercontent.com/121029600/221402657-3b482dc0-99b4-4d3b-a566-2dbe25530870.png)
- Click User Groups
![image](https://user-images.githubusercontent.com/121029600/221402677-4a4f5eac-a9e4-467c-a8af-1f067023419a.png)
- Click Create Group 
![image](https://user-images.githubusercontent.com/121029600/221402699-befa1859-fdc6-45c3-87cc-ba9e1dfaf531.png)
- Enter the name of the group you want to create
![image](https://user-images.githubusercontent.com/121029600/221402728-7f6cae99-dc7f-4c43-9600-f92f072a2a31.png)
- Look for the permission you want to attach
![image](https://user-images.githubusercontent.com/121029600/221402776-a2f6fce3-19e9-4d15-b71a-b5c890e7ecba.png)
- Select the permissions you want to attach
![image](https://user-images.githubusercontent.com/121029600/221402816-494a3019-6653-4b1a-8a94-304a1bb3f556.png)
- Click create group
![image](https://user-images.githubusercontent.com/121029600/221402863-214a5083-48b6-4fe7-84b5-1b5cab733404.png)
# Group VPC-monitoring 
- Still in the User Group then click create group, enter the name of the group you want to create
![image](https://user-images.githubusercontent.com/121029600/221403012-31a55582-8052-48e8-a009-23986908df46.png)
- Look for the permission you want to attach
![image](https://user-images.githubusercontent.com/121029600/221403040-6cafbd18-e661-4cfc-91b1-64ce7c025cb9.png)
- Select the permissions you want to attach
![image](https://user-images.githubusercontent.com/121029600/221403062-88579117-317c-4624-8dc6-1a7d13c4beb9.png)
- Click create group
![image](https://user-images.githubusercontent.com/121029600/221403086-556168c6-494f-46fe-b58e-98c875f27fb5.png)
## Create User
# User1
- Click Users and also click add users
![image](https://user-images.githubusercontent.com/121029600/221403136-1b3b7a28-fe68-46ad-862d-3edf5458b9af.png)
- Enter the user name and password you want to create, and click next
![image](https://user-images.githubusercontent.com/121029600/221403163-5c8b9d0c-0e0c-4c42-b9e6-d29bf5c227e3.png)
- Attach permission, here I choose attach policy directly, search for the permissions you want to attach and select the permissions that have been searched for 
![image](https://user-images.githubusercontent.com/121029600/221403217-6777c008-df9e-49b2-91b9-4cdaa00cf062.png)
- Review users that have been created then create
![image](https://user-images.githubusercontent.com/121029600/221403229-9dd57a27-56ad-4bc4-bc0e-411b8ec19411.png)
## Add User to Group
-	Click the user you want to add
![image](https://user-images.githubusercontent.com/121029600/221403277-44c3d324-a12c-4072-b653-cb797d0e4c0d.png)
- Click Tab Groups and click Add user to groups
![image](https://user-images.githubusercontent.com/121029600/221403291-11384c25-17c8-413f-a533-7da20b7be7f9.png)
- Click the group you want and click add user to groups 
![image](https://user-images.githubusercontent.com/121029600/221403325-095a0fba-dcd6-4c45-aa8e-1afedbdc5cdc.png)
# User2
- Click add users
![image](https://user-images.githubusercontent.com/121029600/221403399-4e8de63e-28f8-42f8-8b08-e43440e32813.png)
- Enter the user name and password you want to create, and click next
![image](https://user-images.githubusercontent.com/121029600/221403435-019f419f-9ecd-4ff7-b8d8-47060831a0cc.png)
- In the topology user2 is in the ec2-monitoring group so for the permission options I select add user to group and select the group that you want to attach
![image](https://user-images.githubusercontent.com/121029600/221403541-36a268b5-2405-41e0-9a64-dee5381e7240.png)
- Review users that have been created then create
![image](https://user-images.githubusercontent.com/121029600/221403562-f846afc3-70f4-4ddc-93f0-56752dcdb01b.png)
# User3
- Click add users
![image](https://user-images.githubusercontent.com/121029600/221403593-a75c1253-fc3b-443a-8bc3-315a1899e8e2.png)
- Enter the user name and password you want to create, and click next
![image](https://user-images.githubusercontent.com/121029600/221403616-9d751fa0-621c-4791-b13b-06fdb2086de1.png)
- In the topology user3 enters the ec2-monitoring and vcp-monitoring groups so for the permission options I select add user to group and select the group that you want to attach
![image](https://user-images.githubusercontent.com/121029600/221403700-8492b5ea-4865-48b8-889f-86bdeae9fc4c.png)
 - Review users that have been created then create
![image](https://user-images.githubusercontent.com/121029600/221403738-ede0611b-e8a1-4f75-82fe-c56d8f42d137.png)

