---
title: "Embedded Rust Day 2: Electric Boogaloo"
description: ""
date: 2020-08-23T13:53:53-05:00
toc: false
tags:
  - rust
  - embedded
  - riscv
categories:
  - development
series:
  - embedded rust adventures
draft: false
---

## Day 2

I was hoping to get through a bit more than I did but I guess there will be
some really productive days and some less so.

## RISC-V Quickstart Examples

I started looking through the quickstart examples to see if there were any
other examples I wanted to flash while I was poking around at it. More
importantly though, I wanted to start getting into the habit of reading and
mentally parsing Rust.

I did notice a few things of note:

```rust
#[entry]
fn main() -> ! {
    ...
    loop {
        ...
    }
}
```

This doesn't look all that different from something like an Arduino program.
The first ellipsis seems logically equivalent to `void setup() {}` and the
second to `void loop() {}`.

```rust
132.mhz().into()
```

This is a cool Rust thing. In `e310x_hal::time` they've defined and implemented
a trait to convert a `u32` into `Hertz`, `KiloHertz` and `MegaHertz`. And then
implemented `Into` to convert into `Hertz`. I think that's pretty cool. It
allows for a really expressive and readable way to work with frequency while
providing all of the safety that comes from strong typing and the Rust compiler.

While trying to look up how this was implemented, my IDE wouldn't go to the
definition. I'm not sure why but it compiled and worked correctly so I had to
believe that the code was on my machine somewhere. Fortunately, a quick
`cargo doc --open` was enough for me to find it. 100 points to Gryffindor.

I also started to look through the HiFive1 and e310x documentation which is
entirely too dry to describe here.

## What's next

Well, that wasn't nearly all that I was hoping to accomplish but, alas, some
days are just like that. I'm still waiting on my Discovery board but I'm going
to start on the book and read ahead while I'm waiting. Hopefully, I can get
started in earnest sometime this week.
