# my-tools
This is an aggregation point for productivity tools and utilities.

Over the years I found myself being productive only if my development environments were heavily customized and extended with numerous productivity tools that I found now difficult to function without. In many cases there the tools and small utilities developed by me and in other cases by great developers around the world.

Quite a few times I was also asked by my colleagues about those tools when they saw me using them. Thus I decided to stop sending emails full of screenshots and links and create a simple page describing these tools and just refer everyone interested to it. So here we go:

## WinGet / Chocolatey / .NET Tools

Modern Windows learned quite a few tricks from Linux. Thus for the deployment of popular applications, you are much better off using Windows package managers. They are great for bringing the apps to your environment and also for distributing your own products if you are a vendor. I will describe them from these two angles

- **WinGet**
  - Great:
    - Already present on all recent Windows. The most straightforward way of getting the apps on your system.
  - So-so:
    - when upgrading the app it may fail if the app is running
    - For vendors: does not allow creating more than one shim/alias for a package. When publishing on WInGet they scan the packages with WinDefender, which is the champion of giving false positives. Thus the package approval may take a while. 
- **[Chocolatey](https://chocolatey.org)**
  - Great: extremely very well-designed package manager. Can manage the upgrade of the locked (running) applications. Supports multiple shims/aliases per package.
  - So-so:
    - it does not come with Windows you need to install it [from PS](https://chocolatey.org/install)
    - Not available on Linux

- **[.NET Tools](https://nuget.org)**
  - Great: the best option for developers
    - For vendors: since the packages are self-contained the whole cycle of publishing takes only a few minutes.
    - Supports automatic target platform selection for .NET applications
    - Available on Linux
  - So-so:
    - does not allow creating more than one shim/alias for a package.
    - it does not come with Windows you need to install it .NET SDK

## Multiclip

## GC-Menu
https://github.com/oleg-shilo/GC-Menu

## GSudo
https://github.com/gerardog/gsudo/

A much better alternative to Win11 default `sudo`. The closest match of Linux sudo.
- **Great**
  - apart from elevating the command being executed, allows an elevation of the terminal session like on Linux
```txt
winget install gsudo
choco install gsudo
```

## CS-Script
https://github.com/oleg-shilo/cs-script

The most mature and still evolving C# scripting platform available today. The first release was in 2004 when MS was convincing everyone "You do not need scripting. You need compiled apps". 
Allows plain vanilla C# script execution in the terminal (CLI) as well as hosting the script engine in the managed apps. Inspired by Python and mimics practically all Pythoin DevX (package importing, runs on any OS).    
Has an integration with mainstream IDEs and editors.

Installation:

```txt
winget install cs-script
choco install cs-script
dotnet tool install -g cs-script.cli
```

## Search Everything

## QTTabs

## Extending Notepad++

## Extending VSCode

## Extending Sublime Text`

## Greenshoot
