---
layout:     post
title:      "Using Surge"
subtitle:   "Deploy a basic web page from your command line"
date:       2016-06-10 12:00:00
author:     "Thacher"
header-img:
categories: basics
---

Steps to deploy a basic web page with surge right from your command line.

This article assumes that you have a basic working knowledge of node and that you know how to use the node package manager (npm).

If you are deploying a simple HTML and CSS web page [surge](https://surge.sh/) is a great (free) option.  

First make sure that all your HTML and CSS files are in a single directory and appropriately linked together. Your main HTML page should be called `index.html`.

From your terminal:

`$ npm install surge -g`

`$ cd yourProjectDirectory`

`$ surge`

This will start the process walking you through the creating an account and launching your first page. Here's surge's sign up gif:
![surgeSignUpGif](https://surge.sh/images/help/getting-started-with-surge.gif)

 Below is my page launch in its entirety:   
![mySurgeLaunch](http://i.imgur.com/haIjt1D.png)

After you make changes to your files, just run `$ surge` again and the new files will be pushed to the page you already set up.

You can even add a custom 404 page -- here's the [specific documentation from surge](https://surge.sh/help/adding-a-custom-404-not-found-page).
