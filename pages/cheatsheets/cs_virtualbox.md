---
title: Virtualbox
keywords: cheatsheets
last_updated: August 2, 2019
tags: [cheatsheets]
sidebar: cheatsheets_sidebar
permalink: cs_virtualbox.html
folder: cheatsheets
---

List running VMs:

    VBoxManage list runningvms

Stop a running VM:

    VBoxManage controlvm <UUID|VMNAME> pause|resume|reset|poweroff etc.

Delete a VM:

    VboxManage unregistervm <UUID|VMNAME> [--delete]
