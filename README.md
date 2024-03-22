# Task Examples

[Task](https://taskfile.dev/) is a task runner / build tool that aims to be simpler and easier to use than, for example, GNU Make.

This repository contains examples of how to use Task as the common homogeneous standard (wrapper) to build, test and run 
your teams application locally regardless of which programming language, architecture or underlying build tool used.

The goal is to make it as painless as possible for a new developer, or a developer who does not work with the code-base daily, to get up and running.

## TLDR

I propose that all your, and your colleagues, projects/repositories should, in the root, alongside a good up-to-date README.md file have a 
Taskfile.yaml with tasks to quickly get started with local development.

The Taskfile should contain the same or similar tasks regardless of project. 

No matter if you are building a web or mobile app, API or something else you will benefit of having a simple and standard way to build, test and run it locally. 

The examples in this repository are meant to get you started, not as a complete list of tasks your project needs.

Tasks to consider should be:

* build
* test
* integration-test
* run
* deploy-dev
* deploy-prod
* cleanup

## Background

### The problem to solve

Imagine that you want to get an application running on your local developer machine in order to make some minor changes, test them and then deploy the new version.

For instance, imagine you have been tasked with updating all new and old applications with the new name and logo of company X, where you work, after the merger with company Y.

You have access to the source code of the application but it is not the usual codebase you work on daily, instead the application is written in a programming language you barely know.

Or just imagine that this is your first week as a new employee or that this is your hobbies-project in Erlang your wrote five years ago and have forgotten all about.

How do you get up and running?

A good place to start would be the README.md file. There is a README.md file right?

You hope that file would contain information on how to run and test the application, and

hopefully that information will be just a one-liner you can copy and paste to your terminal.

But sadly the command or commands you got from the README.md file do not work properly out of the box.

Maybe the README.md is slightly out of date or maybe you are using the wrong version of some dependency or several. 

Or maybe there was no information at all.

Now the investigation work begins.

Can we do better next time around?

### The solution

Yes - we can give some more love to our README.md files and try to make sure that they contain the correct and complete information to get you started.

But it would be even better if you did not need to copy and paste commands from a README.md to your terminal. 

What if the commands instead where contained in some script the daily developers of the application themselves uses, or used at the time when the application where under daily development? That would increase the likelihood that the commands actually work.

But I'm not talking about a build tool which is only used together with a specific programming language or specific technology stack. 

For example most Javascript / frontend developers will likely be a bit lost when it comes to building with Maven or Gradle and most Java backend developers will be a bit lost when it comes to building with Yarn or npm and none of them would know which tool to use to build a Python or Golang project. You get my message. 

Can we wrap these specific build tools in a starter package which will look and work the same regardless of programming language and tech stack?

So that an employee who changes team to work on something else can feel instantly at home. And so that you yourself can pick up an old forgotten project and get up and running in notime? 

#### Tools I have considered

* Bash

What is common for all and already available? Well, Bash should be available on virtually all systems if you disregard Windows, and even on Windows with the use of WSL2 or Cygwin. A simple bash-script could work but bash-scripts can become ugly and hard to read/understand. And the writing style would differ from team to team. Not great.

* Docker and docker-compose

Docker is great in local development for running the stuff around your application, like the database or redis cache or other backend dependencies but you probably do not want to run the application under development in docker. It's a bit heavy for that. Again, not great.

* Make and makefiles

What is common for all and already available? Well, Make should be available on most Linux systems and could be installed on Windows with the use of WSL2 or Cygwin.
Make is a good choice but I recently found a newer and better alternative.

### The winning tool - Task and Taskfiles

[Task](https://taskfile.dev/) is a task runner / build tool written in Go that aims to be simpler and easier to use than, for example Make.

Once installed, you just need to describe your build tasks using a simple YAML schema in a file called Taskfile.yml:

Example with Golang:
https://github.com/tobias-ericsson/taskfile.dev-examples/blob/a079ecf0f2584aa731f67366f0e9f4f1083887c9/golang/Taskfile.yml#L1-L22

Example with Java:
https://github.com/tobias-ericsson/taskfile.dev-examples/blob/a079ecf0f2584aa731f67366f0e9f4f1083887c9/java/Taskfile.yml#L1-L23

And call for instance the build task by running `task build` from your terminal.

This is somewhat cleaner and simpler than using Make, which would look something like this:

https://github.com/tobias-ericsson/taskfile.dev-examples/blob/a079ecf0f2584aa731f67366f0e9f4f1083887c9/golang/makefile#L1-L15

Which you would run by `make build` from your terminal.

### Possible improvments

This is a solution to quickly understand which tools to use and which commands to execute (by inspecting the Taskfile.yml).

It is not a solution to easy install of the right versions of said tools. 

How can we easily install the right versions of the underlying language (Java, Python, Golang, etc) and build tool (Gradle, Maven, Yarn, etc)?

[NIX](https://nix.dev/) to the rescue?

I might soon propose that you use NIX to install the right versions of all tools and dependencies. Possibly all your, and your colleagues, projects/repositories should, in the root, alongside a good up-to-date README.md file have a NIX file to quickly install the right versions of your tools.








