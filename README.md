# Docker Notes

## What is Docker?
A container technology. A tool for creating and managing containers.

A container is a standardized unit of software. A package of code and dependencies to run that code (e.g. NodeJS code + the NodeJS runtime).

The same container always yields the exact same application and execution behavior! No matter where or by whom it might be executed.

## Why Containers?

Different development and production environments:
We want to build and test in exactly the same environment as we later run our app in.

Different development environments within a team/company:
Every team meber should have exactly the same environment when working on the same project.

Clashing Tools/Versions between different projects:
When switching between projects, tools used in project A should not clash with tools used in project B.

## The Problems

Environment: The runtimes, languages, frameworks you need for development and production are often not the same.

## We want Reliability and Reproducible Environments

We want to have the exact same environment for development AND production. This ensures that it works exactly as tested.

It should be easy to share a common development environment/setup with (new) employees and colleagues.

We don't want to uninstall and reinstall local dependencies and runtimes all the time.

## Virtual Machines / Virtual Operation Systems

Pros
    1. Separated environments.
    2. Environment-specific configurations are possible.
    3. Environment configurations can be shared and reproduced reliably.

Cons
    Redundant duplication, waste of space.
    Performance can be slow, boot times can be long.
    Reproducing on another computer/server is possible but may still be tricky.

## Docker Helps You Build and Manage Containers

Container(App, [Libraries, Dependencies, Tools])
Docker Engine
OS Built-in / Emulated Container Support
Your Operating System

## Containers vs Virtual Machines
Docker Containers
    Low impact on OS, very fast, minimal disk space usage
    Sharing, re-building, and distribution is easy
    Encapsulate apps/environments instead of "whole machines"

Virtual Machines
    Bigger impact on OS, slower, higher disk space usage
    Sharing, re-building, and distribution can be challenging
    Encapsulate "whole machines" instead pf just apps/environments

## Docker Tools and Building Blocks

Docker Engine
Docker Desktop (includes Daemon & CLI)
Docker Hub
Docker Compose

Kubernetes


## Running

In the root directory, type this in the terminal:
    `docker build .`
Grab the ID that is outputted in the console and use it in this command (replace id):
    `docker run -p 3000:3000 id`
Open the browser and go to port 3000.

## Terminating

Open a new terminal:
    `docker ps`
Grab the name you get and use it in the next command
    `docker stop name`
