# Deploying Desktop background with group policy

- Go to file explorer
- Click on E drive or C
- Create a folder and upload your background image into it
- Right click folder > properties > sharing > advanced sharing > select share this folder > permissions > Remove everyone read permissions > Add authenticated users and click on read 
 permissions > apply

![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/0fcb649f-8536-4579-8373-7de4486c13c4)

  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/e483358f-fe6f-490e-8da8-57971d3bce26)


- go to group policy management
- right click on your domain and select create GPO and link it here
- right click on the newly created GPO and select edit
  
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/759e84ed-2218-4739-b1d3-777fd5093118)

  



- Go to user configurations/Policies/Administrative templates/Desktop/Desktop
- Right click on desktop wallpaper setting and select edit > select enabled

 ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/54d12775-ecfe-4036-a00f-02dfc529dc0e)

 ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/3f4bb25e-83fe-48b3-89e6-b375c7d24f02)


- Go to windows explorer and type in \\ and your servers name

  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/7ff49f30-86e8-476a-8f56-0123337bd151)

- select the fileshare you just created
- Copy the path and paste it into the wallpaper name
- Go back and copy the name of your image
- paste it next to the path you just copied

 ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/62d32231-69d1-48ae-9f1f-0c2f11217e60)

- Apply
- Go to commnand prompt and type in Gpupdate
- Log out and log back in and your wallpaper should be applied




# Setting up a interactive logon message

- Go to group policy management
- Right-click on your domain and create a GPO
- Right click on the GPO and select edit
- Go to policies/windows settings/Security settings/Local policies/Security options
  
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/87992bb6-a10e-4400-aad4-b489d08fc905)
 
- Select the interactive logon message title > check the box > type in your message
  
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/37c4f367-dee7-476c-8e69-0cd3883b5100)

- Select the interactive logon message text > check the box > type in your messsage
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/aba87c5a-865b-4cab-84f3-e70f3b0573fa)

- Go to command prompt and type in gpupdate /force
- restart your computer and you will see the interactive message when you try to logon
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/149fd976-d399-42ef-9adf-b8a1b1cb58fa)

  















# Deploying software with group policy
- Right click on your software select cut
- Go to your data drive and create a folder paste in your software file
- Right click on the folder select properties > sharing > advanced sharing > check the box > permissions > remove everyone > add authenticated users > check name > select read > apply
  
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/0579312a-c5fc-4494-8223-a491cced82e9)
 
- copy the network path
- go to group policy management
- Right-click on your domain and add GPO
- Right click on your GPO and select edit > computer configurations/Policies/software settings/software installation
  
 ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/9781a932-b748-416a-a3b9-50c691d0a675)

- Right click on software installation and select new package
- Type in \\ and your servername \
   ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/b5422f41-de4e-408d-a038-9ee6260a46cb)

- Go to the folder with your software and open
- select assigned
- Go to command prompt type in > gpupdate /force
- type in shutdown -r -t 0 to restart right away

  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/be363f94-a107-4e22-8c84-2a9146113e1a)


- Your software should be installed on all the computers in your domain
  
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/fc16c559-9ad6-4286-b48b-591cef283255)


  



  









# Configuring domain password and account lockout policies

- Go to group policy management
- Right-click on default domain policy select edit. Click on policies/windows settings/security settings/account policies/password policy/
  
- Enforce password history 24 days passwords > Maximum password age 60 days > Minimum password age 0 days > Minimum password length 14 
  characters > enabled > disabled
  
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/8a531410-e1a6-4d5f-9609-4a3a1404dcdf)

- Now go to account lockout policy > account lockout duration 15 minutes > account lockout threshold 3 attempts > 15 minutes
  
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/78354a31-e02d-4dd1-a826-8cfcf5cbbc5e)

- Open cmd and type in gpupdate /force and restart your computer and see if your policy is working
  
  ![image](https://github.com/ali0999109/CreatingGroupPolicy/assets/145396907/650b5894-4929-4950-8efa-c7c0a50e5168)


  
  


























  















