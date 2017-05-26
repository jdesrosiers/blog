---
layout: post
title:  "Continuous Improvement"
date:   2017-04-25 22:00:00
tags: [XP]
---

A while back I had the opportunity to introduce agile practices to the company I was working for at the time.  The company was in a transition period and I was determined seize the opportunity to improve the way we work.  The problem was that I no practical experience with these practices.  I knew how it was all supposed to work in theory, but I didn’t really know what I was doing.  It was the blind leading the blind.

In “Extreme Programming Explained”, Kent Beck divides the XP practices into two categories: primary practices and corollary practices.  The idea is that the corollary practices are more challenging and build upon the primary practices, but even the primary practices can be difficult to implement and are often built on even more fundamental practices.  The more you can break it down the better, especially when you are figuring it out on your own.  Even if what you are practicing isn’t exactly where you want to be, it could be a valuable stepping stone to get you to where you want to be.

For example, TDD is one of XP’s primary practices and one of the first things my team tried to learn.  Going from not testing at all to writing tests first is a pretty big leap.  So, we started off writing tests last.  We made plenty of mistakes.  Our first tests were too coupled to our code, so we learned to test behaviors rather than methods.  People weren’t remembering to run the tests before checking in the code, so we introduced continuous integration to run the test automatically.  As we got more comfortable with testing, we would start doing some tasks test-first.  We probably went through five distinct stages on our way to test-first development.  Even though test-last was not where we wanted to be, it was crucial in helping us get to where we wanted to be.

