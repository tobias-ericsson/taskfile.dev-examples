# Task Examples

[Task](https://taskfile.dev/) is a task runner / build tool that aims to be simpler and easier to use than, for example, GNU Make.

This repository contains examples of how to use Task as the common homogeneous standard (wrapper) to build, test and run 
your teams application locally regardless of which programming language, architecture or underlying build tool used.

The goal is to make it as painless as possible for a new developer, or a developer who does not work with the code-base daily, to get up and running.

## TLDR

I propose that you use Task as the common uniforming standard (wrapper) to build, test, and run your team’s application regardless of which programming language, architecture, or underlying build tool is used.

Task is a task runner / build tool that aims to be simpler and easier to use than, for example, GNU Make.

All your, and your colleagues, projects/repositories should, in the root, alongside a good up-to-date README.md file have a Taskfile.yaml with common tasks.

This will remove friction and enable you and your colleagues to get started with local development quickly.

## Examples

Once installed, you just need to describe your build tasks using a simple YAML schema in a file called Taskfile.yml:

Example with Golang:
https://github.com/tobias-ericsson/taskfile.dev-examples/blob/a079ecf0f2584aa731f67366f0e9f4f1083887c9/golang/Taskfile.yml#L1-L22

Example with Java:
https://github.com/tobias-ericsson/taskfile.dev-examples/blob/a079ecf0f2584aa731f67366f0e9f4f1083887c9/java/Taskfile.yml#L1-L23

And call for instance the build task by running `task build` from your terminal.

This is somewhat cleaner and simpler than using Make, which would look something like this:

https://github.com/tobias-ericsson/taskfile.dev-examples/blob/a079ecf0f2584aa731f67366f0e9f4f1083887c9/golang/makefile#L1-L15

Which you would run by `make build` from your terminal.


