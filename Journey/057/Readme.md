# Meet8 - Create Bucket & Static Website [Mentor : Yosep Kusuma Wibawa]

## Introduction
For example case scenarios, see the following [Link](https://drive.google.com/file/d/1QRGBj1wR2xjI8yklQo5XciQF_m6r-vTG/view?usp=sharing)

## Cloud Research
## Create Bucket 
- First we search on AWS search, namely S3
- Continue to click S3 and click create bucket
![image](https://user-images.githubusercontent.com/121029600/227812088-0859ec42-a8f4-4db8-aefa-f608650b3555.png)

-	Give the bucket a name and select its AWS Region
![image](https://user-images.githubusercontent.com/121029600/227812132-c418c98f-14d9-40ef-a5dc-484008a55437.png)

-	Uncheck block all public access, so that the bucket is publicly accessible
![image](https://user-images.githubusercontent.com/121029600/227812216-e54db4a9-5e3b-4e5a-8a14-223725725dde.png)

-	Click Create Bucket   
![image](https://user-images.githubusercontent.com/121029600/227812246-f37f7fd7-5909-4a97-9f97-498369a7b9f9.png)

-	Here in the example case scenario, we are instructed to retrieve content from the website [Link](https://github.com/dianazuniarti/aws-s3-testing) and upload it to our bucket
-	Click Bucket 
![image](https://user-images.githubusercontent.com/121029600/227812374-52b997a9-fa25-47bd-8823-e3c0165a0832.png)

-	Click Upload
![image](https://user-images.githubusercontent.com/121029600/227812443-29f8d02c-714b-4b2e-a6b7-53ed25e31497.png)

-	Upload everything needed
![image](https://user-images.githubusercontent.com/121029600/227812486-0d550eee-5be9-4dfb-9eb5-631480ff9c39.png)

-	Scroll down and click Upload
![image](https://user-images.githubusercontent.com/121029600/227812629-f8ea8ff8-7939-4c21-893b-406e74f69bdc.png)

-	Here we give permission so that it can be accessed by public
-	First we go to the permissions tab
![image](https://user-images.githubusercontent.com/121029600/227812971-98dfe41e-dbce-4db1-a4ad-387eff82d8ed.png)

- Then scroll down until there is a Bukcet Policy, click edit
![image](https://user-images.githubusercontent.com/121029600/227812993-e512569e-5917-4d1a-97ba-274ac5660a5b.png)

- Click Policy generator
![image](https://user-images.githubusercontent.com/121029600/227813012-f9397923-741b-46b9-a0a8-072f28d0b3c2.png)

- Type we choose S3 and on the Principal we give the * sign which means for all
![image](https://user-images.githubusercontent.com/121029600/227813091-f2aee599-5194-4963-8042-4bdaa6dd2c2e.png)

- In the Action section select GetObject
![image](https://user-images.githubusercontent.com/121029600/227813127-bbb75bbc-2e07-4aab-bd4a-91127b0de05d.png)

- In this section we copy the ARN and paste it here
![Screenshot_22](https://user-images.githubusercontent.com/121029600/227813303-948345b4-c06d-41c9-870e-f6be95d4974a.png)

![Screenshot_23](https://user-images.githubusercontent.com/121029600/227813434-0a3eac67-503a-4c0f-ae52-42758dfd3aba.png)

- Add /* at the end of the ARN link
![Screenshot_24](https://user-images.githubusercontent.com/121029600/227813466-5041578f-e3f6-4816-80cd-39398e1836d1.png)

- Click Add Statement
![Screenshot_25](https://user-images.githubusercontent.com/121029600/227813570-16dc516e-81c2-418b-8cf1-bb8bbfccfd2c.png)

- Click Generate Policy
![Screenshot_26](https://user-images.githubusercontent.com/121029600/227813600-5989a941-ea72-4634-8dc1-2ce3e214de69.png)

- Copy the JSON!
![Screenshot_27](https://user-images.githubusercontent.com/121029600/227813655-3df9445c-fed9-4f60-a96b-c29baadf646a.png)

- Copy the JSON earlier in this section
![Screenshot_28](https://user-images.githubusercontent.com/121029600/227813679-990e0bfc-b3c2-4bca-97f3-eaf04e4706d5.png)

- Click Save changes
![Screenshot_29](https://user-images.githubusercontent.com/121029600/227813752-b68777ac-1725-4acf-a97a-be0be919499f.png)

## Enable Bucket Versioning
- First, in the Properties section and in the Bucket Versioning section, click edit
![Screenshot_33](https://user-images.githubusercontent.com/121029600/227813878-59bc98d6-9087-40f4-9c6e-a5698b1c1c12.png)

- Select Enable then save changes
![Screenshot_34](https://user-images.githubusercontent.com/121029600/227813911-2a40b94e-df27-4e89-a34b-028c67664e04.png)

- Later it will appear like this
![image](https://user-images.githubusercontent.com/121029600/227814060-7258a76c-4293-492a-9316-f72827d4d7ed.png)

## Create a Static Website
- In the properties section, scroll down until you find Static Website Hosting, and click edit
![Screenshot_36](https://user-images.githubusercontent.com/121029600/227814126-e32eb6db-5798-4639-a3c7-831d4198cebd.png)

![Screenshot_37](https://user-images.githubusercontent.com/121029600/227814146-3023b7b9-f165-441a-9a87-db4666092561.png)

- Adjust to the image below (if you have an error file then add it but if you don't have it don't need to add it, because I have it I will add it)
![image](https://user-images.githubusercontent.com/121029600/227814268-d671ac45-3be6-4885-8598-0b5555a660da.png)

- Click save changes
![Screenshot_40](https://user-images.githubusercontent.com/121029600/227814314-c91a117e-0b2f-4924-be42-ed47d4540f3c.png)

- Copy the link from our static website
![Screenshot_41](https://user-images.githubusercontent.com/121029600/227814359-61ab9388-92f2-4741-9c7b-5defca85a8f3.png)

- Try accessing it, it will be like this, this is the default view of the content that we take, so we have to edit it first according to our portfolio
![Screenshot_42](https://user-images.githubusercontent.com/121029600/227814415-563a0789-4d25-49cb-90f9-9c39d1f95526.png)

- Here I tried to edit and upload again the index.html and others
![Screenshot_48](https://user-images.githubusercontent.com/121029600/227814554-7f41cbde-5bbf-486d-bb42-ac952e65a8c2.png)

![image](https://user-images.githubusercontent.com/121029600/227814707-9d02538b-6f2e-4b45-ab83-7a262a7b4ed4.png)

- And try to access it again, it will change like this, Try clicking Curriculum Vitae
![image](https://user-images.githubusercontent.com/121029600/227814937-b5ebd59f-2c71-45ef-866c-ef83cbc2b570.png)

- And successfully opened
![image](https://user-images.githubusercontent.com/121029600/227814993-778a0289-fed6-4c65-b5f8-9eb74d4d7403.png)

- Then here I try to delete the index.html file so if I access it again an error file like this will appear
![image](https://user-images.githubusercontent.com/121029600/227815060-ff39cfe1-7a15-4743-9a81-a7841403a335.png)


