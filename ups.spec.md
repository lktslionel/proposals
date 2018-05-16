###### SOFTWARE DEVELOPMENT
# UPS Spec.

**Version** : 0.1.0-draft

<br>

## Abstract

This document is an attempt to describe what I named UPS (Universal Project Structure). UPS is an project structure that is meant to be used for any kind of software project. Throughout this document I'll try to explain the philosphy and the goal behind this project structure, the main parts of this folder structure, how does it fit well for any kind of development and what benefits you could get from it.


## Terminology

Let's explain some useful terms used in this docs. Feel free to skip term definitions that you already know.

* **UPS**: Universal Project Structure
* **Kind**: A precise type of project specific to an area in software development. For example, in are of web development, we could have as project ***kind*** : an API, a site(blog), a web-app, etc.
* **runtime**: The environment in which your code will be executed. Eg: nodejs, go, jre(java)
* **lang**: The main language in which the code is written. 
* **lang_extras**: The other programming language used in your project.

## Contents

  1. [introduction]
  1. [Scope]
  1. [Purpose]
  1. [Requirements]
  1. [Overview]
  1. [Metafile]
      * [ups]
  1. [Documentation]
  1. [Examples]
  1. [Source]
  1. [Configuration]
  1. [Scripts]
  1. [Tests]
  1. [Extras]
  1. [License]

## Introduction

Building software today is easier that before. Nowadays, we got IDEs, Frameworks, and Tools which speed up our work or make us more productive. At the early stage of your development process, we have at our disposal tools : 

* To scaffold our project folder
* To setup our development environment 
* To add third-party libraries and dependencies to our project
* And more.

As a result, those frameworks and tools tend to shift our focus far from the business problem we're trying to solve. In fact, we put too much emphasis on how to use thoses frameworks and tools, and less on how we should architect our applications. The aim of our business logic is being hidden by either frameworks or/and tools. As Uncle Bob([@unclebobmartin](https://twitter.com/unclebobmartin)) quoted in [his talk about clean architecture](https://youtu.be/o_TH-Y78tt4?t=10m42s) : 

  > Why does the higher level directory structure of this application tell me the framework I am using; Why doesn't it tell me what the application does ? <br>- Robert C. Martins (Uncle Bob)

For me, this means that we should not let those frameworks hide our buisness logic, but instead, make our application drives to way we use those frameworks. More precisely, the higher level directory structure of your application must either tell what your application does or nothing; the directory structure of your application must be frameworks neutral. But what does ***neutral*** means ? By neutral I mean that at first glance of an application structure you shouldn't be able to guess want framework the application is using. 

I think doing this is a step forward towards the ultime goal of building a directory structure that make us get what the application do. Throughout this document, I will tell you how I acheive neutrality by building a **unique** high level directory structure.


## Scope

I really beleive that UPS could be applied to any kind of project. At the moment, tried and validate UPS for web development projects only but in the future, I plan to apply the same principles to mobile development and more. 

## Goals

UPS aims to provide : 

* A high level projecft structure that is completely framework agnostic (neutral)
* The best workspace and tools to ease our work througout the softwares development processes/activities

## Requirements and tooling

To acheive those goals we need well known and proven tools used in the software development lifecyle. As I said before, UPS is an apinionated folder structure. It is made possible by a set of tools that support the philosophy. So what an UPS project requires ? 

To follow UPS, you need to be familiar with the following tools : 

* **Git** : It's the prefered solution for source code versionning and development flow
* **Docker** : It eanble us to build our application in an isaolated sandbox that is similar to the target live environment
* **Rake** : It is a great tools known and loved by Ruby developers. I use this to manage every tasks executed througout our development process and even till the deployment of the application to any environments.

## Project Structure

### Overview

Let's directly dive into it. Below is the global strucure of an UPS project.


```bash
.
├── .target/                          # Contains the resulting artifact of the `assemble` phase
├── .cache/                           # For caching purpose
├── examples/                         # Use this for useful examples
├── etc/                              # Configuration files
├── tasks/                            # Binaries and utility scripts used for the project mainly inside the Rakefile
│                                     #   for the project mainly inside the Rakefile
├── scripts/                          # Common bash scripts available inside the container
├── tests/                            # Specifications
│   ├── acceptance                    #   For accpetance testing
│   │   ├── features                  #     Contains feature definition in Gherkin langage
│   │   │   ├── XXX.feature           #       - A feature file
│   │   ├── steps                     #     Contains implemenation steps of features
│   │   │   ├── YYY.step.<lang>       #       - A Step file for the specific language
├── docs/                             # Contains all documentation files (*.md)
│   ├── CHANGELOG.md                  #   - Release notes for the project
│   ├── GUIDELINES.md                 #   - Project guidelines inforamtion
│   └── CONTRIBUTE.md                 #   - Information about how to contribute
│   └── MOTIVATION.md                 # Describe the purpose behind building that project
│   └── FAQ.md                        # Frequently Ask Questions about the project/product
├── ci/                               # Contains config file specific to your CI tool. Eg: jenkins
├── src/                              # For your source files
├── README.md                         # Main documentation (How-tos)
├── LICENSE                           # License file
├── Rakefile                          # Contains all our rake task's defintions
└── .ups                              # UPS metafile
```


### Metafile


#### ups


#### project


### Configuration

```
├── etc/                              # Configuration files
│   ├── ansible/                      # Ansible playbooks
│   └── docker/                       # Docker config files
│       ├── Dockerfile                #   - Dockerfile use in the `assemble` phase
│       ├── docker-compose.yml        #   - Compose file use in the `assemble` phase
```


### Continuous Integration

```
├── ci/                               # Contains config file specific to your CI tool. Eg: jenkins
│   ├── jenkins/                      #
│   │   └── Jenkinsfile               # Contains description of our jenkins pipeline (CI)
│   ├── gitlab/                       #
│   │   └── .gitlab.yml               # Contains description of our jenkins pipeline (CI)
```

### Documentation



### Examples




### Source


### Tasks

```
├── tasks/                            # Binaries and utility scripts used for the project not inside the container 
│   ├── code                          #   - Execute tasks for building our code
│   ├── build                         #   - Execute tasks for building our code
│   ├── test                          #   - Execute tasks for testing our code
│   ├── release                       #   - Execute tasks for pushing our packaged app to a repo manager
```

```
rake code:audit 
```

### Utilities

#### Target
#### Cache

### Scripts

```
├── scripts/                          # Common bash scripts available inside the container
│   ├── run                           #   - Execute tasks for running our app
│   ├── backup                        #   - Execute tasks for backuping our app
│   └── restore                       #   - Execute tasks for restoring our app
```


### Tests


### Extras


## Authors

* Lionel T. ( [@lktslionel](twitter.com/lktslionel) )



## License

Copyright (c) 2017 - lktslionel. All rights reserved.

Licensed under the [MIT](LICENSE) License.



[Introduction]:     #Introduction  
[Overview]:         #Overview  
[Scope]:            #Scope 
[Purpose]:          #Purpose 
[Requirements]:     #Requirements  
[Structure]:        #Structure 
[Overview]:         #Overview  
[Metafile]:         #Metafile  
[Sections]:         #Sections  
[ups]:              #ups 
[Documentation]:    #Documentation 
[Source]:           #Source  
[Configuration]:    #Configuration 
[Scripts]:          #Scripts 
[Specs]:            #Specs 
[Tests]:            #Tests 
[Extras]:           #Extras  
[License]:          #License
