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
https://github.com/oleg-shilo/multiclip

Yet another clipboard manager.
What sets it apart is that it is tailored to the programmers. It mimics an IDE autocompletion experience. While all clipboard managers aim to allow the user  to analyze the history and have an intensive "clicking" experience, Multiclip simply pops up (while you are typing) the frameless list of the suggestions from the clipboard history and pastes the suggestion you accept. It works globally on whole Windows. Supports all clipboard formats (images, files, HTML...). Persists history between desktop sessions, encrypts the history content, and allows preview of the suggestion before pasting it.

```txt
winget install multiclip
choco install multiclip
```

## GC-Menu (Global Context-Menu)
https://github.com/oleg-shilo/GC-Menu

It's a logical equivalent of "canned responses" available with some tools that allow using templates everywhere and for everything. 
It allows users to create any sort of content that can be inserted as input in any application.
My recent experience with Jira only confirmed how useful this tool can be. Thus Jira does not allow using templates for comments. It suggests using an expensive 'canned response' plugin. GC-Menu gives a very elegant answer to the problem.

![capture3](https://github.com/user-attachments/assets/51fea672-c534-46d8-9b4b-eeaa5fe84cae)

You can use it to insert signatures in our email or a hard-to-remember git command in the terminal.

```txt
winget install gc-menu
choco install gc-menu
```
 
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

```txt
winget install cs-script
choco install cs-script
dotnet tool install -g cs-script.cli
```

## Search Everything
https://www.voidtools.com/

This little beauty is a real gem. It is everything that the File System search tool should be. 
The tool uses FS events to keep an accurate index of ALL files on your system. Because it avoids silly Windos scheduled indexing, it does not take any CPU resources to maintain the index database. The result is spectacular. ANY file on your system can be found within milliseconds, regardless of where it is. Even Linux, which cannot compete as it is slower, can only find the files that are in PATH or in well-known locations.
Ironically Linux had a somewhat similar product "Bingle Search", which is no longer developed/maintained.

```txt
winget install everything
choco install everything
```

## QTTabs
http://qttabbar.wikidot.com/

This is another Windows gem that is hard to work without after discovering it. It creates a Tabified experience that eats Win11 tabbed explorer on breakfast. Interestingly enough it was available ~10 years before the Windows team decided to accept the user demand and implemented a sad version of the concept. The tool is much more than just tabs. It allows you to create a custom toolbar with the commands to be executed against the selection. 

The tool uses a very clever approach of injecting itself in the Windows native explorer, without impacting the major UX or performance.
![image](https://github.com/user-attachments/assets/53137296-2fad-4e47-b7e0-0cb309f4000e)

 ```
// downloading from the product page is actually better
// choco installer sometimes fails to configure the tool correctly 
choco install qttabbar
```

## Extending Notepad++
TBD

## Extending VSCode
TBD

## Extending Visual Studio
TBD

## Extending Sublime Text`
TBD

## Greenshoot
TBD
