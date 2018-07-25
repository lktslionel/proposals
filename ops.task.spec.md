###### SOFTWARE DEVELOPMENT
# Task Spec.

**Version** : 0.1.0-draft

<br>

## Abstract

This document is an attempt to describe what I named UPS (Universal Project Structure). UPS is an project structure that is meant to be used for any kind of software project. Throughout this document I'll try to explain the philosphy and the goal behind this project structure, the main parts of this folder structure, how does it fit well for any kind of development and what benefits you could get from it.


## Contents

  1. [Proposal]
  1. [Tests]
  1. [Extras]
  1. [License]

## Proposal

Everything start with a task file. A task file is written in YAML and it contains a collections of task definitions. 
A task definition describes only one command to be run. As I said before, the goal here, is to organize all your scripts into concrete tasks definitions; this to avoid having to worry about where all those scripts scattered all over the system are, when you need them.

### DSL 

A simple DSL is used to describe a task. Every task definition contains : 

* **Name** : The task name in form of `<namespace>:<action>:<target|object>`
* **Alias** : some shortcut to run the task. Make sur it's unique
* **Short Description** : The summary of the goal of the task
* **Long Description** : A more detailed description with some examples
* **Command** : The full command to execute when the task is triggered
* **Args** : Contrains on args passed to the command
* **Hooks** : A way the execute scripts before or after a command execution

### Some examples

```yaml
---
- name: create 
```


### Tests


### Extras


## Authors

* Lionel T. ( [@lktslionel](twitter.com/lktslionel) )



## License

Copyright (c) 2017 - lktslionel. All rights reserved.

Licensed under the [MIT](LICENSE) License.



[Proposal]:     #Proposal  
[Tests]:        #Tests 
[Extras]:       #Extras  
[License]:      #License
