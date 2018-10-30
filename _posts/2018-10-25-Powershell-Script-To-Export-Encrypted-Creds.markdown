---
layout: post
title: "Powershell Script To Export Encrypted Creds"
date: 2018-10-25 20:26:26 -0500
author: Chuck Lindblom
image: /img/powershell.png

categories:
  - Guides
  - Tech News
tags:
  - Powershell
  - Crednetials
  - Scripts
  - Encrypted
---

{% highlight ruby %}

# Script Name: ExportCreds.ps1
# Written By: Chuck Lindblom
# Updated By:
# Date: 10/25/2018
# Version: 1
# Description: 
# This script will ask the user for a username and password, and store that information in an encrypted .CRED file in C:\Temp
# The credentials can be imported into other scripts by using the following
# $Credential = Import-CliXml -Path **Path to .CRED file**

# Check to see if the Temp Folder exists, if not make it
Write-Host "Checking if directory exists"
If(!(Test-Path "C:\Temp"))
{
    Write-Host "C:\Temp has been created for you"
    New-Item -ItemType Directory -Force -Path "C:\Temp"
}
Else
{
    Write-Host "Directory found! Moving on`n"
}

# Ask the user for the username and password that needs to be exported
$Credential = Get-Credential
$Credential | Export-Clixml -Path "C:\Temp\creds.Cred"

# Output to user
Write-Host "`nCredentails have been stored in C:\Temp"

{% endhighlight %}
