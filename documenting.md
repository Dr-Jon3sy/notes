### Project Set up

#### Why 

Using this as a space to collect my thoughts on setting up machines for research and development. There's a lot of little things to remember, especially when talking to someone new about all this. 

#### Virtualization

On Windows x64, the only real answer is VMWare. I'm sorry VirtualBox, I love you, my early career was using you with all sorts of ~~messed up~~ quirky Vagrantfiles, but in terms of stability and features (specifically scripting virtual network devices and routing tables) nothing beats VMWare...apart from Broadcom. 

VMWare Workstation Pro 17 is free for individual use...for the time being. Take advantage while we can I guess. Player is supposedly no more but [we can still download it from the CDS](https://softwareupdate.vmware.com/cds/vmw-desktop/ws/17.6.2/24409262/windows/core/). 

[Windows pro x64 1909](https://archive.org/details/windows-10-1909-home-pro-english-x-64)
[Windows home x64 1909](https://archive.org/details/win-10-1909-english-x-64)
[Windows 7 all](https://archive.org/details/Windows7-iso)

8 gigs of memory, 2 processors, 2 cores each is enough for a _fine_ environment. I tend to disable internet access just to stop all attempts to update/send telemetry, very rarely do I actually need that. Be sure to take a snapshot of everything in a pristine state, after installing VMWare tools. 

#### Visual Studio

Visual studio is a fucking memory hog but by god does it do work. Download the community edition, make sure you get the debugging tools. It comes with a shit ton of options, 3/4s of which you'll never need. The one that's absolutely essential is 

[Get it here, check all the fun boxes you like.]

...ok you hate M$ and refuse to use their products and have a deep innate hatred of their tools and don't want to touch them at all. You want to use Microsoft the operating system but don't want to use VisualStudio for _reasons_. Your only answer is MinGW, [which can be found here](https://www.mingw-w64.org/), and is useful for some stuff, but tbh you're going to have a bad time doing any of this without the VS suite. It _can_ be done, but you're making things harder than they need to be. 

#### WSL 

Not needed but incredibly helpful, especially for runing local webservices or when git starts being an absolute pain in the ass. There are many flavours out there, and they're lightweight enough to not take up too much space once downloaded, but you should probably make sure one of them is Ubuntu, or Debian. Probably Ubuntu tbh - for better or worse, it's treated as the default. 

Do yourself a favour and install [oh-my-bash](https://github.com/ohmybash/oh-my-bash). It's got a lot of plugins that make life a lot easier, plus it has an insane amount of themes (for the aesthetics). Be the cool kid with the cool editor. Double points if you figure out how to [install the Synthwave84 theme for Windows Terminal](https://gist.github.com/tiffany352/28412a55045b2db5d9f35fdcedf117e4)

#### Text Editor

Sure you can do evrything in vim or Visual Studio...but ain't no one got time for that. In this year of our Lord 2025, the choices are

* __Visual Studio Code__. Took Atom's lunch and ate it. Runs fast, runs good, and looks pretty doing it. Also is free, though in Microsoft's typical "embrace extend exterminate" worldview that means you have to consent to all the telemtry known to man being sent to the mothership, and you can't make money publishing extensions and a bunch of exhausting things no one cares about. 

* __Sublime Text 3__. Still has its die hard adherents, the original source of multi-cursor drifting. Probably as close to a "perfect" or complete software project out there. It's paid software, but the trial license is unlimited. 

* __Notepad++__ idk I see people use this I figured I should include it. 

#### Git

Set up a github account. Yes they suck. Yes it's necessary. This isn't college, `thing.final-3.actually.c` isn't going to cut it. 

There are a few ways to install Git on Windows - the laziest is to just use WSL to handle it for you. `sudo apt install git` and bob's your uncle. 

If you want it on your Windows machine [github has a good guide](https://github.com/git-guides/install-git) as does [The Official Git Book](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)...which you should read once a year, just on general principle. 

The important thing to do is SET UP YOUR GIT TO USE SSH. 