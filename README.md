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

3. Open the folder in VSCODE
VSCODE will recognize the container and prompt you to open in the container. Once the container is loading it will take a couple of minutes to setup the devcontainer

4. Create a folder of your choosing and run
   
'''
flutter create directory
'''

6. To run the web server

'''
cd directory
flutter run -d web-server
'''

# Issues
1. Depending on your hardware it could take over 10 minutes to open
2. After completing startup terminal may need to clicked to get into devcontainer
3. After restarting errors will be thrown after running flutter run -d web-server, this can resolved by running the command below
'''
dart pub update
'''
