[![Codacy Badge](https://api.codacy.com/project/badge/Grade/ad3a390ed44e4ad28b786d760b2dd5f6)](https://www.codacy.com/app/Xmetalfanx/linuxSetup?utm_source=github.com&utm_medium=referral&utm_content=Xmetalfanx/linuxSetup&utm_campaign=Badge_Grade)

# NOTE: THIS is under heavy construction

# March 31, 2020 Update:

Things may be delayed as my main rig (laptop) has a keyboard issue that needs to be repaired and with everything going on in the world,
	A) they are very backed up
	B) I am not sure when I can send my laptop out to get fixed, or if i even can right now
	C) I have NO idea when it may come back if i can .... if say 3-5 extra days vs normal .. I am cool with that if it comes back fixed ... I am thinking it may be alot longer now ... just due to everything ... because of this I do not want to screw up my only other rig i was using for testing.

# Xmetal's Linux Scripts

## Introduction

A problem SOME users, even if they are experienced have when setting up some distributions, is all the post install tasks they have to do to setup a "workable" system. The tasks may not be difficult to do, but just rather they are time consuming. These scripts can hopefully give people a "helping hand" getting different distro bases set up.

While The main distributions listed are meant to be "Distro family bases", not ALL scripts are practically on all distros. For example a few of the "Fedora scripts" are already pre-done for you, if you use Korora.

## Disclaimer

-   Standard Disclaimer about how I am not responsible about what scripts you run on your own computer or what mistakes may occur

## Requirements

Some of these are auto-installed when the script is first run ... others I may add to "auto install" later

-   `wget`
-   `curl`
-   `lsb` (different package names on different distros ) type packages
    -   so lsb_release \* can be run
-   `inxi`
    -   (? if it's autoinstalled or needed)
    -   ... even I am not 100% sure about this one, but for later "DE/Distro" detection, inxi seems needed
-   `git`
    -   this is to git clone the scripts; however, from the github or gitlab page for the scripts, there are ways to download the repo in a .zip form too ... in this case `git` is not "needed"

## Thanks

-   Too many to list them all

-   While I was likely to do this anyway, it is people like [Midfngr](https://www.youtube.com/user/midfingr/undefined) that inspire me to help other, though this entire idea started with no menus, and just a way for ME TO AUTOMATE some post distro install tasks, the idea this could help others is why it has grown so much

-   Thanks to [Matthew Moore](https://www.youtube.com/user/MrGizmo757/undefined) for much of the Arch info in his Arch install notes. Matthew Moore's Debian install guide also helped me add the Codec section for Debian... credit goes to him for that and figuring out in some cases you need to add some of the packages before others (vs having it all in one big "sudo apt install" line).  Thanks Matt

## Known issues

### Some RPMs are not being signed by the devs

-   I can not say this is the case for all apps; however, to my knowledge GitKraken and Atom (see <https://github.com/atom/atom/issues/16499> for more info on Atom) ... they recommend ignoring it ... .and it still does work I can confirm but this doesn't seem like a good idea.

### KDE Neon Updating Output

-   April 2020 update: I am not sure this is still an issue
-   The output of the updating is not as clean as apt-get upgrade or apt upgrade ... not sure if I can really do anything as that is on the way they upgrade via the CLI and has nothing to do with my scripts

### MakeMKV Compiling

not sure this is an issue but IF something ever goes wrong (this is sort of a note-to-self)... check out [This commit](https://github.com/Xmetalfanx/linuxSetup/commit/58b1a2bb2e11817ffc01f8f645a5323ed4430602)

### Ubuntu 14.04 support MAY not be the best

-   while it's not end of life yet... I do not beleive ... I cant say that may scripts work great with 14.04 based LTS releases ... 16.04 (at the moment...) is as far back as I am really checking

* * *

## Links to other useful projects similar to this

### [Mr Sam Hewitt's Main Page and Scripts](https://github.com/snwh)

-   [Fedora Post Install Scripts](https://github.com/snwh/fedora-post-install)
-   [Solus Post Install Scripts](https://github.com/snwh/solus-post-install)
-   [Ubuntu Post Install Scripts](https://github.com/snwh/ubuntu-post-install)

Thank you to Mr. Hewitt for some code ideas, when browsing through his projects

-   Also thanks to [Fedora Install Script](https://gist.github.com/KingsleyOmon-Edo/711c0a79c29d532840bb5cae55b7c2d6) for ideas coming in future commits (posted this here to remember to give credit, before hand)

-   More thanks go to KittyKatt and screenfetch's contributors [Screenfetch on Github](https://github.com/KittyKatt/screenFetch)

* * *

## How to download via git

-   ### In Arch:

    `sudo pacman -S git`

-   ### In Fedora:

    `sudo dnf install git`

-   ### In OpenSUSE:

    `sudo zypper install git`

-   ### In Ubuntu:

    `sudo apt install git`

    -   if that doesn't work `sudo apt-get install git`

## How to get the script via git method

In a Terminal run `git clone https://github.com/xmetalfanx/linuxscripts.git && cd linuxscripts`

## How to run the main script file

1.  Open a Terminal
2.  Navigate to the root folder you extracted the LinuxScripts archive to
3.  type `bash xmetalLinuxScripts.sh`

* * *

## Goals

1.  To have scripts I can run on various distros that automate many of the post install "out of the box" tasks that I always perform anyway.

-   Distro families to be included are

        - Arch
        - Debian
        - Fedora
        - OpenSuse
        - Solus
        - Ubuntu

* * *

## [Xmetal's Task Info](/documentation/xmetalTasks.md)

-   This is where the original idea for all of this came from ... These are "for me" where instead of "going to this menu and selecting this, and that menu and selecting another thing, I can just run this one "batch" set of tasks and do it all at once.

* * *

# Test Results

-   Please note that I do not run all versions of all distros, so in some cases, (example) OpenSuse 15.0 Leap may say "fail" for that task, but OpenSuse Tumbleweed says "Pass" and I may have fixed the issue for Leap too ... but If i dont see it pass on an actual install, I will leave what I saw with my own eyes

## Distro Testing

-   [Arch Based Task ](tests/archBasedTests.md)
-   [RPM Based Distro  - Fedora and OpenSuse ](tests/rpmBasedTests.md)
-   [Solus Task ](tests/solusTests.md)
-   [Ubuntu Task ](test/ubuntuBasedTests.md)

## Software Tests

-   [Theming Testing ](tests/themingTests.md)
-   [Web Browser Installer Tests](tests/browserImstallerTests.md)

#### Extra Notes

-   note: move this to better documentation section, later The repo used for an option to install Audio-Recorder on Debian is <https://www.deb-multimedia.org/>
