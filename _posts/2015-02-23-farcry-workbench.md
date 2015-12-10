---
layout: post
title: "FarCry Workbench Project"
date:   2015-02-23
author: "geoff-bowers"
tags: development
---

## Ambition

We want to build a distributable development environment for FarCry with a number of core features:

- works across Windows, Linux and OSX development workstations
- only requires a few instructions from a README to get going
- doubles as a deployment pipeline for updating your production code

It’s part of our goal to have a maximum 4 hour window to project productivity for any employee (no matter how new).

<!--more-->

## Stack

While FarCry supports a myriad of deployment configurations, we’re focused on a stack that resembles our ideal production environment.  More variants will come in time.

Base stack includes:

- Latest Ubuntu LTS (currently Trusty64)
- Tomcat 8
- NGINX
- Lucee 4.5
- mySQL 5.5

## Deployment 

Our deployment scripts all assume you have code stored in GIT repos, and that they only require a single ssh key (or anon) to get access to them.

The FarCry project format has an `./install` folder that can be filled with sample data, and a `deploy.txt` describing project dependencies. We want to leverage these options to automate the installation of projects.

## Progress

Daemonites have been involved in a lot of devops projects over the last couple of years.  We’d hoped to bring you an instant “FarCry In A Box” style of development environment for a while, but its been hard to make our scripting environments generic enough for public consumption.

@blair and @modius spent the last week cherry picking the best options from our various deployments.  We trying to build a generic set of `ansible-roles` to drive both vagrant and ec2 deployments (and potentially any sort of deployment).  We think we may have cracked it.

If you would like to help us get a universal **FarCry Workbench** up and running, please take a look at the prototype at http://github.com/modius/farcry-env-chelsea and give us your feedback.

