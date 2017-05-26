---
layout: post
title:  "Intervention"
date:   2017-05-25 22:00:00
tags: [java, scala]
---

OK, Java, we need to talk.  Why do I need to keep repeating myself.  It's getting pretty annoying having to say things three times or more every time I want to use a class.  It's to a point where you pretty much have to use an IDE to be productive.  This is what I’m talking about.

```java
Foo foo = new Foo();
```

See what I mean? That's three "foos".  If I use a lot of `Foo`'s, I'm writing that statement a lot.  But, that's not even the bad part.  What if I want to pass my `Foo` to a `Bar` class and have getters and setters for them.

```java
public class Bar {
    private Foo foo;

    public Bar(Foo foo) {
        this.foo = foo;
    }

    public Foo getFoo() {
        return foo;
    }

    public void setFoo(Foo foo) {
        this.foo = foo;
    }
}
```

There are fourteen "foos" in this code!  Fourteen!  And that doesn't even count the at least two, but probably three more it takes to instantiate just one `Bar` instance.  Seriously, Java, get your head out of ass!  Why can't you be more like your little brother Scala.  Here is Scala's version of the `Bar` class.

```scala
class Bar(var foo: Foo)
```

Two "foos"!  That's all it takes.  Yeah, OK, it's not exactly the same thing.  You could make your member variables public and get your count down to six, but you need those getters and setters.  If later on you need to do something special when you set a variable, you want that setter around so you don’t have to change every line of code that set's a `Bar`s `foo`.

Scala doesn’t have that problem.  `foo` can be made private and getters and setters created without changing the external interface.  That means Scala can forgo creating getters and setters until they actually need for a real reason.

```scala
class Bar(private var _foo: Foo) {
    def foo_=(foo: Foo) {
        // Do something special
        _foo = foo
    }
    def foo = _foo;
}
```

With "foo" mentioned nine times, Scala has a bit more of a stutter than I want to see.  But, this is rarely necessary, especially since Scala avoids the mutability crowd as much as possible.  Side effects are bad for you, Java.  Just say no!  When you are using mutability you tend to expose your privates more that you realize.  Trust me, no one wants that.  Let me show you mean.

First lets assume we have these Foo and Bar classes.

```java
public class Foo {
    private String baz;

    public Foo(String baz) {
        this.baz = baz;
    }

    public String getBaz() {
        return baz;
    }

    public void setBaz(String baz) {
        this.baz = baz;
    }
}
```

```java
public class Bar {
    private Foo foo;

    public Bar(Foo foo) {
        this.foo = foo;
    }

    public String getFoo() {
        return foo;
    }
}
```

Notice that `foo` in `Bar` is private with no setter.  We shouldn't be able to modify it, right?  Wrong!

```java
Bar bar = new Bar(new Foo("foo"));

bar.getFoo().getBaz();        // “foo”

bar.getFoo().setBaz("baz");

bar.getFoo().getBaz();        // “baz”
```

See how anyone, not just `Bar`, is able to change the state of `Bar`s `Foo`?  The `private` modifier gave you a false sense of security.  Your privates are really just hanging out there for anyone to whatever they want with.  Keep that in mind next time you create a getter that exposes a standard mutable data structure like a `List` or a `HashMap`.  Without mutability, this accidental exposure can't happen.

Java, I love you and I want you to get better.  (but honestly I'll probably always love your brother Scala more).
