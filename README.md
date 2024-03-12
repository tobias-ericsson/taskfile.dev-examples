# Taskfile.dev-examples
Taskfile.dev Examples

## TLDR

Proposal.

All your, and your colleagues, projects/repositories should, in the root, have the following three files:

* A good up-to-date README.md
* A Taskfile with tasks to quickly get started with local development.
* A NIX file. Use NIX to install right versions of dependencies.

Homogenize your projects by
use Nix and Taskfile.

The Taskfile should contain the same or similar tasks. No matter if you are building a web or mobile app, or API or something else you need a simple way of running it locally, and testing and deploying.

Tasks:

* run
* test
* cleanup


## Background

### The problem to solve

Imagine that you want to get an application running on your local developer machine in order to make some minor changes, test them and then deploy the new version.

For instance, imagine you have been tasked with updating all new and old applications with the new name and logo of company X, where you work, after the merger with company Y.

You have access to the source code of the application but it is not the usual codebase you work on daily, instead the application is written in a programming language you barely know.

Or just imagine that this is your first week as a new employee or that this is your hobbie-project your wrote five years ago and forgotten all about.

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

What if the commands instead where contained in some script the daily developers of the application themselves uses, or used at the time the application where under daily development? That would increase the likelihood that the commands actually work.

But I'm not talking about a build tool which is only used together with a specific programming language or specific technology stack. 

For example most Javascript / frontend developers will likely be a bit lost when it comes to building with Maven or Gradle and most Java backend developers will be a bit lost when it comes to building with Yarn or npm and none of them would know which tool to use to build a Python or Golang project. You get my message. 

Can we wrap these specfic build tools in a starter package which will look and work the same regardless of programming language and tech stack?

So that an employee who changes team to work on something else would feel instantly at home. 

And so that you yourself can pick up an old forgotten project and get up and running in notime? 












