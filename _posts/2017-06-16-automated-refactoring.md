---
layout: post
title:  "Automated Refactoring"
date:   2017-06-16 12:00:00
tags: [refactoring, TDD, automation]
---

A couple years ago I listened to a podcast (I don't remember which one) where they were talking about the importance of refactoring.  Generally I agree with that sentiment, but they were taking it to an extreme that I've never heard before.  They were saying that TDD is *not* especially important, but relentless refactoring is one of the best development practices you can have.

It took me a while to wrap my head around that perspective.  I've always thought of TDD and refactoring as mutually supporting practices.  Martin Fowler makes this assertion in "Refactoring" [^1] as well.  Even though a refactoring should only change the structure of the code and not its functionality, you still need a solid set of tests to ensure that you didn't inadvertently introduce some new or changed behavior.  In my experience working with code that doesn't have tests, I've been reluctant to refactor for fear of breaking things.  No matter how careful you are, we all make mistakes.

Eventually I realized that the people in the podcast were talking in the context of C# using ReSharper.  They were talking about automated refactoring where human error is removed from the equation.  That was why they minimized the necessity of having tests.  Martin Fowler hints at this as well in "Refactoring" [^1].  At the time the book was written, automated refactoring didn't exist yet.  He doesn't come right out and say it, but he seems to suggest that testing is so important because automation is not yet available.

This is intriguing, but even with really good refactoring tools, I'm not ready to say tests are no longer important for refactoring.  I've only used ReSharper (and C# in general) a little bit, but my experience with automated refactoring has never been good enough that I can rely completely on the tools.  Maybe ReSharper is that much better, but I doubt it.  Automating refactoring saves you typing, but you still have to closely monitor what it did to ensure it didn't do something weird or unexpected.  In my experience with automated refactoring, weird or unexpected outcomes are very common.  Automation is certainly much safer than refactoring manually when you don't have tests, but I’d still rather have my tests monitor the automated refactorings than having to review every change manually.

It has also been my experience that automated refactorings are often not inclusive of all refactoring I might want to do.  Again, ReSharper might be better, but I'm skeptical that it's good enough that I would rarely need to refactor manually.  Therefore, I still need those tests for when I need to refactor manually.

Finally, not all languages are well suited for automated refactorings.  The strong typing and general rigidness of languages like C# or Java make them fairly ideal to automate refactorings, but automation is not so easy in many other languages.  So, making the statement that TDD is not necessary for refactoring, at best, depends on the language.

Without a healthy dose of AI, automated refactoring is mostly just a way to save a few keystrokes.  It can give you more confidence to refactor if you don't have tests, but automation is certainly no *substitute* for having tests.  And all of this only addresses testing with respect to refactoring.  There are still many reasons why you should TDD outside of the context of refactoring.

[^1]: [Refactoring, Martin Fowler](https://www.amazon.com/Refactoring-Improving-Design-Existing-Code/dp/0201485672)
