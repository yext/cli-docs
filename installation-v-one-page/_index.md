---
title: Installation
order: 1
---

## Mac

**Install using Homebrew**

If you are using Mac, you can install the Yext CLI using [Homebrew](https://brew.sh/). If you don’t already have Homebrew installed, follow the installation instructions on the [Homebrew](https://brew.sh/) site first. Then, you can run the following command to install the Yext CLI on your machine: 

```cli
$ brew install yext/tap/yext
```


If the Yext CLI is already installed, you can upgrade your version with the following command:

```cli
$ brew upgrade yext
```


**Debugging**

If you run into problems installing or running the CLI, look through the following debugging steps:

1. Make sure which yext outputs /usr/local/bin/yext. If not, run the following command and then open up a new bash shell before running the CLI again.
        
    ```cli
    rm -f <output of "which yext"> 
    ```

2. Make sure there is no alias for yext with alias yext.
    
3. Run brew untap yext/tap and then brew install yext/tap/yext.


## Windows

**Install with MSI Installer**

If you are using a Windows machine, we recommend installing with MSI Installer. 

1. Download the Yext CLI MSI installer for Windows: http://yext-cli-pub.s3.amazonaws.com/cli/windows/yext.msi

2. Run the downloaded MSI installer and follow the on-screen instructions. By default, the Yext CLI installs to `C:\Windows\system32`

3. Open Powershell and run `yext init` to get started.


## Linux

If you are using Linux, The Yext CLI can be installed via wget.
wget https://yext-cli-pub.s3.amazonaws.com/cli/linux/yext


## Download the Latest Executable

You can download the latest executable directly here: 

Mac: https://yext-cli-pub.s3.amazonaws.com/cli/mac/yext
Windows: https://yext-cli-pub.s3.amazonaws.com/cli/windows/yext
Linux: https://yext-cli-pub.s3.amazonaws.com/cli/linux/yext