## DevContainer Environment
DevContainer are docker containers that are configured to provide a fully functional development environment that can be rapidly delpoyed.

## Requirements
[Docker Desktop](https://www.docker.com/products/docker-desktop/)

[Visual Studio Code](https://code.visualstudio.com/download)

## Configuration
![DockerFlutterImage](/docs/images/DockerFlutterLogo.jpg)

For this configuration we will be configuring with vscode

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

### Opening Dev Container

To open the folder you can either press ***CTRL+K CTRL+0*** or click open folder under the file tab as shown below

![openfolder](/docs/images/VSCODE_Open_Folder.PNG)

Once file exployer opens go to the directory where you cloned the repository to and click the repository folder. Then you will be asked to trust the authors, trusting allows you to change and add files.

### Starting DevContainer
To run the container ensure that Docker Desktop is running in the background

Once Docker Desktop is running in background press ***CTRL + P*** in vscode and type ***Dev Containers: rebuild and reopen in container*** or as shown below

![rebuild](/docs/images/rebuild_DevContainer.PNG)

This will rebuild and launch the DevContainer

