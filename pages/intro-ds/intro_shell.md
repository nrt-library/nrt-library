---
title: Introduction to the UNIX Shell (Bash)
tags:
  - getting_started
keywords: "stats" # new keywords requiere to create a new tag file
last_updated: "August 6, 2020"
summary: "The UNIX Shell is a interface and programming languague that provides an interactive instance to start programs, manage files, and processes running in the computer. "
published: true
sidebar: intro_ds_sidebar #name of yml sidebar file withouth extension
permalink: intro_shell.html
folder: intro-ds
---

## What is the UNIX Shell (Bash)?

The UNIX shell is a program to **interface** with the lowest level of UNIX-based operating systems (i.e., the kernel). If you are running any Mac OS or Linux Distribution, you are using a UNIX-based or Unix-like operating system. UNIX-based operating systems have two main parts: the **kernel** and the **utilities**. The *kernel* is the program managing and allocating the resources of the computer hardware (i.e., the Central Processing Unit or CPU, the Random Access Memory or RAM, and devices like the mouse, speaker, etc). It is a **software layer facilitating the control of the computer hardware**. The *utilities* are a set of commands to interface with the kernel. For instance, if you type `pwd` in your terminal, the kernel will load a program called `pwd` into the RAM, read the program instructions, and display the output, in this case, the current working directory path.

The so-called **shell**, also happens to be a UNIX utility program. It has a dual identity: as a **user interface** to the UNIX utilities, and as a **programming language** facilitating the usage and combination of the UNIX utilities. When you open the terminal, the shell program is loaded into the computer memory. When you type commands in the terminal, the shell reads the commands and converts them into a format that is readable by the kernel to be executed. It provides an interactive instance to start programs, manage files, and processes running in the computer.

## Recommended path for learing

- Introductory article: [Introduction to the UNIX Shell (Bash)](https://pabloinsente.github.io/intro-unix-shell)

- 74 minutes introductory video: **Beginner's Guide to the Bash Terminal**
<iframe width="560" height="315" src="https://www.youtube.com/embed/oxuRxtrO2Ag" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Video courses

- **Bash Script with Practical Examples - Full Course**

<iframe width="560" height="315" src="https://www.youtube.com/embed/TPRSJbtfK4M" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- **Linux Command Line Full course: Beginners to Advance. Bash Command Line Tutorials**

<iframe width="560" height="315" src="https://www.youtube.com/embed/2PGnYjbYuUo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Online tutorials

- [Software carpentry UNIX shell introduction](https://swcarpentry.github.io/shell-novice/)
- [Introduction to the Bash Command Line](https://programminghistorian.org/en/lessons/intro-to-bash)
- [Bash handbook](https://github.com/denysdovhan/bash-handbook)

## Contributors

- [Pablo Caceres](mydoc_about.html#pablocaceres) 

{% include links.html %}
