## WSL

### Why so slow?

WSL2.0 uses a virtual ext4 filesystem, which is about as fast as you'd expect it to be. However, if you ever have to access the baseline Windows environment -- ```/mnt/c``` etc -- there's a translation you have to go through that slows things down D R A S T I C A L L Y. 

### Git Don't

Don't mix WSL git and git for windows, either from MinGW or the shit they have as an "app." It'll work, but if you push from one after the other, it's going over write __all__ the files in question, not the diffs as it should. Not sure why that is, worth looking into at somepoint. Probably something with how git handles nodes it can't read or a binary diff between the two systems. 

### On that (git) note

Christ git you have my ssh keys, can't you pull my email from that god damn. I guess it makes some sense but still. 
Do I want to go through the effort of signing my commits? On the one hand, pain in the ass and not really much of a concern. On the other, that sweet sweet green badge next to my commits; never say gamification doesn't work. 