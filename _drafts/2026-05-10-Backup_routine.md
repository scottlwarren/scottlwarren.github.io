---
layout: post
title: "Backup automation - A homelab approach"
date: 2026-05-10
categories: update
---

# You don't need a backup - until you need one

Backups are one of those maintenance tasks that can be a bit annoying to set up, but really can save time in the longrun. Indeed, one of the cons of repurposing hardware is that it's hard to know when it's going to fail. And it will fail, just hopefully after many years of faithful service.

# What to backup?

I've chosen a few key things that I wanted to backup on my two systems that make up my [homelab]({% post_url 2026-04-27-Homelab %}):

* Docker compose files
* Gitea database dump
* Essential documents

I've chosen not to backup media for now, as this is something that requires a lot of storage and is replaceable should any drives decide to retire. The Gitea database on the other hand, is something that I would rather not lose. When I was in the initial setup of the new lab, I did actually lose it leading to lots of panicked repo creation!

Another reason to focus on Gitea is due to the storage solution of the Raspberry Pi on which it's hosted. MicroSD cards are wonderful things, but are less reliable long term storage solutions to normal drives, and so the risk of loss is higher.

# Backup routine

In order to make things as smooth as possible, I aimed to create a backup schedule that would be automated, while also allowing for some level of version control. This means that when I inevitably break something, I can revert back to something that actually worked.

### Capturing Docker Compose changes in Gitea

In order to both source-control and backup my services on Docker Compose, I used Git. First step was finding the sources on the main mini PC, and then setting the remote repository. This workflow assumes that you are comfortable with [git](https://git-scm.com/)

```shell
cd /var/lib/casaos/apps/
# set directory to location where Docker Compose .yml files are stored
sudo git init
sudo git remote add origin http://192.xxx.xx.xxx:xxxx/scott/casaos-backups.git 
# Change your IP and port to your Gitea Instance
```
With the repo initiated, and remote set it's easy now to `git push` the Docker Compose files into Gitea, and therefore save them. However, this is still a manual process. 

To automate, I created a bash script that could be scheduled:

```shell
#!/bin/bash
cd /var/lib/casaos/apps/
sudo git add .
sudo git commit -m "Automated backup: $(date)"
sudo git push origin master
```
This script, saved as `dc_backup.sh`, essentially runs the code needed to stage (add .), commit (with a timestamp) and push the commits to the Gitea server. We are still missing the automation part, as a manual call would be required for this to run. Linux machines have a scheduling system known as Cron. Cron is a bit difficult to find if you don't know where to look, but can be accessed using the `crontab -e` command in your terminal.

Cron also uses a bit of a weird setup for defining actions.