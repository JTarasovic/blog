---
title: "Embedded Rust Introduction"
date: 2020-08-22T19:40:00-05:00
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

I'm embarking on a journey to better understand how computers work by learning
about embedded development, FPGAs, Operating Systems and more.
My rather aspirational goal is to work on it every day with, at least, a short
post here about what I did and what I've learned. If you're interested, I
welcome you to come along for the journey.

## Why?

It may be instructive to start with why I am interested in this before
proceeding to what I hope to achieve.

As I am not formally educated as a software engineer, I have had to learn
almost everything on my own. While I feel like I have a pretty good sense of how
computers work and I am pretty happy with what I've been able to accomplish, I
wouldn't feel comfortable doing low(er) level systems programming - writing a
device driver or lower.

Additionally, I'm also interested in electronics generally. I am a licensed
amateur radio operator and have a whole bin of microcontrollers, FPGAs, SBCs,
etc.

It seems to me like the logical next step in my journey.

## What?

So what is it exactly that I want to learn / accomplish? Well, this is what I've
got thus far in decreasing order of likelihood / attainability:

- Program a microcontroller to do basic input / output via standard
  protocols like I<sup>2</sup>C and SPI using a low-level, systems programming
  language - Rust.
- Design and build a very simple, very small Operating System for a small
  system such as a Raspberry Pi.
- Use RISC-V assembly to control a dev board such as VEGAboard or
  HiFive1.

<!-- - Program an FPGA for extremely high channel home energy monitoring (think
  high-frequency monitoring for every circuit). -->

### Alternatives considered

While it is certainly possible to use something like the Arduino IDE or
PlatformIO with a higher level language to accomplish most of those, I'm not
sure that it would satisfy the learning objectives I've laid out. Moreover,
by doing it this way, I also get the multiplicative opportunity to learn
not only the overarching thing - microcontrollers, OS design and development,
etc - but also learn some newer technologies that I am excited about - Rust
and RISC-V.

## How?

With that out of the way, what I'd like to do is to start by working through the
embedded Rust books as well as the OS development tutorials.[^1][^2][^3]

[^1]: https://docs.rust-embedded.org/discovery/index.html
[^2]: https://docs.rust-embedded.org/book/index.html
[^3]: https://github.com/rust-embedded/rust-raspberrypi-OS-tutorials

Then I want to move on to a trilogy of RISC-V material:

- **The RISC-V Reader** _David Patterson_
- **RISC-V Assembly Language** _Anthony Dos Reis_
- **Computer Organization and Design RISC-V Edition** _David Patterson_

As I am working through the material, I want to write something about it as
something of a forcing function or commitment device.

It's all a bit aspirational and I may fall flat on my face in a day or week or
whatever but that's the initial plan.
