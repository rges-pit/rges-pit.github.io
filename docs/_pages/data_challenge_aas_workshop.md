---
permalink: /data-challenge/aas-workshop/
title: "Data Challenge AAS Workshop"
sidebar:
  nav: "workshop"
description: "AAS 247 workshop for RMDC25: requirements, agenda, Roman Research Nexus access, and session outlines."
---

> | January 4, 2026 | 9 am – 5 pm | AAS 247 | Room TBD |

## Registration

<!-- https://aas.org/meetings/aas247/registration -->
<!-- Registration button -->
<div style="text-align: center; margin: 2em 0;">
  <a href="https://aas.org/meetings/aas247/registration" target="_blank" style="background-color: #a859e4; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold; display: inline-block; transition: background-color 0.2s;">Sign Up</a>
  <div style="margin-top: 0.5em; color: #555;">Workshop/AAS 247 Registration</div>
</div>

You can register for this workshop when you register for the AAS 247 Meeting. Select "Roman Galactic Bulge Time Domain Survey Data Challenge" from the list of offered workshops.

## Description

The RMDC25 AAS Workshop is a hands-on, full-day session designed to get participants—from newcomers to seasoned microlensers—set up and productive with the Roman Research Nexus and the core open-source tools used in the Roman Microlensing Data Challenge. We’ll walk through Nexus access and environment setup, introduce essential microlensing concepts and modeling workflows, explore single- and binary-lens fitting (including grid searches and practical strategies for degeneracies and higher-order effects), and show how to organize, validate, and package results for submission using microlens-submit. Bring a laptop and a willingness to experiment; light Python experience is helpful but not required. The day closes with an information session and Q&A covering timelines, tiers, data access, evaluation, and how to get help throughout the challenge.

## Requirements

* A laptop with a functioning web browser (optionally, VS Code and Slack installed).
* Ideally, some Python experience.
* An intention to participate in the [Roman Microlensing Data Challenge 2025]({{ site.url }}{{ site.baseurl }}/data-challenge/) or be on an already signed-up team. You can sign up [here]({{ site.url }}{{ site.baseurl }}/data-challenge/sign-up/).
* Microlensing-specific knowledge or experience is **not** necessary.

## Itinerary

#### Morning

9:00–10:30 | Nexus help
10:30–11:00 | Break
11:00–12:30 | Single lenses and pipelines
12:30–1:30 | Lunch

#### Afternoon

1:30–3:00 | Binary lenses
3:00–3:30 | Break
3:30–onward | Data Challenge Q&A

## Session Outlines

### [1. Introduction to the Nexus]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/1-nexus/)

For discussion, information, troubleshooting, and updates about the Nexus, see the `#nexus` channel and the channel canvas.
In this session we will be covering:

* Creating Nexus accounts
* How to access the Nexus
* Nexus notebook content:
    * Creating Teams
    * Microlensing open source software
    * Accessing data and creating data challenge submissions
* Installing packages and other technical help
* Using the Nexus with VSCode or Colab

### [2. Single Lenses and Pipelines]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/2-single-lenses/)

In this session, we will learn about basic microlensing parameterization and terminology and test that knowledge on a mini modeling Data Challenge.
Topics covered:

* An introduction to microlensing
* Helpful microlensing resources
* Alternate data access, for those not using the Nexus
* Hack-session where we will learn about:
    * Single lens fitting
    * Priors
    * Parallelization
    * L2 observer
    * Anomaly finding

### [3. Binary Lenses]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/3-binary-lenses/)

We will begin this session with a more complicated binary-lens model and exercises to demonstrate the challenges of binary-lens fitting and common approaches to addressing them. We will fit that same event using three different methods:

1. Start a fit from an uninformed guess
2. Start with a grid search 
3. Start from an informed guess

Some of these methods are computationally expensive, so we will parallelize our efforts and discuss common challenges in microlensing binary-lens modeling, e.g., degeneracies, stochastic likelihood space, and higher-order effects.

### [4. Information Session and Q&A]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/4-info/)

Ask the demonstrators anything you would like to know about microlensing and/or the Data Challenge.
They will also provide details on:

* The RGES-PIT website
* The Slack channel
* Sign-up
* Tiers
* Data insights
* Submission rules and guidelines
* Evaluation process and rubric
* Publication plans
* Important dates
* Contact
