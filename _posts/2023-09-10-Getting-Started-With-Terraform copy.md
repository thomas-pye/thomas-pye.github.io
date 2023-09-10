---
author: Tom Pye
title: Getting Started with Terraform - Part 1
tags: terraform windows azure
date: 2023-09-10
#published: false
---

Today we are going to talk about the bare basics of running terraform locally. In this article we will setup a basic configuration, run all the main terraform commands in order to create a very simple infrastructure setup on azure.

Why local? I'm strongly of the opinion that you need to drill and understand the command line of your tooling, and running locally allows you to learn the terraform fundamentals without the complexities of CI/CD pipeline providers.

After all, if you can understand your command line, you can incorporate it into your pipelines as a script.

First, lets install terraform, we're going to make an assumption that you're running windows here.

You can use chocolatey...

```
$ choco install terraform
```

or install manually from the terraform home page https://www.terraform.io/

Once installed, run the terraform command and you should see some basic usage instructions

```
Usage: terraform [global options] <subcommand> [args]

The available commands for execution are listed below.
The primary workflow commands are given first, followed by
less common or more advanced commands.

Main commands:
  init          Prepare your working directory for other commands
  validate      Check whether the configuration is valid
  plan          Show changes required by the current configuration
  apply         Create or update infrastructure
  destroy       Destroy previously-created infrastructure
```


Before we progress further, lets discuss the main commands

init - Initializes a working directory that contains terraform configuration files. This is the first command that should be run when setting up your terraform configuration.

validate - Checks your configuation files without referring to any remote services, checks that you have valid syntax, ignoring variables or state.

plan - Creates an execution plan, comparing against the current state and remote object states, and generates a set of change actions to be applied.

apply - Runs the actions proposed in plan

destroy - Removes ALL remove objects managed by your configuration


TO-DO

Set-up azure configuration

Set-up azure RBAC

Create a very simple main.tf (resource group and storage account)

Variablise the configuration

validate it

plan it

apply it

destroy it

