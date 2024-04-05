# CI/CD Pipeline Section
## 1. CI/CD Pipeline Environment

The CI/CD pipeline for our semester project operates within the GitHub Actions environment. GitHub Actions provides a seamless and integrated platform for automating workflows directly within our GitHub repositories. The environment is primarily based on GitHub's infrastructure and utilizes virtual machines known as runners to execute workflows. These runners are configured to support various operating systems including Windows, macOS, and Ubuntu, ensuring compatibility with our Flutter app development environment. Additionally, GitHub Actions integrates seamlessly with cloud services, allowing us to leverage cloud resources for testing and deployment processes. Network configurations are managed within GitHub's ecosystem, providing secure and reliable connectivity for our CI/CD pipeline operations.
## 2. CI/CD Pipeline Tools
### GitHub Actions

GitHub Actions was chosen as the primary tool for our CI/CD pipeline due to its tight integration with our GitHub repository and its ease of use. It offers a wide range of features including workflow automation, event-driven triggers, and extensive marketplace integrations for third-party tools and services. GitHub Actions allow us to define our CI/CD workflows using YAML syntax directly within our repository, providing transparency and version control for our automation processes. While GitHub Actions excel in simplicity and integration, they may have limitations in terms of scalability for larger projects.

### Flutter SDK

The Flutter SDK is essential for our CI/CD pipeline as it provides the necessary tools and libraries for building and testing our Flutter applications. By integrating Flutter SDK within our GitHub Actions workflows, we can ensure consistent build environments across different operating systems and streamline the build process for our Flutter app.

## 3. Automation Process
### Workflow Overview

Our CI/CD pipeline automates the build and deployment phases of our Flutter app using GitHub Actions. The workflow, defined in the build.yaml file, encompasses the following steps:

1. **Checkout Repository**: The workflow begins by checking out the latest version of our repository to the GitHub Actions runner.

2. **Setup Flutter Environment**: We configure the Flutter SDK environment using the subosito/flutter-action@v2 action, ensuring that the necessary dependencies are installed for building and testing our Flutter app.

3. **Install Dependencies**: The workflow installs project dependencies using flutter pub get.

4. **Run Tests**: Unit tests are executed using flutter test to ensure code integrity and quality.

5. **Build Application**: The workflow builds the Flutter web app using flutter build web.

6. **Deploy to GitHub Pages**: Upon successful build, the workflow deploys the Flutter web app to GitHub Pages using the peaceiris/actions-gh-pages@v3 action. This step publishes the built web assets to the gh-pages branch, making the app accessible via a public URL.

By implementing this automation process, we aim to streamline our development workflow, enhance code quality, and accelerate the delivery of our Flutter app to end-users.