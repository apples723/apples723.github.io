Git is installed on MacOS by default. It's not the offfical distro, but the Apple distribution of git. 

## Overview

This guide goes over installing the official distro via ```homebrew```. First we will install Homebrew and then install Git. Since Git is installed by defualt this guide will also walk you through how to change your path to use the official (non-Apple) distribution.

## Step by Step Guide


**Install Homebrew**

_if Homebrew is already installed, you can skip to the Git section_

```terminal
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```


**Update Homebrew to ensure you are on the latest version**
  
  ```terminal
  brew update
  ```

**Run brew doctor to ensure everything is good to go**

```terminal 
brew doctor
```

If all is well, the output should say 

`Your system is ready to brew.`

Now let's get to Git.

**Check your current version of git**

```terminal
git --version
```

If the version of git says something like `git version 2.24.3 (Apple Git-101)` then you are running the Apple version of Git, not the official distribution.

No worries, Homebrew has got us covered.

**Insttall Git via Homebrew**
```terminal
brew install git
```

**Change your local path to the Homebrew version of Git**
```terminal
export PATH=/usr/local/bin:$PATH
```

**Check the version of Git**
```shell
git --version
```
You should now see the current version of git, such as `git version 2.29.2`.

**To upgrade Git in the future simply run**
```
brew upgrade git
```
