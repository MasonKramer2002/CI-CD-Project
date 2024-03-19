## DevContainer Environment
DevContainer are a self-contained environment that contains all the necessary tools, dependencies, and configuration for software development. The role of a DevContainer is to ensure a consistency across different development environments. This consistency is benefitical for developing flutter due to managing mutliple dependicies. In Flutter, developers manage dependencies such as Flutter SDK, Dart language, Andriod SDK, and plugins. 

## Requirements
[Docker Desktop](https://www.docker.com/products/docker-desktop/)

[Visual Studio Code](https://code.visualstudio.com/download)

## Configuration
![DockerFlutterImage](/docs/images/DockerFlutterLogo.jpg)

For this configuration we will be configuring with vscode and using ubuntu as the base image for the docker container.

### **Clone the Repository:** 
Click ***Clone Git Repository*** on the welcome page as shown below

![VSCODEWELCOM](/docs/images/VSCODE_Welcome_Page.PNG)

Then paste the github link below in the top bar
```
https://github.com/MasonKramer2002/CI-CD-Project.git`

```

Or another option is to open a new terminal by pressing ***CTRL+`*** and inputting the command below. ***Ensure you are in the directory you want to store the project files in before clonning.***


```bash
git clone https://github.com/MasonKramer2002/CI-CD-Project.git
```

### **Extensions:** 
On the left bar there will be a extensions tab indicated by the image below

![ExtensionsLogo](/docs/images/ExtensionsLogo.PNg)

Necessary Extensions
+ Dev Containers
+ Dart
+ Flutter

Recommended Extensions
+ Docker

## Developing in VSCODE

### Opening Dev Container

To open the folder you can either press ***CTRL+K CTRL+0*** or click open folder under the file tab as shown below

![openfolder](/docs/images/VSCODE_Open_Folder.PNG)

Once file exployer opens go to the directory where you cloned the repository to and click the repository folder. Then you will be asked to trust the authors, trusting allows you to change and add files.

### Starting DevContainer
To run the container ensure that Docker Desktop is running in the background

Once Docker Desktop is running in background press ***CTRL + P*** in vscode and type ***Dev Containers: rebuild and reopen in container*** or as shown below

![rebuild](/docs/images/rebuild_DevContainer.PNG)

This will rebuild and launch the DevContainer and the terminal will display the current actions of the DevContainer. This contains changing permissions on boot, once all the permissions are changed there will be a ***Done. Press any key to close the terminal.*** prompt.

### Creating Flutter APP
1. Run flutter create
```
    flutter create myapp
```

2. Enter app directory
```
    cd myapp
```

### Editing Flutter APP
To edit the Flutter app there are main files that need to be changed. These include the pubspec.yaml file and the main file in the lib folder. These files can accsessed via linux terminal or explorer tab on vscode. The explorer tab on vscode allows easy clickable accsess to files and folders.

In order to add dependecies to the app edit the pubspec.yaml file. Adding dependencies to the flutter app allows packages created by other uses to be used. 

```
    nano pubspec.yaml
```

To change the code in the main.dart file navigate out of the pubspec.yaml file with ctrl+x then enter the lib folder.

```
    cd lib
    nano main.dart
```

### Running Flutter web server

To run the Flutter app on a web server navigate to the Flutter app directory in the terminal. This can be done using cd app or if in a subfolder in the flutter app use cd .. to move up a folder. In order to run the web server flutter run will be used.

```
    flutter run -d web-server
```

This will run the flutter app on a web server shown in the terminal. In order to accsess the web server either type in the ip address shown in the terminal or click the link.

## Issues
1. Depending on the hardware launching the DevContainer changing the Flutter permissions might take a while. To ensure that the DevContainer is working click show details while starting the DevContainer and will output all the changes in the terminal

2. After prompted with ***Done. Press any key to close the terminal.*** and hitting any key might not open the bash terminal. In this case just creating a new terminal will fix the issue.

3. After restarting the DevContainer errors will thrown trying to start the web server. This can be resolved by running dart pub upgrade inside the flutter app directory
```
    cd myapp
    dart pub upgrade
```

## Conclusions
In conclusions, DevContainers offer a consistant approach to software development by provising self-contained environments with necessary tools and dependencies. Utilizing VSCODE and Docker Desktop, developers can easily configure and manage DevContainers for Flutter development. Despite the issues such as slow permissions changes, terminal glitches, or out-dated dependicies, DevContainers provide consistant and efficient development for Flutter apps.
