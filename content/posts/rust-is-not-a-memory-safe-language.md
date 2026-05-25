+++
title = "Rust is not a memory safe language: it is more"
date = 2026-05-25

[taxonomies]
tags = ["programming-languages", "rust"]
+++

I find it counterproductive,
and almost disparaging,
when _memory-safe_ is used as the primary descriptor of Rust.

It puts Rust in the same bucket
as Java, Python, Go, and JavaScript.

Putting Rust in that category feels wrong to me.

{% aside() %}
[rust is a niche language](@/posts/rust-settled-foundations-freed-minds.md),
in 2026, almost everyone programs in other languages
{% end %}

"Memory safety" gets the tagline,
because it's easiest to explain to C++ engineers.{{ fnref(id="tiobe", n="1") }}

But if “memory safety” alone were the point,
Python would already solve the problem.
Rust matters because it offers something different.

Rust feels like an entirely different class of memory-safe language.

One that:

{% quote() %}
empowers everyone
to productively build
reliable and efficient software
{% end %}

The first time I read that tagline,
I dismissed it as standard, meaningless, marketing fluff.

But as I wrote more software in the language,
the importance of every word in that phrase became apparent.

Empowers:

{% aside() %}
I wrote a multi-threaded,
raw-flash, file store in Rust.

The language gave me confidence
to implement this correctly.
{% end %}

- Rust democratizes systems programming
- It encodes rules that experts usually carry in their heads
- The language helps ordinary programmers apply those rules

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

{% aside() %}
Rust efficiency is roughly same as C/C++.
Spans microcontroller to supercomputer.
{% end %}

- handles high performance, and low resource
  without needing to switch languages
- The naive, understandable approach
  is often _"good enough"_ by default

Some companies inherently value the security memory safety provides.
Others are more swayed by the productive, reliable, and efficient tagline.
I think "memory-safe" undersells what Rust actually offers.

Instead, I think we should strive to view Rust through the official tagline:

**Rust empowers everyone to productively build reliable and efficient software**

{% footnotes() %}

## Footnotes

{{ fn(id="tiobe", n="1") }} C and C++ together hold ~20% of language market share. Rust sits at ~1%. Source: [TIOBE Index](https://www.tiobe.com/tiobe-index/).

## Aside

The NSA's ["Software Memory Safety"](https://media.defense.gov/2025/Jun/23/2003742198/-1/-1/0/CSI_MEMORY_SAFE_LANGUAGES_REDUCING_VULNERABILITIES_IN_MODERN_SOFTWARE_DEVELOPMENT.PDF) directive,
is a pragmatic step,
and purposefully narrow in its scope.

The NSA encourages new software development
away from C and C++,
and towards memory-safe languages.

That recommendation is correct.

But framing Rust solely through this lens does it a disservice.

The NSA acknowledged,
based on defect data from [Microsoft](https://www.microsoft.com/en-us/msrc/blog/2019/07/a-proactive-approach-to-more-secure-code), [Chromium](https://www.chromium.org/Home/chromium-security/memory-safety/), and [Android](https://security.googleblog.com/2022/12/memory-safe-languages-in-android-13.html),
the argument _"careful C++ programmers can solve this"_
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
