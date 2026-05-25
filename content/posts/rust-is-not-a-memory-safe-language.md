+++
title = "Rust is not a memory safe language: it is more"
date = 2026-05-25

[taxonomies]
tags = ["programming-languages", "rust"]
+++

I find it counterproductive,
and almost disparaging,
when _memory-safe_ is used as **the** primary descriptor of Rust.

It puts Rust in the same bucket
as Java, Python, Go, and JavaScript.

Putting the Rust language in the same category as them is illogical to me.

"Memory safety" gets the tagline,
because it's easiest to explain to C++ engineers.

But as a motivation to move from C++ to Python?
That makes no sense.

Rust feels like an entirely different class of memory-safe language.
It is a language class that:

{% quote() %}
empowers everyone
to productively build
reliable and efficient software
{% end %}

The first time I read that tagline,
I dismissed it as standard, meaningless, marketing fluff.

But as I wrote more software in the language,
the importance of every word in that phrase became apparent.

Empowers everyone:

- Rust removes barriers
  previously reserved for systems programming wizards only,
- lowers the barrier to entry by leveraging the compiler/tooling

Productive:

- my time to feature is faster than any language I've used
- Where feature is not just compiled and debugging,
  but actual working code

Reliable:

- is coupled with productivity
- the type system often replaces need for unit tests
- most difficult part of software is often logic and control flow:
  Rust has clearest description of these constructs I've ever used

Efficient:

- handles high performance, and low resource
  without needing to switch languages or ecosystems
- The naive, understandable approach
  is often _"good enough"_ by default

{% footnotes() %}

## aside

The NSA's "Software Memory Safety" directive,
is a pragmatic step,
and purposefully narrow in its scope.

The NSA encourages new software development
away from C and C++,
and towards memory-safety languages.

That recommendation is correct.

But framing Rust solely through this lens does it a disservice.

The NSA acknowledged that,
based on defect data from Google and Microsoft,
that the argument
_"careful C++ programmers can solve this"_
is definitively false.

History shows that developer teams,
do not write memory-safe C and C++ in practice.

After decades of running static and dynamic analysis tools,
the NSA noted:

{% quote() %}
Rigorous tests have shown that even
the best-performing static application security testing (SAST) tools
only identify a portion of memory issues
in even the simplest software programs
and usually generate many false positives.
{% end %}

They acknowledge that:

- Some languages provide minimal memory safety
- and those protections can be costly in performance and flexibility

But Rust has neither of these attributes.

- Rust's memory-safety attributes are extreme
- **and enable performance and flexibility**

The NSA is right
that memory-safety matters
and humans can't do it manually.

But "memory-safe" undersells
what Rust actually offers.

{% end %}
