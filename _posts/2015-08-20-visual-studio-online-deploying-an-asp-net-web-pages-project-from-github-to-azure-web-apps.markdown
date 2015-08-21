---
published: false
title: Visual Studio Online: Deploying an ASP.NET Web Pages project from GitHub to Azure Web Apps
layout: post
---
Most articles online cover how to deploy modern ASP.NET applications to Azure from code hosted in Visual Studio Online (VSO) itself. For example:

* [Build and Deploy your ASP.NET 5 Application to an Azure Web App](https://msdn.microsoft.com/en-us/Library/vs/alm/Build/azure/deploy-aspnet5) and
* [Build and deploy your web site to Azure](https://msdn.microsoft.com/en-us/Library/vs/alm/Build/azure/index) 

What if you want to automate the deployment of a classic ASP.NET Web Pages project, and from code hosted on GitHub? This post uses the great [MiniBlog](https://github.com/madskristensen/miniblog) project created by [Mads](http://madskristensen.net/) as an example and automates deploying a fork of it. At the end VSO will be building and deploying it all the way from GitHub to an Azure Web App.

This assumes you already have a [VSO](https://www.visualstudio.com/products/what-is-visual-studio-online-vs) account and permissions to create and run build definitions, and an Azure subscription.

## Connecting Visual Studio Online to Azure

You need your Publish Settings profile file from your Azure subscription. Here's a couple of ways to get to it:

* Log in to [https://manage.windowsazure.com/publishsettings](https://manage.windowsazure.com/publishsettings) with the credentials of your Azure subscription. If you have multiple subscriptions or Azure Active Directory domains associated with the account there will be a drop down for you to choose the right one. A .publishsettings file will be downloaded.
 
* You can also use the [Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/powershell-install-configure/) commands to help get to the download page: ``` PS> Get-AzurePublishSettingsFile ```



## Create Build Definition