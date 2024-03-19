# Source Code Version Control Tools

## Introduction
Version Control is used in software development by securing the integrity, histroy, and collaboration of a project. It serves as a safety net against loss of data by tracking changes changes made to a repository. Through version control systems like Git developers can maintain a record of changes and enable identification of changes. The historical part of version control helps in debugging, rollbacks for a project compliance. Version control allows multiple team members to work on different branches and merging code. 

## Version Control System Used
For this project, Git was chosen as the version control system (VCS) due to its popularity, robust features, and excellent support for distributed development. Git's branching and merging capabilities, speed, and flexibility make it ideal for managing code changes effectively. 

## Repository Setup
- **Structure**: The repository follows a branching strategy with two main branches: `main` and `devEnv`. The `main` branch contains stable code for production, while the `devEnv` branch is used for development and integration of new features.
- **Integration**: The repository is integrated with a DevContainer for developing Flutter apps. It ensures a consistent development environment across team members. Additionally, GitHub Actions are utilized via workflows for CI/CD pipeline automation. GitHub Actions are used to build the app and deploy it when changes are pushed or pull request to the `main` branch.
- **Standards**: Commit messages follow a standardized format (e.g., `<type>: <description>`), and branch naming conventions are adopted to reflect the purpose of the branch (e.g., feature/<feature-name>, bugfix/<issue-number>).

## Common Commands and Usage
- **Git Commands**:
    - `git add <file>`: Add changes to the staging area.
    - `git commit -m "<message>"`: Commit staged changes with a descriptive message.
    - `git checkout <branch>`: Switch to a different branch.
    - `git merge <branch>`: Merge changes from a specified branch into the current branch.
    - `git push <remote> <branch>`: Push commits to a remote repository.
    - `git pull <remote> <branch>`: Fetch and merge changes from a remote repository into the current branch.
- **VSCode Version Control Tab**:
    - The VSCode version control tab provides a user-friendly interface to perform common Git operations directly within the code editor.
    - It allows users to stage changes, commit them with a message, switch between branches, and push/pull changes from remote repositories.
    - The integrated interface streamlines version control tasks and enhances developer productivity within the development environment.


## Collaboration Features
Git facilitates collaboration through various features:
- **Pull Requests**: Team members can propose changes, review code, and discuss modifications before merging them into the main codebase.
- **Code Reviews**: Peer reviews ensure code quality, identify potential issues, and share knowledge among team members.
- **Conflict Resolution**: Git provides tools to resolve conflicts that arise when merging branches with conflicting changes.

## Challenges and Solutions
One challenge encountered was setting up github actions via workflow build.yaml file. To fix this issue, the permissions of the repository needed to be changed, aswell as changing the branch and version getting installed. These fix's allow for github actions to take place whenever a pull request or push on main happens to ensure the code is working properly.

## Conclusion
The adoption of Git for version control in this project has provided numerous benefits, including efficient collaboration, robust history tracking, and streamlined development workflows. Integrating Git with GitHub and DevContainer has enhanced productivity and code quality, enabling seamless development and deployment of Flutter apps. With GitHub Actions automating the build and deployment process, the development team can focus more on coding and less on manual tasks, further improving the project's efficiency.