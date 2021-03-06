+++
title = "The Embedded Working Group Newsletter - 8"
date = 2018-07-29
draft = false
in_search_index = true
template = "page.html"
aliases = ["2018-07-29/"]
+++

This is the eighth newsletter of the [Embedded WG] where we highlight new progress, celebrate cool projects, thank the community, and advertise projects that need help!

<!-- more -->

If you want to mention something in [the next newsletter], make sure to leave a comment on the issue.

[the next newsletter]: https://github.com/rust-lang-nursery/embedded-wg/issues/134
[Embedded WG]: https://github.com/rust-lang-nursery/embedded-wg

## Highlights

* [libm], the `no_std` port of MUSL's math library led by [japaric] has finished its' first release! It can now be used by embedded (or `wasm`!) targets that need support for math functions.
* [droogmic] is working on [microrust], a port of [japaric]'s Discovery book for the BBC MicroBit, based on the Nordic nRF51
* [Hideki Sekine] and [Vaishali Thakkar] have landed initial support for an [Embedded CI Harness] in the [`rust-lang/rust`] repo as part of the [Increasing Rust's Reach] project. This opens the door for tests that will help prevent regressions in `rustc` and `cargo` for ARM Cortex-M targets
* [CMSIS intrinsics] for ARM Cortex processors have landed in [stdsimd]. Check out the [the docs] in nightly soon<sup>†</sup> for info, thanks to [Paolo Teti] and [japaric]!
* [Ashley Williams] released [cargo-generate], a CLI tool for generating Cargo projects from a template, reducing the need to manually write boilerplate code. If you write some embedded templates, [let us know]!

†: The CMSIS intrinsics will show up in the docs after the next successful nightly build (after 2018-07-30)

[japaric]: https://github.com/japaric
[libm]: https://github.com/japaric/libm#libm

[droogmic]: https://github.com/droogmic
[microrust]: https://droogmic.github.io/microrust

[Embedded CI Harness]: https://github.com/rust-lang/rust/pull/52465
[Increasing Rust's Reach]: http://reach.rust-lang.org/
[Hideki Sekine]: https://github.com/sekineh
[Vaishali Thakkar]: https://github.com/nerdyvaishali
[`rust-lang/rust`]: https://github.com/rust-lang/rust

[Ashley Williams]: https://github.com/ashleygwilliams
[cargo-generate]: https://crates.io/crates/cargo-generate
[her tweet]: https://twitter.com/ag_dubs/status/1022191996293865472
[let us know]: https://twitter.com/rustembedded

[CMSIS intrinsics]: https://github.com/rust-lang-nursery/stdsimd/pull/518
[stdsimd]: https://github.com/rust-lang-nursery/stdsimd
[the docs]: https://doc.rust-lang.org/nightly/core/arch/arm/index.html
[Paolo Teti]: https://github.com/paoloteti

## Embedded Projects

If you have an embedded project or blog post you would like to have featured in the Embedded WG Newsletter, make sure to mention it on the tracking issue for [the next newsletter], we would love to show it off!

* [David McGillicuddy] has released his crate, [eight-segment], an `embedded-hal` driver for displaying digits on 8 segment displays like the HDSP H-101
* [James Waples] announced the newest release of his [embedded-graphics] library [in a tweet]. This version fixes some small issues, as well as provides functionality to save memory
* [Mart Roosmaa] released [bolos-rs], a 3rd party Rust SDK for the Ledger Nano cryptocurrency wallet. Check out his [Medium post] for more info!
* The [cc1101] crate can now recieve radio packets! Check out [the reddit post] by [Daniel Svensson], as well as [his blog post] for more info

[cc1101]: https://crates.io/crates/cc1101
[the reddit post]: https://www.reddit.com/r/rust/comments/8zk03w/cc1101_crate_can_now_receive_radio_packets/
[Daniel Svensson]: https://github.com/dsvensson
[his blog post]: https://dsvensson.github.io/posts/2018-07-13-Electrosmog-trapping-with-CC1101.html#article

[David McGillicuddy]: https://github.com/djmcgill
[eight-segment]: https://crates.io/crates/eight-segment

[James Waples]: https://github.com/jamwaffles
[in a tweet]: https://twitter.com/jam_waffles/status/1022837939041132545
[embedded-graphics]: https://crates.io/crates/embedded-graphics

[Mart Roosmaa]: https://github.com/roosmaa
[Medium post]: https://medium.com/@roosmaa/bringing-rust-to-ledger-hardware-wallet-ccf1356a7de1
[bolos-rs]: https://github.com/roosmaa/bolos-rs


### `embedded-hal` Ecosystem Crates

As part of the [Weekly Driver Initiative], crates that are part of the `embedded-hal` ecosystem are now tracked in the [Awesome Embedded Rust] repository. Here is a current snapshot of what is available there:

| Type                      | Status    | Count | Diff |
| :---                      | :-----    | :---- | :--- |
| [Device Crates]           | released  | 14    | 0    |
| [HAL Impl Crates]         | released  | 11    | 0    |
| [Board Support Crates]    | released  | 8     | +2   |
| [Driver Crates Released]  | released  | 11    | +2   |
| [Driver Crates WIP]       | WIP       | 35    | +5   |
| [no-std crates]           | released  | 12    | +12  |

[Awesome Embedded Rust]: https://github.com/rust-embedded/awesome-embedded-rust
[Weekly Driver Initiative]: https://github.com/rust-lang-nursery/embedded-wg/issues/39
[Device Crates]: https://github.com/rust-embedded/awesome-embedded-rust#device-crates
[HAL Impl Crates]: https://github.com/rust-embedded/awesome-embedded-rust#hal-implementation-crates
[Board Support Crates]: https://github.com/rust-embedded/awesome-embedded-rust#board-support-crates
[Driver Crates Released]: https://github.com/rust-embedded/awesome-embedded-rust#driver-crates
[Driver Crates WIP]: https://github.com/rust-embedded/awesome-embedded-rust#wip
[no-std crates]: https://github.com/rust-embedded/awesome-embedded-rust#no-std-crates

## Help Wanted

* The Embedded-WG is looking for someone to write an [RFC for ARM Intrinsics] to get them stabilized
* [Jonathan Pallant] is looking for ideas to implement for the Monotron project. Check out the [monotron blog post] for more details!
* The [libm] project is looking for help with [refactoring] in order to better support chips without hardware double-floating-point support

[Jonathan Pallant]: https://github.com/thejpster
[RFC for ARM Intrinsics]: https://github.com/rust-lang-nursery/embedded-wg/issues/63#issuecomment-408509178
[monotron blog post]: http://railwayelectronics.blogspot.com/2018/07/where-next-for-monotron.html
[refactoring]: https://github.com/japaric/libm/milestone/3