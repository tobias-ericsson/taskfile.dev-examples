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


