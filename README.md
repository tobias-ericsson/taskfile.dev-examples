# Taskfile.dev-examples
Taskfile.dev Examples

## TLDR

Proposal:

All your, and your colleagues, projects/repositories should, in the root, alongside a good up-to-date README.md file have:

* A Taskfile with tasks to quickly get started with local development.

Homogenize your projects by the use of Taskfiles.

The Taskfile should contain the same or similar tasks regardless of project. No matter if you are building a web or mobile app, or API or something else you need a simple way of running it locally, and testing and deploying. 

 Tasks to consider should be:

* build
* run
* test
* integration-test
* deploy-dev
* deploy-prod
* cleanup

## Background

### The problem to solve

Imagine that you want to get an application running on your local developer machine in order to make some minor changes, test them and then deploy the new version.

For instance, imagine you have been tasked with updating all new and old applications with the new name and logo of company X, where you work, after the merger with company Y.

You have access to the source code of the application but it is not the usual codebase you work on daily, instead the application is written in a programming language you barely know.

Or just imagine that this is your first week as a new employee or that this is your hobbie-project in Erlang your wrote five years ago and have forgotten all about.

How do you get up and running?

A good place to start would be the README.md file. There is a README.md file right?

You hope that file would contain information on how to run and test the application, and

hopefully that information will be just a one-liner you can copy and paste to your terminal.

But sadly the command or commands you got from the README.md file do not work properly out of the box.

Maybe the README.md is slighty out of date or maybe you are using the wrong version of some dependency or serveral. 

Or maybe there where no information at all.

Now the investigation work begins.

Can we do better next time around?

### The solution

Yes - we can give some more love to our README.md files and try to make sure that they contain the correct and complete information to get you started.

But it would be even better if you did not need to copy and paste commands from a README.md to you terminal. 

What if the commands instead where contained in some script the daily developers of the application themselves uses, or used at the time when the application where under daily development? That would increase the likelihood that the commands actually work.

But I'm not talking about a build tool which is only used together with a specific programming language or specific technology stack. 

For example most Javascript / frontend developers will likely be a bit lost when it comes to building with Maven or Gradle and most Java backend developers will be a bit lost when it comes to building with Yarn or npm and none of them would know which tool to use to build a Python or Golang project. You get my message. 

Can we wrap these specfic build tools in a starter package which will look and work the same regardless of programming language and tech stack?

So that an employee who changes team to work on something else can feel instantly at home. And so that you yourself can pick up an old forgotten project and get up and running in notime? 

#### Tools I have considered

* Bash

What is common for all and allready available? Well, Bash should be available on virtually all systems if you disregard Windows, and even on Windows with the use of WSL2 or Cygwin. A simple bash-script could work but bash-scripts can become ugly and hard to read/understand. And the writing style would differ from team to team. Not great.

* Docker and docker-compose

Docker is great in local development for running the stuff around your application, like the database or redis cache or other backend dependencies but you probably do not want to run the application under development in docker. It's a bit heavy for that. Again, not great.

* Make and makefiles

What is common for all and allready available? Well, Make should be available on most Linux systems and could be installed on Windows with the use of WSL2 or Cygwin.
Make is a good choice but I recently found a newer and better alternative.

### The winning tool - Task and Taskfiles



### Loose ends

For next blog post, follow up with...

How to install and make sure you use the right versions of the underlying language (Java, Python, Golang, etc) and build tool (Gradle, Maven, Yarn, etc)

NIX to the resque?

Proposal:

All your, and your colleagues, projects/repositories should, in the root, have the following files:

* A NIX file. Use NIX to install right versions of dependencies.




















