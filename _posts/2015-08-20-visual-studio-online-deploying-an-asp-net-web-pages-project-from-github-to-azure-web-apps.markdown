---
published: false
title: Visual Studio Online: Deploying an ASP.NET Web Pages project from GitHub to Azure Web Apps
layout: post
---
Most articles online cover how to deploy modern ASP.NET applications to Azure from code hosted in Visual Studio Online (VSO) itself. For example:

* [Build and Deploy your ASP.NET 5 Application to an Azure Web App](https://msdn.microsoft.com/en-us/Library/vs/alm/Build/azure/deploy-aspnet5) and
* [Build and deploy your web site to Azure](https://msdn.microsoft.com/en-us/Library/vs/alm/Build/azure/index) 

What if you want to automate the deployment of a classic ASP.NET Web Pages project, and from code hosted on GitHub? This post uses the great [MiniBlog](https://github.com/madskristensen/miniblog) project created by [Mads](http://madskristensen.net/) as an example and automates deploying a fork of it. At the end VSO will be building and deploying it all the way from GitHub to an Azure Web App.

This assumes you already have a [VSO](https://www.visualstudio.com/products/what-is-visual-studio-online-vs) account and permissions to create and run build definitions.

## Connecting Visual Studio Online to Azure


Register your Azure subscription in VSO as described in [this](https://msdn.microsoft.com/en-us/Library/vs/alm/Build/azure/deploy-aspnet5) article.
 
## Create Build Definition
