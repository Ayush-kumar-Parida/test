# ciam-tech-demo
A repository to showcase the capabilities the ciam team has built.

Visit Site: https://legendary-adventure-kq9l5z7.pages.github.io/

## Getting Started

1. Install Hugo.
    ```
    brew install hugo
    ```

2. Clone the project repository.
    ```
    git clone https://github.com/Maersk-Global/ciam-tech-demo
    ```

3. Change directory to the project root.
    ```
    cd ciam-tech-demo
    ```

4. Install the Hugo theme.
    ```
    hugo mod get -u hugo-fresh
    hugo mod get -u bulma
    ```

    You can also use it as git submodules for bulma and hugo-fresh. The hugo-fresh config.yaml should point to the local version of bulma

5. Build the project.
    ```
    hugo
    ```

    The 
    ```
    hugo -D option allows us to build markdown pages that are still in draft
    ```

6. The project will be built in the `public` directory.

## Developing

1. Make changes to the project files.

2. To preview the changes, run the following command:
    ```
    hugo serve
    ```

3. The project will be served on http://localhost:1313.

4. To make the changes permanent, commit them to the Git repository.

## Deploying

1. Push the changes to the remote repository.
    ```
    git push origin master
    ```

2. The changes will be deployed to the production environment.


## Creating a publish profile on Azure

To create a publish profile on Azure, you can use the Azure portal or the Azure CLI.

**Using the Azure portal**

1. Go to the Azure portal.
2. Click on App Service.
3. Click on the name of the App Service that you want to deploy your application to.
4. Click on the Deployments tab.
5. Click on the New Deployment button.
6. Select the Azure App Service publish profile option.
7. Click on the Next button.
8. Select the publish profile that you want to use.
9. Click on the Next button.
10. Review the deployment settings.
11. Click on the Deploy button.

**Using the Azure CLI**

1. Install the Azure CLI.
2. Log in to Azure.
3. Create a publish profile.

The following command creates a publish profile for the App Service named `ciam-tech-demo`:

