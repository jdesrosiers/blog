---
layout: post
title:  "Conquer and Divide"
date:   2017-05-04 22:00:00
categories: XP
---

One of the criticisms I heard about agile is that it doesn’t scale.  It’s nice for small teams, but once you get to a certain size, some layer of management is necessary to coordinate the masses.  I think this is mostly people trying to cling to the familiar, traditional way of doing things.  There are a few real world examples I can think of that seem to contradict that assumption.

Consider the example of a blog like this one.  Creating this site took a team of one.  Just me.  Well of course it only took one person because it’s a really simple project.  Or is it?  A blog might be really easy to create, but there is nothing simple about it.  Think about all the technologies that make a website possible: a web server, a web browser, HTML, CSS, JavaScript, HTTP, search engines, TCP/IP.  We could go on for a while like that and that’s just making the web work.  There is an equally large number of pieces to implement this little piece of the web.  This blog is written using Jekyll, which in turn is built off of dozens of other projects.

So, there are countless people who have contributed to building my blog and we needed no managers between us to make it happen.  First of all, it is not necessary to coordinate with every team that worked on something used in my blog.  Usually documentation is sufficient communication, but sometimes I have to go to the team to ask for features, report a bug, or submit a pull request.  Again, no need for management.  Teams should be capable of communicating directly as needed.

But, what about when it doesn’t work out like my blog?  A couple years back I worked at a company whose developers were divided into three teams.  Just about everything we did involved multiple teams that needed to be in constant communication to coordinate efforts.  That was a case where management was needed.  Our teams didn’t work because responsibilities were divided along business components rather than software components.

Extreme Programming advocates a conquer and divide approach to forming and scaling teams.  Start out with a small team and add people or form new teams as the project demands.  This allows teams to form along the most efficient lines possible thus requiring less inter-team management.  You end up with the dynamic I described with my blog.  Teams occasionally need to communicate, but it’s not nearly to the level that the team would be overwhelmed managing it themselves.

I had a similar plan to fix the teams at my old job that I unfortunately never had the chance to implement.  Instead of having three teams that never change, I wanted teams that continuously formed, grew, shrunk, and disbanded as needed.  Whenever a new project came through the pipeline, anyone can volunteer to lead the project.  That person then assembles a team to get the job done.

This approach has several benefits. One benefit is that it has the effect of spreading knowledge throughout the team similar to the way pair programming works.  One of the problems with our three static teams was that we were very siloed.  I knew my team was learning and growing, but I didn’t really know what other teams were doing.  When my team was learning Test-Driven Development, it was difficult to share what we learned with the other teams because we never worked with them.  With dynamic teams, everyone gets to work with everyone else at some point and learn from each other.

The other benefit is that it’s great for people.  Often times talented people are stuck in lower level positions because there are no positions available.  They end up either leaving or being unhappy.  The ones that do get promoted find themselves unprepared when for the job because they have never lead a team before.  With dynamic teams, someone can start as a lead on a small project and learn from the experience before taking on larger projects.  The dynamic teams model opens up opportunities for everyone.  It allows the best people to rise regardless of seniority.

I haven’t actually seen this model in action, so I don’t know if it will actually work the way it works in my head, but I think it has merit.  As our teams scale we need to be able to embrace change among our teams, not just within them.
