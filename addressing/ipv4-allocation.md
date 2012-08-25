Routing Policy
==============

As a federation of small wireless networks, XXXX maintains a routing
policy distinct from any one upstream ISP or peer. The first such
upstream network is AS786 (JANET), the interconnection being at UHI
facilities at the college (proper name?) on the Isle of Skye. A second
independent interconnection is to be made at Mallaig.

XXXX also intends to establish a presence at the Scolocate facility in
Glasgow and to maintain private peering arrangements at the internet
exchange there with an open peering policy.

Resilience of the network is critical to providing a stable, reliable
Internet service in this presently underserved area especially as the
communities come to rely more and more on our network for their
communications needs, including Voice over IP facilities as well as
vanilla Internet access. In order to engineer this resilience, we
require control over addresses and routing policy.

Note that for this to be possible a minimum of a /22 allocation of
provider-independent addresses is required for it to be possible to
announce this address space into the default-free zone, and, of
course, an autonomous system number with which to make the
announcement.

Current Address Usage
=====================

There are currently 10 backbone sites in the Loch Horne / Sound of
Sleat / Small Isles area. Each site consists in two or more
routers. There are point-to-point links between these sites and at
each site there is one or more routers with a point-to-multipoint
arrangement serving between 2 and 20 client sites.

Present Requirements:

    Description                                          Allocation
    ---------------------------------------------------------------
    /32 for each router for loopback interfaces             /27
    /30 for each of 15 point-to-point links                 /26
    /29 for LAN on each heavily populated mask              /26
    /29-/27 block for each point-to-multipoint interface    /24
    /30-/29 block for each user requiring public
        addressing for, e.g. SIP telephones or other
        services                                            /24
    ---------------------------------------------------------------

The smallest CIDR block that will satisfy current requirements is
therefore a /22.

Note that the network is currently provisioned with RFC1918 addresses,
with address translation 2-3 levels at some end-user sites. This is
unsuitable for several reasons, namely that the usual facilities with
IP routing for resiliency are unavailable and applications such as
VoIP that require end-to-end connectivity in order to function
correctly and predictably cannot be reliably used.

Projected usage
===============

It is expected that the size of the network will at least double over
the the next two years. Given that this is the case, it may be
appropriate to allocate a block of size /21 in the first instance to
permit growth.

Reporting, etc.
===============

Upon allocation of the requested addresses and autonomous system
number, we will put them into service within X months and of course
undertake the standard obligations of holders of RIPE resources,
particularly SWIP'ing each single block of /29 or larger with correct
and up-to-date contact information, etc..
