---
title: Capstone
date: 2020-07-07
description: Reflection on my final year capstone project, a Computer Vision powered Garden Sentry IoT device
layout: post
---


A capstone project carries with it certain undertones of importance, finesse, and great deal of effort. Needless to say, my capstone project was none of the above, and to top it all off it was all but canceled due to the global COVID-19 pandemic. It was, however, pretty fun, and gave me some perspective on everything that I've learned studying at University over the years.

### What's a capstone project?

In most engineering schools in Canada, senior year undergraduate students have to form groups of around four or five people to work together and build some sort of novel invention that is hopefully greater than the sum of each of the individual's parts. Usually, the groups have a high degree of freedom to pursue whatever project they want, so long as the level of difficulty is appropriate for a senior year student, there are no dangerous hazards involved, and the scope of the project is realistic (in terms of physical and time constraints).

Being in Computer Engineering basically gives you a wide variety of different software and hardware projects to explore. Of course, many groups did purely software projects, and others purely hardware, but a good deal of projects (including ours) stuck to the nature of ECE and tried to mix software and hardware.

[Full list UW ECE 2020 capstone projects](https://uwaterloo.ca/capstone-design/2020-electrical-computer-engineering-capstone-design)

### Brainstorming Process

As it turns out, brainstorming for a project idea is hard. Since we had a great deal of freedom in terms of projects, my group members and I seemed to have suffered from the [paradox of choice](https://en.wikipedia.org/wiki/The_Paradox_of_Choice).

Some ideas that were thrown around initially:

* a smart bread baker
* a smart plant monitor
* software that recommends restaurants for groups of friends

It also turns out that many ideas already exist, and are on the market already. A quick google or amazon search of any of these will yield thousands of results. Stubborn as we were, we wanted to be more original.

I thought back on anything that would be useful to me or anyone in my family. Randomly, I started thinking about how my mom always complained about how rabbits were always eating our plants. So I mentioned that we could have some kind of smart scarecrow for gardens.

Our team liked the idea, so we brainstormed some more on how it could work. Since rabbits don't really make any distinct noise, we figured that we required vision to identify them. Bam. Now our project had machine learning in the form of Computer Vision.

How would we actually deter the rabbits away? We could have it play an alarm sound, but that would quickly get annoying for the garden owner and any neighbours, especially since quieter alarms would not alarm the rabbits at all. We would need some kind of physical deterrence, like in the form of a turret shooting air or water.

We had thought water guns were an easy thing to model with control software (we were wrong) so we decided to go with that.

Still, how would a user know that the product actually worked? To provide some visual feedback to users, we decided that the project should have a website attached to it, with a gallery of cloud-based video snapshots of the device shooting the poor rabbits in action. Now we can say another buzzword - IoT enabled.

And so our project finally had legs, even if they were all just conceptual. Being the uncreative engineers that we are, we decided to give it the name "Garden Sentry".

### Planning

The course UWaterloo makes us take for our capstone project does things pretty thoroughly. The planning process involves creating functional and nonfunctional requirements, as well as coming up with criteria to evaluate those requirements. It also required us to create a block diagram, which I had a bit of fun making since I'd never done something quite like this before.

|![Garden Sentry Block Diagram](https://i.imgur.com/fguwNY2.png)|
|:---:|
|*Garden Sentry Block Diagram*|


### Execution

Once we had the planning done, we had to shop for parts and write more detailed requirements for the course requirements. I'll save you the boring paperwork and skip to the fun details.

In the end, the hardware for our sentry consisted of:

* An NVIDIA jetson for running our Computer Vision application and control software
* A servomotor (from a raspberry pi kit)
* An electric water pump
* A plastic hose and nozzle
* A bunch of wood 2x4s
* A camera and an infrared sensor
* LED Floodlight

### Cloud Backend

Most of my contribution (other than report writing, which was mostly shared by all members) was handling the web application portion of the _Garden Sentry_, which consisted of a React front end of a live video gallery of "Defence Incidents" showing poor rabbits getting pelleted by water, writing the agent software which uploaded said videos from the jetson to a group managed Google Storage bucket, and a SQL database for storing video URLs and descriptions. With GCP, it was fairly straightforward.

|![Web Architecture](https://i.ibb.co/TkwzsMS/web-arch.png)|
|:---:|
|*Web Architecture*|

Both [backend](https://github.com/montagao/gardensentry) and [frontend](https://github.com/montagao/gardensentry-ui) repos are available on my github.

### Demonstration

Of course, none of this would matter if the thing didn't actually work.

Luckily, there's video evidence that it (sort of) does:

<iframe width="560" height="315" src="https://www.youtube.com/embed/P_gJE73BijM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


Debugging view:

<iframe width="560" height="315" src="https://www.youtube.com/embed/wdaB4Qs_Iyk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Symposium

Typically, the capstone project climaxes with a stuffy engineering building and groups of surprisingly presentable engineering students showing off their year long efforts to the rest of the school in what's known as the Capstone Symposium. For me, it meant going up to the booths of people you knew and asking them purposely dumb questions like "Can it run Crysis?"

| ![What I missed out on](http://danhadi.com/blog/wp-content/uploads/2010/03/body_motion_analyzer.jpg.jpg) |
|:--:|
|*Looks cool, but I don't think it can run Crysis.*|

Unfortunately for us (this was around February 2020), COVID-19 hit pandemic status, and the symposium was cancelled with no alternatives. Not long after, all in-person classes were cancelled too. People felt a mix of relief and disappointment, but when these things happen they're really out of our control, so I felt pretty indifferent.

|![Our final poster design](https://i.imgur.com/pxqnxSu.png) |
|:---:|
|*Our final poster design, unfortunately never saw the light of day*|

### Final Thoughts

Even though our Capstone was cut short by COVID-19, I enjoyed it far more than I thought I would.

Truth be told, I had a very pessimistic outlook on my whole education up until this point, because we never really build anything creative on our own in our regular courses. Going into this, I just wanted to get it over and done with. Near the end, I was feeling weird sense of pride and satisfaction.

Capstone is rewarding in that sense because you can really put your own knowledge together and understand your own capabilities, given your knowledge of eletrical and computer engineering, as well as understand how a team of individuals can combine their efforts and make something much better than just the sum of each of their parts.

We may not have been able to have much to show for it this time, but next time I build a somewhat challenging, multidisciplinary project, I'll have the much needed confidence of being able to say "Hey, I can actually do this!"
