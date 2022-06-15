## Flutter On MAC



To begin with building anything you need to first set up the environment and then only you will be able to build anything for anyone. We will go through various steps in this whole setup process but first you need to know what things are required.

All of this is in the next section.

Note : This setup is strictly designed and structured for mac users. 

## Ingredients

- Flutter Software
- Xcode
- Android Studio
- Vs Code
    - Extensions
        - Flutter
        - Dart
        - Themes (Not Necessary)
        - Error Lens
        - Bloc

## Flutter Software

We will walk through each of the ingredients one by one providing you with the easiest way to setup the whole build.

Starting with `flutter software.`

- Headover to [flutter.dev](http://flutter.dev)
    - Go to the [get started](https://docs.flutter.dev/get-started/install/macos#update-your-path) section and choose the operating system. In our case macOS(Intel or Silicon)
        
        
![arm.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655232888591/B_6ei3zvm.png align="left")

   - After the Download, Extract it anywhere in your system. I recommend you to extract it in your user/Personal(In my case it is my `shashmit` directory, inside a folder( I have given the folder name as `dev`). 
Also you can directly keep the flutter extracted folder in your personal directory as well.
        
![File.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655233626366/FT5KuIUH_.png align="left")

![Screenshot_2022-06-14_at_10.35.17_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655233650945/-5Y-izqIV.png align="center")

- Now, you have to add flutter in your path directory.
  - First Check what shell your terminal is running. By typing `echo $SHELL`, In my case it is Zsh.
  
![Screenshot_2022-06-14_at_10.42.05_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655233934322/a33-XjxOH.png align="left")

After Checking for the shell type `touch .zshrc` in the terminal.
            Go in your Personal Directory Folder and press `cmd + Shift + .` Button. This will enable the hidden files in the directory.

 Locate the `.zshrc file`
![Screenshot_2022-06-14_at_10.47.44_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655233999093/9L2UTL6eb.png align="left")
 Open it and add `export PATH="$PATH:/Users/shashmit/dev/flutter/bin"` . In this instead of my personal directory name and my folder where I have saved the flutter file change it to your own directory and folder name if any.

![Screenshot_2022-06-14_at_10.48.53_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655235046165/nB3aeZhr0.png align="left")
Or just go to the flutter folder and open the bin folder in it. And click on get info

![Screenshot_2022-06-14_at_10.52.00_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655235086261/OPJHBPtCz.png align="left")

 Here, Copy the where section and paste it `export PATH="$PATH:[Your Destination]/bin"` here.

After this one last step open the terminal and refresh the window. By typing `source $HOME/.zshrc` .
            
Now Flutter is added in your path. To check if everything is working, type `Flutter` in your terminal. If Everything is done right the command should run and will show all the commands and functions.


![Screenshot_2022-06-14_at_10.56.10_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655235158251/ztj-SY0Jz.png align="left")


   - You can also go through this video If you are not able to understand or had any problem in setting up the path.
        
       [✂️ To update the path](https://youtube.com/clip/Ugkx38ETHmgkKawEbVMBBvST3uGsXmtfb4zQ)

  ## Xcode
    
    Bravo you have installed flutter in your system, added it in your path. I know few things might have been a little tricky but with all the information and a little bit of tinkering you must have achieved the installation process.
    
    Now, we come to installing the next important thing in this whole process which is Xcode apple code editor. For this you don’t need to go anywhere if you are running MacOS Big sur.
    
    - Go to the app Store and search Xcode.
    - Install it.
    
    After this you need to install a few more things in your xcode.
    
    You need to install some developer friendly tools by typing a few lines in the terminal after installing Xcode.
    
    ```bash
    sudo xcode-select --switch /Applications/Xcode-beta.app
    sudo xcode-select --install
    ```
    

And you are good to go. But you need one more thing in your Xcode which is required by the Flutter System and that is **[CocoaPods](https://guides.cocoapods.org/using/getting-started.html#installation).
CocoaPods manages library dependencies for your Xcode projects.**

To install this you need to open terminal and type 

```bash
sudo gem install cocoapods
```

## Android studio

![download.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234814025/h5-Wj0haN.png align="left")

Hooray We have installed Xcode as well now we only have to finish two more steps and we are done.

- Head over to [Android studio](https://developer.android.com/studio) and click on the Download button. Scroll Down and Accept the agreement and choose the type of chip in your device.

![Screenshot_2022-06-14_at_11.22.29_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234767111/8qS6HzPJX.png align="left")
- Install it on your device, after that open the app.
- Go through all the licences and accept all the agreements and then you will see a screen similar to mine.
![Screenshot_2022-06-14_at_11.25.00_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234679810/uX6lzs9oB.png align="left")
Here, Click on the `More Actions` and then `SDK Manager`
![Screenshot_2022-06-14_at_11.25.32_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234632743/_gzJRN54o.png align="left")
In this Select any given android Version.
![Screenshot_2022-06-14_at_11.26.56_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234567473/Kvr7BbFwV.png align="left")
After this locate to `SDK Tools`
![Screenshot_2022-06-14_at_11.28.09_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234501750/6UfNdxcD_.png align="left")
Here, Select `Android SDK command-line-tools`
![Screenshot_2022-06-14_at_11.28.21_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234480459/Q8tiCRBPA.png align="left")
    
After that click on the `Apply` Button and you are done.
![Screenshot_2022-06-14_at_11.29.27_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234357940/uRbgv2DTf.png align="left")
Now Open Terminal And type `Flutter Doctor` . And if there arises any error in the Command line licence section copy the syntax from the error and paste it in the terminal.

![Screenshot_2022-06-14_at_11.31.58_PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234317956/f3O2F0pmS.png align="left")

And you are good to go for the next step. 

 ## Vs Code 
![vs code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655234183976/FLzWFx7Uz.png align="left")
    
 Finally, you are all set just one more and you are ready to code and build whatever you want to.

- Download [VS code](https://code.visualstudio.com)
- Install it and go to Extensions
![extensions.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1655232999374/5vZEA-AYk.png align="left")

  - [bloc](https://marketplace.visualstudio.com/items?itemName=FelixAngelov.bloc)
  - [Flutter](https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter)
  - [Dart](https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code)
  - [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)

And You have Finally completed all the steps. Now you can create things you want to.
    
Thank you for following the whole process.
    
See you in the next blog related to something new, something that I’m also doing.

Follow me On [Twitter](https://twitter.com/Shaashmit)
       