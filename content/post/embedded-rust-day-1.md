---
title: "Embedded Rust Day 1"
date: 2020-08-22T19:41:39-05:00
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

Day 1 is done. I spent a fair amount of time writing the introductory post.
Additionally, while I am waiting on materials to arrive, I started to set up my
environment.

## Getting Started

First things first. I started looking around to figure out how to get set up to
do embedded Rust work.

I already have `rustup` installed so nothing to do there yet.

Next, I wanted to get my HiFive1 Rev B running using the
[riscv-rust-quickstart](https://github.com/riscv-rust/riscv-rust-quickstart).
I downloaded the Segger JLink software for my system, grabbed the nearest USB-B
micro, plugged it in and fired up `screen` to connect.

Nothing.

Reset.

Nothing.

Unplug it and re-plug it back in.

Nothing.

Okay. This is a less than auspicious start. Let's see what the kernel says.
I spent more than a few minutes poking around `dmesg` and `lsusb` but there
wasn't even anything there to see that the kernel even recognized that the
device was inserted but it was getting power and blinking.

Of course! The cable is power only. Doh!

After grabbing a real cable, I could see the serial output from the device with
no issues.

## Flashing the HiFive1

Next up, I installed `cargo generate` and used it to generate the quickstart
project and flashed a couple of examples on the device.

As I have a rev b, I used `JLinkGDBServer` to connect to the device and
`cargo run` connected through it. It wasn't a workflow that I'd experienced
before and I've never done much with `gdb`. First day and there's already
something to add to the TODO list! Fortunately, the
[Discovery Book](https://docs.rust-embedded.org/discovery/index.html)
seems to get right into it.

> We'll make plenty use of tooling to ease development. "Real" debugging, with
> GDB, and logging will be introduced early on. Using LEDs as a debugging
> mechanism has no place here.

## Wrapping up

I started to look through the examples to understand how they are put together
and how they work. I was hoping to get through a bit more but it was getting
late and was time to wrap up.

On deck for tomorrow is finishing up going through those examples, starting
on the Discovery Book and finalizing the orders for some of the components
that I don't already have.
