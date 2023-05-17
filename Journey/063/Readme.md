# 

## Introduction

✍️ (Why) Explain in one or two sentences why you choose to do this project or cloud topic for your day's study.


## Cloud Research
## Edit Volume
- If you want to change basic volume information, such as name and description, select the volume, then click More and select edit

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/a55c4076-cbb6-41d0-aeeb-2401b17a8913)

- Edit if you click save

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/60a52d22-c7df-4184-a3e8-71ec01507391)

- And yeah succeed

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/7038a3dc-82f9-466c-88d8-4022f8c2c47f)

## Extend Volume 
If the size of a volume in the Available and In use state cannot meet service requirements, you can expand the volume size to larger capacity
- Select the volume and click more then choose extend size

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/4cc4b8bf-60eb-44df-80c2-33a5015331ac)

- Specify the volume size and click Extend

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/711ae727-29d6-4594-856c-752af2d7bff1)

- Click Confirm

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/6a99de66-9d0f-445e-86f0-7f81b3ff8c22)

- You can see that the size has changed

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/06dc5efd-5cb7-442b-a3a3-b3547caa78fc)

## NOTE :
- After expanding the volume capacity, you must log in to the instance and manually modify the file system configuration to make the additional capacity take effect.
- If an expanded volume has not been attached, the capacity expansion takes effect immediately after you attach the disk to a instance
- Because the volume capacity that has been changed cannot be reduced, you are advised to set a proper capacity during expansion
- After expanding an In-use volume, if the boot source kernel version of the instance mounted on the volume is too low, you may not see the additional capacity in instance. In this case, detach the disk and reattach it, or stop theinstance and then start it.

## Create Image Using Volume 
A volume can be used to create an instance image. It is recommended that you create an image in RAW format. This function is usually used by common users to create a required ISO format image in the project
- Select the volume then click more and select create image

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/e05cdf15-0216-4876-819d-29791328358b)

- 
