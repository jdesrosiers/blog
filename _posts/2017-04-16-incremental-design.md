---
layout: post
title:  "Incremental Design"
date:   2017-04-16 22:00:00
categories: XP
---

Agile has revolutionized the way we think about software development.  There are many flavors such as Scrum, Kanban, and Lean.  If you look at the Scrum framework for example, it defines things like meetings and how to split and prioritize work.  This is all valuable for managing a project, but there is no guidance to help developers to be more agile in their work.  If the developers don’t know how to be agile, there is no way the project as a whole is going to be agile no matter what framework you have around it.

After all these years, only Extreme Programming (XP) has ever defined a set of specific technical practices for agile programming.  Of the 13 primary practices identified in Kent Beck’s Extreme Programming Explained, five are technical practices: Pair Programming, Ten-Minute Build, Continuous Integration, Test-First Programming (a.k.a Test Driven Development), and Incremental Design.

Pair Programming, Test Driven Development (TDD), and Continuous Integration (CI) are all practices that most people in the software industry are at least aware of, but the one I want to talk about today is one that is often overlooked: Incremental Design.

A little while ago, I was involved in a discussion about whether software architecture is dead or dying and what role agile has played.  The debate was sparked by a speaker at a conference who claimed that the fast pace of development today has led to people no longer putting effort into developing an architecture for a system.  Despite being the author of a software architecture textbook, he didn’t see this as necessarily a bad thing, just an artifact of the fast pace of the industry.  Most systems are obsolete and need to be replaced in a few years anyway, so why put the effort into a strong foundation.

I’m not sure he really believed that.  I think he was mostly trying to provoke discussion.  The value of having a well designed system is cumulative.  A messy system slows down progress very early on.  It’s not like a toaster that works smoothly for years until one day its parts start to give out.

Incremental Design is how we reconcile the problem of having a strong foundation and being agile.  Architecture and design don’t happen at the front of the development cycle anymore, it happens throughout the project.  If we are continuously improving the design as we learn and better understand the needs of the system, we often come up with something better than we would have had if we designed something upfront.  I have yet to see a project that goes exactly as planned.  Whatever design is determined upfront, will almost certainly change drastically by the time you get to the end of the project.

That being said, Incremental Design is not easy.  You can’t just decide to do it and see improvements immediately.  Like TDD, it takes skill and practice to do it well.  You have to know what makes a good architecture and design in order to get there.  You have to be skilled at refactoring techniques and you need to have good set of tests that allow you make changes without fear of breaking things.

The study of software architecture and design is just as relevant as it always was, but it needs to shift its focus from a design upfront activity to an incremental activity.

