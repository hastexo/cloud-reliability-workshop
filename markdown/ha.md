## High availability
in OpenStack


### Back in
# 2012
OpenStack Summit, San Francisco


### arguing
over whether OpenStack
## needed HA


### opposing argument:
# It's hard.


<!-- .slide: data-background-image="//i.stack.imgur.com/jiFfM.jpg" data-background-color="black" data-background-size="contain" -->


What has
# changed
since then?


OpenStack
# API
### High Availability
(now a given)

Note: Has been in vendors' OpenStack products since at least 2013,
using Corosync/Pacemaker stack.


OpenStack
# Storage
### High Availability
(just use Ceph)

Note: Ceph has been the default distributed storage solution for
OpenStack for years. It comes with built-in resiliency and high
availability, and scales almost indefinitely.


OpenStack
# VM
### High Availability
(unification underway)


## Root cause analysis
and automated service resiliency

Note: This is a keynote from the just-completed OpenStack Summit in
Barcelona, with Mark Collier and Ildiko Vancsa from the OpenStack
Foundation, and Ryota Mibu from NEC. What you're seeing is an mobile
phone/data stack that responds, automatically, to "interesting"
failure scenarios.


<!-- .slide: data-background-color="black" -->
<iframe data-autoplay src="https://www.youtube.com/embed/Dvh8q5m9Ahk?start=485&end=555&controls=0&showinfo=0&autohide=1&modestbranding=1&rel=0"></iframe>

Note: What you are seeing here is a combination of Congress and
Vitrage (from OpenStack) with Doctor (from OPNFV). What is being
detected is that an existing service is no longer accessible over the
network, while alternate paths still exist. The system automatically
routes around the failure, which is a classic feature of carrier-grade
resilient systems.