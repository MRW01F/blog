---
title: Manually Adding PPA In ParrotOS
published: true
---

**ParrotOs** is great Distro for pentesters and NO.1 competitor of **kali linux** but some features are disable for security purpose see their [Documentation](https://docs.parrotlinux.org/) for more information, hear we are going to add launchpad's Proprietary GPU Drivers ppa.

>**WARNING: this guide is just for information purpose however it is not recommended to do, because ParrotOS is rolling relese so adding a ppa can be risky and may break your system.**

In other debian based distro, you can add ppa by just typing simple following command...

`$ sudo add-apt-repository ppa:graphics-drivers/ppa`

But In ParrotOS we have to manually take the Repo links and add them in their **source list**, but before we proceed further update & upgrade your syatem first.

`$ sudo parrot-upgrade`

OR

`$ sudo apt update; sudo apt upgrade`

and now go to the repository site for the provider's page, here i am demonstrating by adding launchpad's [Proprietary GPU Drivers](https://launchpad.net/~graphics-drivers/+archive/ubuntu/ppa).
But first make sure you have compatible graphics card before adding ppa or you may have problems later on. So Follow the steps.

<hr>

## 1. Go to the provider's site and scroll down where you can see "Adding this PPA to your system"

<img src="{{ site.baseurl }}/assets/images/adding-ppa-1.png">

here as you can see the mormal `add-apt-repository` command for most debian based distros but we dont need that, Click on the `Technical details about this PPA` to see the actual links of repo.

<hr>

## 2. Select 

<img src="{{ site.baseurl }}/assets/images/adding-ppa-2.png">

Select `Xenial` From the dropdown list to get the repo links OR you can Replace the text which says "YOUR_UBUNTU_VERSION_HERE" with xenial. some of you might think why xenial ParrotOS is based on Buster?, its because this ppa does not have buster repos in it so we are choosing the closest one. (**If add the Buster Repo In the future You might want to select `buster` repo**)

Now your `deb` and `deb-src` will look like this...
```
deb http://ppa.launchpad.net/graphics-drivers/ppa/ubuntu xenial main 
deb-src http://ppa.launchpad.net/graphics-drivers/ppa/ubuntu xenial main 
```

<hr>

## 3. Add these links to your `/etc/apt/sources.list` with any text editor.

>NOTE: remember not to add in /etc/apt/sources.list.d/parrot.list because that mirror list is used by system and it's better not to touch it,

Paste/Append the Links into the `/etc/apt/sources.list` file.

<hr>

## 4. Adding the Signing key

so finally we are going to add the `Signing key`, see the text which says `Signing key:<key>` on the page and text below it.

```
Signing key: 4096R/2388FF3BE10A76F638F80723FCAE110B1118213C
```

We only need the part after the forward slash, So the final key will look like this...

```
2388FF3BE10A76F638F80723FCAE110B1118213C
```
### add Keys using this command..

```
$ sudo apt-key add --keyserver keyserver.ubuntu.com --recv-keys \
2388FF3BE10A76F638F80723FCAE110B1118213C
```

And Now finally update & upgrade Your system. and install your graphic drivers as per your requirements. You can also add microsoft's `vscode`'s repo to install `vscode`, as well as you can add repos for custom `WINE` versions. 

<hr>

## How to Remove PPA

Just delete OR comment out the links form `/etc/apt/sources.list` and update your system.

<hr>
<br />

# Final Notes

Adding PPA in parrotOS is risky and may breake your system, developers highly recommend **NOT** to do that. But the this propritary graphics driver ppa is not causing any trouble (For NOW), I have tested it in parrotOS 4.8 with kernal version 4.8. So before you just go ahead and throw some third party PPAs in the list file, you may want to refer the [ParrotOS Community Forum](https://community.parrotsec.org/).

