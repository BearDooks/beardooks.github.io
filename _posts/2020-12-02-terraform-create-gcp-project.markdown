---
title: "Using Terraform To Create A GCP Project"
description: "How to create a GCP project using terraform to have a standard and easy to use method"
date:  2020-12-02 10:00:00 -0500
categories: [GCP, Terraform, Guide]
tags: [GCP, Terraform, GCP Project, Guide]
author: chuck lindblom
sharing: true
show_author_profile: true
cover: /assets/images/terraform_logo.png
show_excerpt: true
excerpt_type: html
---

# Creating a GCP Project with Terraform

Like most jobs today, mine requires me to automate as much of it as possible. One of the things that seemed like an easy goal was to auto the creation of a GCP Project using a tool. We used to use Google Deployment Manager, but soon found it was more of a pain than we wanted to keep up to date.

# Project Layout

When creating this I laid out the files in easy to use sections. I also made sure to use the *depends_on* line a lot so I could ensue that everything was working in the order I wanted

* project.tf - Used to create the basic project
* services.tf - Used to tunr on APIs
* iam.tf _ Used to create all IAM policies
* network.tf - Used to create basic networking
* storage.tf - Used to create standard buckets
* serviceaccounts.tf - Used to make any service accounts needed

# Project Files

