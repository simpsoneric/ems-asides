+++
title = "Rust: settled foundations, freed minds"
date = 2026-04-16

[taxonomies]
tags = ["programming-languages", "rust"]

# [extra]
# subtitle = "Why some developers never want to return to renegotiated decisions"
+++

Despite the fervor of "rewrite it in Rust!",
Rust is a niche language.

Today almost everybody works in:
JavaScript, Python, and C-family languages.
Rust is a small minority.

But for those that start using the Rust ecosystem,
it has the strongest "I want to stay here" signal.

My hot-take reason for this "I don't want to go back signal" is

Rust appeals to developers who are okay giving up low-level choices:

- to get one-way to do everything that isn't your actual problem,
- to get high-level cohesion,
- to get shared leverage instead of individual cleverness.{{ fnref(id="dijkstra", n="1") }}

This includes:

- One way to build and package software: "cargo"
- One set of baseline patterns to express your ideas: "clippy"
- These patterns are formatted identically: "rust fmt"
- Patterns related to sharing data are settled: "the borrow checker"
- Patterns related to sharing behavior are settled: "rust traits"

Rust is seen as a low-level language,
but the reason it holds people is the opposite,
it has already answered the hard low-level questions,
how to share resources, structure data, and compose behavior.

These are settled, not open questions.

These are not endlessly renegotiated;
...team-by-team, file-by-file, or engineer-by-engineer.

No mental overhead for every project, or pull-request.
The computer keeps track of it;
...not your brain.
...not the project's maintainer.

The real payoff is above the low-level.
Rust's type system lets you express intent, not just implementation.
It lets you productively build.
This only works because of the settled foundations.

Not many developers enjoy giving up this much choice.{{ fnref(id="liskov", n="2") }}
But for some, once the language has provided so much,
&nbsp;&nbsp;...by freeing the human brain from low-level decisions
There's no going back.

{% footnotes() %}

## Footnotes

{{ fn(id="dijkstra", n="1") }} Dijkstra argued for
more reasoning about a program
by removing arbitrary control flow ("goto considered harmful")
...by the machine, not human convention

{{ fn(id="liskov", n="2") }} Liskov argued for
more composable programs (eg "modularity")
by removing arbitrary control AND data access
...by the machine, not human convention

{% quote() %}
Languages that enforce encapsulation
are based on a less is more kind of philosophy.
**The idea is that something can be gained
by having a programmer give up some freedom**.

What is gained is global: increased easy in reasoning about an entire, multi-module program.

What is lost is local: a programmer must live by the rules, which can sometimes be inconvenient

---

Liskov, B. _A History of CLU._ In History of Programming Languages II, edited by T. J. Bergin and R. G. Gibson, 471–510. ACM, 1996. (p. 476)
{% end %}

## aside

I recently watched Jon Gjengset discuss Rust in an interview.

He articulated something I had thought, but not connected.
Rust deliberately continues Liskov's philosophy at scale.

**It removes local programmer freedom
to gain global reasoning power.**

Rust does not remove freedom arbitrarily.
It removes the wrong freedoms,
to gain the ability to productively build software.

That is Liskov's thesis, embodied in the entire language and ecosystem.

It was a real-time discussion,
but I've attempted to faithfully capture his phrases.
Any out of context mistakes are mine;
please go watch the full interview.

{% quote() %}

rust is quite opinionated
they won't let you compile things you shouldn't do

cargo, has built in strong preferences
for how you're supposed to build code, package code, version code,
it might come across as constricting,
but they wanted an opinionated system
for people to build on-top of

if you try to do things the non-idiomatic way,
you will eventually get stuck,
because the compiler will not let you get away with doing things
that would naturally fall out of writing Java in Rust.

if you're very set on
I need to do things my way
and the way I've always done it.
Rust is not the language that lets you do that.

there are a bunch of patterns
you would write in those languages,
and if you try to write code in that way in Rust
either it just will not compile
or you have to pull a bunch of hacks to make it compile

and you get into all these painful problems
it makes you feel your application is architectured
in a way where the language dislikes it

When you hit that point,
you have two paths
&nbsp;&nbsp;I don't like it, it's really annoying
&nbsp;&nbsp;[...]
or the other path
&nbsp;&nbsp;the language is trying to teach me something here
&nbsp;&nbsp;how do I change my application
&nbsp;&nbsp;so these problems don't manifest in the first place

I think there is an interesting sort
of programmatic philosophical question here

my experience has been that
programs that come out of adapting to Rust's way of doing things,
do often produce better architected programs.
Like the internal structure of the program is actually better,
easier to refactor in the future,
more modular,
higher performance.

It tends to push you in directions that are useful

---

Gjengset, Jon. "on Rust Internals [...]" YouTube,
[https://youtu.be/Cg8gASzqqOs?si=-XSdZU6JAJEXB_4k&t=1032](https://youtu.be/Cg8gASzqqOs?si=-XSdZU6JAJEXB_4k&t=1032)

{% end %}
{% end %}
