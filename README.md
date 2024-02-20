## Flutter Web DevContainer using Docker Desktop for VSCode
This project aims to provide a development environment for Flutter Web applications using Docker Desktop and Visual Studio Code's DevContainer feature

# Requirements
[Docker Desktop](https://www.docker.com/products/docker-desktop/)

[Visual Studio Code](https://code.visualstudio.com/download)

# Getting Started
1. **Clone the Repository:** Clone this repository to your local machine.
'''
git clone https://github.com/MasonKramer2002/Project1_Dev_Environment.git
'''
2. Open the folder in VSCODE
   ![ALT TEXT](https://imgur.com/a/ZkRr7vK)
VSCODE will recognize the container and prompt you to open in the container. Once the container is loading it will take a couple of minutes to setup the devcontainer

3. Create a folder of your choosing and run
'''bash
  flutter create directory
'''
4. To run the web server
'''bash
cd directory
flutter run -d web-server
'''

# Issues
1. Depending on your hardware it could take over 10 minutes to open
2. After completing startup terminal may need to clicked to get into devcontainer
3. After restarting errors will be thrown after running flutter run -d web-server, this can resolved by running the command below
   '''bash
  dart pub update
   '''
