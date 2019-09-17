---
title: "Deploy a Spring Boot App using Jenkins and Pulumi"
no_edit_this_page: true
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/mktutorial. -->

<p class="mb-4 flex">
    <a class="flex flex-wrap items-center rounded text-xs text-white bg-blue-600 border-2 border-blue-600 px-2 mr-2 whitespace-no-wrap hover:text-white" style="height: 32px" href="https://github.com/pulumi/examples/tree/master/azure-ts-appservice-springboot" target="_blank">
        <span><i class="fab fa-github pr-2"></i> View Code</span>
    </a>

</p>


This example shows how you can deploy a Spring Boot app to an Azure App Service instance using Pulumi in a Jenkins Pipeline. The Spring Boot app is packaged into a container image that is conveniently built as part of the Pulumi app. The container image is pushed up to a private Azure Container Registry and then used as the source for an App Service instance.

## Prerequisites

1.  [Install Pulumi](https://www.pulumi.com/docs/get-started/install/)
1.  [Configure Azure credentials](https://www.pulumi.com/docs/intro/cloud-providers/azure/setup/)

## Steps

### Step 1: Create a new stack

```
$ cd infrastructure
$ pulumi stack init dev
```

### Step 2: Log in to the Azure CLI

You will be prompted to do this during deployment if you forget this step.

```
$ az login
```

### Step 3: Install NPM dependencies

```
$ npm install
```

### Step 4: Deploy your changes

Run `pulumi up` to preview and deploy changes:

```
$ pulumi up
Previewing changes:
+  pulumi:pulumi:Stack jenkins-tutorial-dev create
+  docker:image:Image spring-boot-greeting-app create
+  azure:core:ResourceGroup jenkins-tutorial-group create
+  azure:containerservice:Registry myacr create
+  azure:appservice:Plan appservice-plan create
+  azure:appservice:AppService spring-boot-greeting-app create
+  pulumi:pulumi:Stack jenkins-tutorial-dev create
...
```

### Step 5: Check the deployed website endpoint

```
$ pulumi stack output appServiceEndpoint
https://azpulumi-as0ef47193.azurewebsites.net

$ curl "$(pulumi stack output appServiceEndpoint)/greeting"
{"id":1, "content": "Hello, World"}
```
