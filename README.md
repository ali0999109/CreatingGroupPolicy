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


  















