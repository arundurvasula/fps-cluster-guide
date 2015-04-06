# Foundation Plant Services Cluster Guide

by Arun Durvasula

Welcome to the FPS cluster usage guide! Please read this document fully before working on the cluster.

## Setting up an account
In order to set up an account on the cluster, you will need to 1) be able to use SSH on your computer and 2) register an account with your KERBEROS username here: [insert link]

### Windows
In order to set up SSH on Windows, you will need to install Putty: http://www.putty.org
 
You will also need to generate a public and private key so that you can log in to the cluster. In order to do this, please follow this guide: http://www.ualberta.ca/CNS/RESEARCH/LinuxClusters/pka-putty.html


### Mac

### Linux
Same as Mac.

## Logging in
Now that you have your account set up, you need to log in. If you are using Putty on Windows, you will need to follow this guide: https://www.howtoforge.com/ssh_key_based_logins_putty

The host name for the cluster is `agri.cse.ucdavis.edu`

On Mac or Linux, you can log in using the ssh command in the terminal:

`ssh <username>@agri.cse.ucdavis.edu`

## General cluster notes

### Filenames
Never *ever* use spaces in your filenames. Linux uses spaces to delimit arguments in many programs and will break if there is a space in a filename. In order to avoid this, please use the _ (underscore) character instead of spaces.

### Directory structure
The cluster is a linux computer, which has a standard hierarchy of folders. Each user gets a home directory, located at `/home/<username>`. We also have a group directory, located at `/group/fps` which everyone has access to. Because we want everyone to be able to access the data files and run analyses on them, we will store all data and results in `/group/fps`. However, because everyone will have access to these files, you have to be very careful when removing or modifying files because other people may be using them. Please check with other members of the lab before removing/modifying files.

- `/group/fps/software`: this directory contains the exectuable programs that we will use. This directory only contains software that isn't installed on a system-wide basis.
- `/group/fps/data`: this directory contains all the data that we will be using. 


### Removing temporary files
Assembly creates a lot of temporary files that we do not need after the assembly is run. Please remove the temporary files after the assembly has finished to save disk space.



## fps-init.sh
Run this program to set up your environment and install the necessary software.

- install R packages
- add `/group/fps/software` to path
