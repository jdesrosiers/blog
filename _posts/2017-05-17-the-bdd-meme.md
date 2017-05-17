---
layout: post
title:  "The BDD Meme"
date:   2017-05-17 12:00:00
categories: TDD BDD
---

When we hear the word "meme" these days, it conjures visions of some iconic image with a clever caption.  But, before memes were pictures of cats, the word "meme" had a more profound meaning.  The word "meme" was coined by Richard Dawkins in his book, "The Selfish Gene" [^1].  As defined by Richard Dawkins, a meme is a thought or idea that replicates, mutates, and evolves the way DNA does with genes.  Memes today are often compared to viruses and the way they spread, but that still doesn’t do justice to the original meaning because it doesn't address the concept of mutation and evolution.  So, in the original sense of the word, even the concept of a meme is a meme that has evolved over time.

Concepts in software are memes too.  One particular meme that is the subject of this post is BDD.  Today, BDD and TDD are considered two different things with two different goals.  TDD is for unit tests and BDD is for acceptance tests.  There are at least three things wrong with that statement, but as is typical of memes, it's often not the best interpretation that wins but rather the one that gets repeated the most or the most fervently.

The first problem is Kent Beck's use of the term "unit" when describing Test-Driven Development.  This was a poor choice of words because there is already a concept of unit testing in the software testing field.  It is understandable that people assumed that TDD used the same definition, but what Kent Beck meant as a unit test was a test that runs in isolation [^2].  It is not dependent on other tests.  Each test must setup the state it needs and do any cleanup when it is done.  It is in this sense that a unit test in the TDD sense is a unit.  It is self contained.  It can run by itself or it can be run along with any other unit test in any order.

Unit tests in the TDD sense were never intended to be limited to low level tests as they are in the software testing sense.  Kent Beck used the terms zoom-in and zoom-out to describe the concept that tests can and should be written at any and all levels of abstraction.  Zoom-in and test very specific behaviors, but also zoom-out and test higher level behaviors.  Sometimes you need to be thinking at a low level, other times something higher level is needed.  Other times you write a higher level test to help figure out what lower level tests you need.  Often times I will purposely write tests at a higher level than I otherwise might because I expect that the lower level classes or methods are likely to change.  Having tests at a higher level allows me to more more agilely rewrite or refactor the lower level parts.  If later the implementation stabilizes and I want to reuse those lower level modules somewhere else, I’ll go back and write test for them.

Just as TDD got pigeonholed into low level tests, BDD got pigeonholed into being only about high level tests.  If you go back and read Dan North’s original blog post introducing BDD [^3], you will see that BDD is little more than a different vocabulary to help people think about writing tests as testing behaviors.  This was not a new concept.  Dan North just came up with a better vocabulary to express the concept.  The thing that is most recognizably BDD is the Given-When-Then vocabulary to describe high level behaviors.  But, BDD is low level as well.  Using "should" instead of "test" for low level tests is also a BDD concept.

However, just because BDD is little more that a change in vocabulary doesn't mean it isn't a valuable contribution.  I prefer the BDD vocabulary to the original TDD vocabulary.  My favorite part of BDD is the concept of tests as executable specifications.  If we take care to give our tests good descriptions, the test report could read like a requirements document.  A requirements document that can’' get out of sync with the code could be pretty valuable.

I would describe my practices as using TDD with BDD vocabulary.  But, saying something like that in the company of most software developers results in confused stares.  The BDD meme has changed enough that the original concept is almost unrecognizable.  BDD is far from the only meme in the software world that has changed significantly.  Often times a new term is coined to reclaim original meanings.  Maybe BDD needs something like this, but I’m not sure adding more terms to the lexicon is the right approach.  I’m not sure what the answer is, but talking about it is always a good step.

[^1]: [The Selfish Gene, Richard Dawkins](https://www.amazon.com/Selfish-Gene-Richard-Dawkins/dp/1491514507).  Memes are described in Chapter 11 - Memes: the new replicators
[^2]: [Test Driven Development By Example, Kent Beck](https://www.amazon.com/Test-Driven-Development-Kent-Beck/dp/0321146530) Kent Beck describes what he means by "unit test" in Chapter 32 - Mastering TDD
[^3]: [Introducing BDD, Dan North](https://dannorth.net/introducing-bdd/)