[Para ver em Português clique aqui](README-PT.md)

# Slidy

This CLI consists of a way to assemble your project structured by modules, pages, repositories, widgets always following the standards of good practices that has been applied by the community flutter in bigger and more structured projects.
It also provides the libraries manager (libs or pubs) with it you can install multiple libraries with just one command line and even remove and update.

## IMPORTANT NOTE! This project is under development.

We're excited to deliver slidy to the community, but it's still a package that's developing and may show some weird behavior. Use with caution.
To speed up and help with development, cooperate by putting your problems and suggestions in the **issues** tab of that repository.

## Motivations

We realized that the lack of a project pattern is affecting the productivity of several developers at that initial moment, so we are proposing a development pattern along with a tool that imitates NPM (NodeJS) functionality as well as template generation capabilities (similar to Scaffold ).

## About the Proposed Pattern.

We adopted the BLoC standard for business rule in a structure similar to MVC, where a page or widget has one or more BLoC to manage its business rule.

We are using the module structure and dependency injection of the package [bloc_pattern](https://pub.dev/packages/bloc_pattern). Read the bloc_pattern README to familiarize yourself with the concept of dependency injection, BLoC Provider and modules.


For services and provider we use the **Repository Pattern**.

In this way our folder structure is organized into local modules and a global module, as well as models, repositories and BLoC`s that can be accessed throughout the application in the shared folder.

Sample folder structure generated by **slidy**:

![Folder example](/folder.png)

## Installation

- You need to have the Dart SDK installed. If you do not have [download now](https://dart.dev/get-dart).
- Now just activate the slidy using the pub:

```
pub global activate slidy
```
- Type  ` slidy --version` -  if you return the slidy version you can consider the complete installation.
- To update the slidy just use the command:
```
slidy upgrade
```

Ready now you can enjoy this new world.

## Commands:    
  **start:** 
     Create a basic structure for your project (confirm that you have no data in the "lib" folder).
```  
slidy start
```     

**Install:**
Install (or update) a new package or packages:
```
slidy install rxdart dio bloc_pattern
```
You can also install a package as dev_dependency using the flag --dev
```
slidy i flutter_launcher_icons --dev
``` 
remove a package
 ```
 slidy uninstall dio 
 ```
You can also remove a dev_dependency using the flag --dev


## Generate:

Create a module, page, widget or repository according to the option.
    
**Options:**
    
Creates a new module with **slidy generate module**:
``` 
slidy generate module manager/product/product
``` 

Creates a new page and its respective Bloc
```
slidy generate page manager/product/pages/add_product
``` 
            
Creates a new widget and its respective Bloc:
```
slidy generate widget manager/product/widgets/product_detail
``` 
NOTE: You can create a page or widget with your respective BLoC using the flag **-b**
            
Create a new repository
```
slidy g r manager/product/repositories/product
``` 

For more details https://t.me/flutterando

