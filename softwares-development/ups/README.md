# UPS Spec.

**Version** : 0.1.0-draft

Dec, 2017

<br>

## Abstract

This document is an attempt to describe what I named UPS (Universal Project Structure). UPS is an project structure that is meant to be used for any kind of software project. Throughout this document I'll try to explain the philosphy and the goal behind this project structure, the main parts of this folder structure, how does it fit well for any kind of development and what benefits you could get from it.


<br>

## Terminology

Let's explain some useful terms used in this docs. Feel free to skip term definitions that you already know.

* **UPS** : Universal Project Structure
* **Kind** : A precise type of project specific to an area in software development. For example, in are of web development, we could have as project ***kind*** : an API, a site(blog), a web-app, etc.


<br>

## Contents

  1. [Overview]
  1. [Scope]
  1. [Purpose]
  1. [Requirements]
  1. [Overview]
  1. [Metafile]
      * [ups]
  1. [Documentation]
  1. [Source]
  1. [Configuration]
  1. [Scripts]
  1. [specs]
  1. [Tests]
  1. [Extras]
  1. [License]

<br>

## Overview

Building software today is easier that before. Nowadays, we got IDEs, Frameworks, and Tools which speed up our work or make us more productive. A the early stage of your development process, we are provided with tools : 

* To scaffold our project folder
* To setup our porject for development
* To add third-party libraries to our project
* And more.

As a result, those frameworks and tools tend to shift our focus far from the business problem we're solving. In fact, we put too much emphasis on how to use thoses frameworks and tools, but less on how we should architect our applications for the business problems we are facing. As Uncle Bob([@unclebobmartin](https://twitter.com/unclebobmartin)) quoted in [his talk about clean architecture](https://youtu.be/o_TH-Y78tt4?t=10m42s) : 

  > Why does the higher level directory structure of this application tell me the framework I am using; Why doesn't it tell me what the application does ? <br>- Robert C. Martins (Uncle Bob)

It means for me that we should not let the framework encapsulate what our application is doing but instead, make our application encapsulate the framework it is using. More precisely, the higher level directory structure of your application must either tell what your application does or nothing (being completely neutral). But what does ***neutral*** means ? By neutral I mean that at first glance of an application structure you shouldn't be able to guess want framework the application is using. 

I think doing this is a step forward towards the ultime goal of building a directory structure that make us get what the application do. Throughout this document, I will tell you how I acheive neutrality by building a **unique** high level directory structure.


<br>

## Scope

I really beleive that UPS could be applied to any kind of project. At the moment, tried and validate UPS for web development projects only but in the future, I plan to apply the same principles to mobile development and more. 

<br>

## Goals

UPS aims to provide : 

* A high level projecft structure that is completely framework agnostic (neutral)
* The best workspace and tools to ease our work througout the softwares development processes/activities



<br>

## Requirements and tooling

To acheive those goals we need well known and proven tools used in the software development lifecyle. As I said before, UPS is an apinionated folder structure. It is made possible by a set of tools that support the philosophy. So what an UPS project requires ? 

To follow UPS, you need to be familiar with the following tools : 

* **Docker** : It eanble us to build our application in an isaolated sandbox that is similar to the target live environment
* **Rake** : It is a great tools known and loved by Ruby developers. I use this to manage every tasks executed througout our development process and even till the deployment of the application to any environments.

<br>

## Metafile

<br>

### ups

<br>

### project

<br>

## Documentation

<br>

## Source

<br>

## Utilities

<br>

## Scripts

<br>

## Tests

<br>

## Extras

<br>

## Authors

* Lionel T. ( [@lktslionel](twitter.com/lktslionel) )


<br>

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