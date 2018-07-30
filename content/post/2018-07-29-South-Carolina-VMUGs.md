---
title: "South Carolina VMUGs and Modern Data Centers"
date: 2018-07-29T21:14:27-04:00
draft: true
tags: ["VMUG","Virtualization","IT Resiliency","2018"]
---

This past week, I had the amazing opportunity to speak at two different VMUG events.
The first group I got to speak with was the [Columbia, SC VMUG](https://community.vmug.com/communities/localcommunityhome?CommunityKey=48abd35e-f8de-4128-8e25-3fdffdbac9be) and the second was with the Hilton Head / Bluffton, SC VMUG group.
Both of these events had some very smart people in the room which led to quite interesting conversations.

<!--more-->

![Bluffton Thank You!](/img/bluffton_vmug.jpeg)

One conversation I had with an attendee got me thinking about where we once were as it relates to IT Resiliency and how far we have come from the days where bare metal ruled the data center.
Back in the "good old days" almost nothing was virtual.
We didn't have "cheap and deep" storage that we could afford to use as a backup target.
Full backups were kicked off every Friday night and incrementals or differentials every other night.
These would always go straight to tape.
Application consistency across multiple servers?
Not a chance.
Your off-site storage provider of choice would always be at the door to pick up the tapes from last night way too early.
If a file was deleted or lost, it would take hours to just get the tapes back.
If a server went down and could not be restored, it could take days.
There were no secondary data centers.
If you lost an entire site due to an "Act of God" you were calling your off-site storage provider, recalling tapes (and pray that they would work), and hopping on a plane to attempt to restore everything on rented hardware.
You were lucky if you had spare hardware to test any of this ahead of time.

Now look at where we are.
Disk to Disk backups are now the norm.
Most organizations are leveraging the cloud for long term retention and have gotten out of the tape game completely.
Full backups now happen once and then "forever incrementals" as approved backup windows have shrunk to be almost non-existent due to the increasing nature of 24 x 7 businesses.
While backup windows have shrunk, this "forever incremental" technology now gives us the ability to take backups more frequently of our most important servers and workloads.
Restoring a file in minutes is now table stakes for any organization.
Restoring an entire machine?
Thanks to virtualization, this is now child's play.
Recover an entire application stack server set to the exact point in time?
Recover an entire data center in a different part of the country?
Thanks to [Zerto](https://www.zerto.com), both of these are now child's play as well.

This isn't to point out to everybody "how good you kids have it" or any such nonsense.
This is just to point out where we were and how far we have come in such a short amount of time.
I am in awe of the technology that many outside the realm of the data center take for granted.
Serverless?
Come on.
I would hope that we all know the vital role that both servers and IT Resiliency will play in the "Serverless Revolution."
At the end of the day I can't wait to see what the next years of technological advancement will bring us and what we will look back upon in wonder of how we ever did it that way!

What are your thoughts? Please feel free to leave them below.