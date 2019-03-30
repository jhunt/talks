Docker Docker Docker Docker - Nesting cgroups & You!
====================================================

**Categories:** docker, cgroups, virtualization, containers

**Audience:** intermediate; must understand basics of Docker



Elevator Pitch
--------------

You wouldn't virtualize a VM, so you shouldn't containerize in a
container, right?

Actually, it's a bit more nuanced than that.  Let's take a tour
through the nuts and bolts of Docker, Linux cgroups, and explore
the pros and cons of nesting containerization.


Description
-----------

While you _can_ run a hypervisor inside of another hypervisor, the
conventional wisdom is that you shouldn't.  In fact, you shouldn't
even think about it.  Or even consider it.  We probably shouldn't
even be speaking about it.

Does the same taboo hold in the land of Docker?  I've dealt with
several containerization platforms, from Docker to rkt to runc to
Cloud Foundry's Diego Runtime, and I've had some engaging and
preconception-smashing discussions with some really smart people
on this topic.

The truth is: you can safely nest containerization.  I know.  I
didn't believe it myself either.  In this talk, I'd like to walk
you, my beloved audience, through the technology, and into the
epiphany of **why** nesting containers isn't necessarily the
performance nightmare you may have thought it was.  We'll explore
the nuts and bolts of Docker, vis-a-vis Linux cgroups namespaces,
and get into the nitty-gritty of what it means to run Docker,
inside of Docker, inside of another Docker!


Selling Myself
--------------

I've been active in the Cloud Foundry scene, primarily focused on
the open source side, for a few years now, and in that time I've
seen two different bespoke container runtimes come and go (DEA and
Diego); I've seen warden (VMWare's container runtime from way
before it was cool to have a container runtime) morph into garden
(when they rewrote it in Go), and then be replaced almost
wholesale by runC.  Before Cloud Foundry, I experimented with BSD
Jails (ca 2006) and Linux LXC (roughly the same time) when they
came on the scene.  At one point I famously said "Why do I need
Docker when I have _chroot_?"

I've given talks at Cloud Foundry summit, and at employer and
customer events.  I've conducted medium-to-large training classes
on Cloud Foundry, data services, data protection, and automation.
I even tell jokes!


Shop Log
--------

- Submitted to _Devops Days Buffalo 2019_, Mar 29 2019.
