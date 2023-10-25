Codesandbox-clent(If this pull request is approved) has just add support for fnm and systemd so what does that mean. here the 
**who**(codesandbox frog-o and others) **what** and  

# Why FNM ?
In summary 
 - Easier to have one config
 - FNM already metion in doc and  arguably fast
 - Multipe project requier differnt config
# Why Systemd?
In Summary
 - Correct pid reping see  and others.
 - It what people are used to  
 - Arguably cool
 - systemd is better [now](https://www.redhat.com/sysadmin/improved-systemd-podman)

## Systemd details 
 Most of the reason where take after read and working with the     [docker-debian-base](https://salsa.debian.org/jgoerzen/docker-debian-base) image.
 where this info came from from.  
 
 Please also note while systemd used to requier root capabilitys it  is no longer the case [see](https://developers.redhat.com/blog/2016/09/13/running-systemd-in-a-non-privileged-container#the_quest)  and [this](https://blog.while-true-do.io/podman-systemd-in-containers/)

 Even though the last one just show you more how to build it notice no specail flage podmant know how to do the right thing.

## FNM Details 
 It been quite a quest to find the best place to put Node version that requier for your program. Should it be in the enviorment.json in package.conf or in .nvrmc and hard tell where else. Is this realy what you want to do? What happen when you upgrade mode? You would have to reconfig all of these or set an enviorment varible or just rely on one config.  What happen when part of your project uses a new feature of node while other area still realy on the old you whould have to rewrite all of it.  This is arguably a real big problem for monorespotores? What if you want to test againt other version of node? 

 This is where FNM or NVM shine.  You no longer need to worry about these. You simply remove the engine from the package.json and create one .nvmrc file per project it allows for that do. I realy need to say more.
