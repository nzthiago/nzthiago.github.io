---
published: false
title: Visual Studio Online: Deploying an ASP.NET Web Pages project from GitHub to Azure Web Apps
layout: post
---
Most articles online cover how to deploy modern ASP.NET applications to Azure from code hosted in Visual Studio Online (VSO) itself. For example:

* [Build and Deploy your ASP.NET 5 Application to an Azure Web App](https://msdn.microsoft.com/en-us/Library/vs/alm/Build/azure/deploy-aspnet5) and
* [Build and deploy your web site to Azure](https://msdn.microsoft.com/en-us/Library/vs/alm/Build/azure/index) 

What if you want to automate the deployment of a classic ASP.NET Web Pages project? There's just a few changes needed to accomplish it that I found worth documenting.

Let's take the great [MiniBlog](https://github.com/madskristensen/miniblog) project created by [Mads](http://madskristensen.net/) as an example. Here are some steps you can follow to use VSO build to automate deploying it all the way from GitHub to an Azure Web App.

Connecting Visual Studio Online to Azure and GitHub 
=============

Register your Azure subscription in VIsual Studio Ooline