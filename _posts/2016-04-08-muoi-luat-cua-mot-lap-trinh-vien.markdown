---
layout: post
title: "10 luật để trở thành một lập trình viên tốt"
date: "2016-04-08 12:47:54 +0700"
---

10 luật để trở thành một lập trình viên tốt

Bài viết này được lấy ý tưởng từ [pragmatic-programmer][một cuốn sách nổi tiếng]. Rất nổi tiếng ở thế hệ thôi, nhưng có thể bạn chưa từng nghe nói tới. Nó xứng đáng được đọc, đọc lại và nhắc lại.

Here are the 10 most interesting rules I’ve found in that book, if a programmer manages to apply them in his daily duties, no doubt they’re pragmatic (and productive).

Rule #1: Do not repeat yourself

Respect the DRY principle:

Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.

This will increase your maintenance capabilities and lower bugs proliferation.

Rule #2: Fix broken windows

The concept of Broken Windows come from the criminological theory:

Consider a building with a few broken windows. If the windows are not repaired, the tendency is for vandals to break a few more windows. Eventually, they may even break into the building, and if it’s unoccupied, perhaps become squatters.

In software development, broken windows are bad designs, wrong decisions or even poor code. If you don’t fix them as you find them, you’ll end up quickly with software rot.

Rule #3: Crash Early

It’s always better to make your code crash as soon as possible. Using return values (error codes) to notify a calling component about an error is a very bad idea. Eventually, a component will ignore that value, that means that an error can occur and silently be ignored.

As the saying goes: Dead software don’t lie.

Rule #4: Use tracer bullets

The idea of tracer bullets is to get things up in production as soon as you can.

We speak also about code that glows in the dark. When you have a new projet in mind, try to get to the point where you can ship something in production. Just make it as simple as possible, don’t try to envision everything in the first place. The first target is to have a simple, consistent package that works, in production. After that, you’ll be able to upgrade that package iteratively.

The tracer bullet is your first package, by reducing its feature set, you’ll focus on the essential: production/packaging/deployment issues. Other features and enhancements will come later on. This strategy has also the benfit of reducing the risk of premature optimizations (which is the root of all evil, as you may already know).

Rule #5: Write Shy Code

Shy code is basically what we call the Law of Demeter. It could be described as the Principle of Least Knowledge, as Wikipedia explains:


The guideline […] can be succinctly summarized in one of the following ways:

Each unit should have only limited knowledge about other units: only units “closely” related to the current unit.
Each unit should only talk to its friends; don’t talk to strangers.
Only talk to your immediate friends.
 

Respecting the Law of Demeter when writing code enhance maintainability and reduce code duplication (so yes, that helps you repsect rule #1).

Rule #6: Configure, don’t integrate

Details mess up our pristine code, they change frequently. Every change to the code is a risk to break the system. To avoid that, you should get the details out of the code, in configuration files. Configurable code is called Â« soft code Â», it’s adaptable to change.

Whenever you come to the point where you put details into your codebase, stop, and extract them out of it. The time you spend now will pay-off ten times in the future.

Rule #7: Refactor Early, refactor often

You should refactor, yes, but when? Here are the moments when refactoring is a good idea:

You’ve found some duplication you want to remove (again, rule #1!)
You want to extract details out of the code (rule #6)
You see a way to generalize something in your code.
Also, don’t refactor blindly, if you go into a refactoring session it’s very important to do it well, or it will come back to bite you:

Don’t refactor and add functionality at the same time
Make sure you have tests to avoid regressions
Take short, deliberate steps. Change one thing at a time.
Rule #8: Design to test

If you’re a perfectionist, you might write your tests before the code (it’s called Test-Driven Development) but it’s not mandatory. A matter of taste I’d say. What is important though is that you always keep tests in mind when you write the code. Respecting the Law of Demeter (rule #5) will definitely help, because a good encapsulation always leads to testable code.

If a part of the code is difficult (or impossible) to test, you need to refactor it to smaller components.

Rule #9: if you’ve found a bug, write a test

This is a very sane approach: whenever a bug is found in production, first thing to do is to write a test that reproduces the issue. That way you’ll be sure to understand the bug correctly before thinking at the fix and you’ll have a non-regression test that will make sure the bug won’t happen again.

Rule #10: Know when to stop

Programmers are like painters, they build a picture of some part of the world out of their mind. The major difficulty here is not know when, or where to stop. Keep in mind that perfect software does not exist (no, you won’t be able to write it, no matter how hard you try).

When is a painting finished? Only the painter can say so. You are the painter of your code, know when to stop.

Source: http://blog.sukria.net/2012/01/06/the-10-rules-of-the-pragmatic-programmer/

