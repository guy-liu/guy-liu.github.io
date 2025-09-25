---
title: Moving to Gigabit (Finally)
date: 2025-09-23 23:00:00
categories: [Networking, Hardware, Home Lab]
tags:  [Networking, Switches, Home Lab]
---
A few weeks ago, I finally got round to upgrade my home network switch from 100Mbps to 1Gbps. This doesn't sound particularly interesting, and you'd be forgiven for thinking that I am at least 20 years late to the party. But through this, I came to a realisation that is often overlooked in today's culture - how much value we get from a piece of equipment, isn't always down to its specifications or cost.

## My Old Pal

![Front of Switch](/assets/images/2025-switch-front.jpg){: width="868" height="311" .w-50 }
_Cisco Catalyst 3560 8 Port PoE Switch_

My old switch was a Cisco Catalyst 3560 I bought off eBay in the late 2010s. I bought this particular switch because:

- It uses Cisco IOS (not to be confused with Apple iOS) so I can learn and practice Cisco CLI commands
- It has PoE (Power-over-ethernet). Not often a feature for home use - but this helps me to reduce the amount of the power adapters under my desk and makes testing PoE devices like IP phones and WiFi Access Points a doddle
- It is small to comfortably fit in the spot I want and is passively cooled - no annoying fan noise to distract me
- It supports VLAN, as I need it for my home and lab network and my main Internet router is virtualised
- It has lots of enterprise features (STP, SNMP, RADIUS, SYSLOG) but is affordable. I think I paid around £30 for it.

The fact that it was a 100Mbps didn't really bother me. The job it *needs* to perform is to get local devices connected to the Internet. Even today, my broadband connection is a "mere" 65Mbps. So 100Mbps is more than fast enough.

## My New Pal

My "new" switch is a NETGEAR ProSafe GS110TP. It has 8x Gigabit PoE ports and 2x SFP ports. I reckon it is about 10 years old and a kind colleague of mine had given it to me as a gift to "get me to the 21st century". 

This works perfectly for me, as by now, I no longer have the needs to practice Cisco stuff. I wanted to "future proof" my network for the days when I might upgrade my Internet connection to more than 100Mbps. Given quite a few of my colleagues already has 1Gbps connections, we are probably not too far from my ISP moving the minimum package to greater than 100Mbps!

I also took this as an opportunity to tidy up my "home lab" so I got some new patch leads. I'm rather pleased with the end result. With the filing unit and printer in front of it, the whole setup is nicely tucked away and is quite non-intrusive. I run my entire home lab on one Lenovo M900 Tiny with a 6th Gen i7 processor (the old M900 Tiny with the i3 processor is now serving as a spare).

It only has a single network port, but it hosts my main Internet router and a few other "production" VMs as well as a bunch of lab VMs. Despite its modest physical footprint, it has managed to host more than 10x running VMs at one point - but that's for another post.

![Home Lab](/assets/images/2025-homelab.jpg){: width="3102" height="2016" .w-50 }
_The newly tidied up home lab_

## A Word on Home Labs

Many IT professionals would consider 100mbps to be antiquated. But for me, I can probably count on one hand the times that I would have noticed a difference if I had a Gigabit switch over the years I've had it. But the learning and practical hands-on experience I have gained from it is huge. What causes us to consider a perfectly functional piece of equipment obsolete?

Working in IT or cyber, you often don't naturally gain the hands-on experience needed to progress to the next role, especially if you want to move to a slightly different specialisation. e.g. moving from IT to cyber. This issue is more pronounced for entry level jobs, but I think it does affect professionals already established in their career as well. The fact is, because technologies used in this field is really diverse, and most are moving at such a pace, there is simply not a lot of well-established resources or methods that can equip you with the hands-on skills you need for the job.

For me, building home labs is *the* best way to gain new practical skills in order to advance your career. This is where these seemingly "obsolete" dull-looking metal boxes really shines. Speaking as a hiring manager of an IT service provider, I often don't have the luxury of hiring someone that has skills and experience on the exact technology stack we use. In these cases, I will have to look for candidates who can demonstrate transferrable skills that allows us to train them up relatively quickly.

This provides a great opportunity for individuals who's looking to move into a new role - those weird and wonderful projects you have built in your home lab, with niche requirements and creative solutions, can say a lot about your ability to learn new things with minimal supervision, to solve problems with independence, to carry out longer term projects with persistence in order to reach completion - the list goes on.

So… keep hold of those old kit, keep on building and experimenting, and most of all, keep learning. The world will be a better place as we do that. 

What's your favourite "obsolete" kit and why?
