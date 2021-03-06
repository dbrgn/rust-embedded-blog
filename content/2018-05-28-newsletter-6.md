+++
title = "The Embedded Working Group Newsletter - 6"
date = 2018-07-01
draft = false
in_search_index = true
template = "page.html"
aliases = ["2018-07-01/"]
+++

This is the sixth newsletter of the [Embedded WG] where we highlight new progress, celebrate cool projects, thank the community, and advertise projects that need help!

<!-- more -->

This newsletter covers the past ~6 weeks.

If you want to mention something in [the next newsletter], make sure to leave a comment on the issue.

[the next newsletter]: https://github.com/rust-lang-nursery/embedded-wg/issues/103
[Embedded WG]: https://github.com/rust-lang-nursery/embedded-wg

## Highlights

* [Jacob Creedon] gave an introduction talk about using Rust with embedded systems at the [Teardown Conference] in Portland, check out [Jacob's Slides] or the [Video of Jacob's Talk]
* The [Embedded WG]'s own [theJPster] talked about the [Monotron] at [RustFest Paris], you can see [JP's Slides], or check out the [Video of JP's Talk]
* [Jorge Aparicio], [Vadzim Dambrouski] and [Hanno Braun] from the embedded WG also attended RustFest Paris and the following impl days. They worked towards embedded Rust on stable, better embedded Rust tooling and better MSP430 support; gave away some hardware; and chatted with lots of people interested in embedded Rust.
* The `#[panic_implementation]` feature has [landed][panic-impl-pr] and has been proposed for stabilization ([FCP merge][panic-impl-fcp]). This feature lets you define the behavior of `panic!` in `#[no_std]` context and it's the final piece for making embedded Rust development possible on the stable channel. :tada:
* The [Discovery] book has been updated to work with the [preview of stable embedded Rust].
* A new [`llvm-tools` rustup component] is now available on recent nightly releases. It contains LLVM tools to inspect Rust binaries regardless of their target architecture. One set of tools for ARM Cortex-M, MSP430, x86_64 and other architectures!

[theJPster]: https://github.com/thejpster
[Monotron]: https://github.com/thejpster/monotron
[RustFest Paris]: https://paris.rustfest.eu/
[JP's Slides]: http://railwayelectronics.blogspot.co.uk/2018/05/talking-about-monotron-at-rustfest.html
[Video of JP's Talk]: https://media.ccc.de/v/rustfest18-11-monotron_making_a_80s_style_computer_with_a_20_dev_kit

[Jacob Creedon]: https://github.com/jcreedon
[Jacob's Slides]: http://github.jcreedon.com/static/EmbeddedWithRustSlidesTeardown2018.pdf
[Video of Jacob's Talk]: http://youtu.be/g25xsK3HKkE
[Teardown Conference]: https://www.crowdsupply.com/teardown/portland-2018

[Jorge Aparicio]: https://github.com/japaric
[Vadzim Dambrouski]: https://github.com/pftbest
[Hanno Braun]:  https://github.com/hannobraun

[panic-impl-pr]: https://github.com/rust-lang/rust/pull/50338
[panic-impl-fcp]: https://github.com/rust-lang/rust/issues/44489#issuecomment-398965878

[Discovery]: https://github.com/japaric/discovery
[preview of stable embedded Rust]: https://users.rust-lang.org/t/cortex-m-library-development-now-possible-on-beta-and-the-path-towards-stable-embedded-rust/17420

[`llvm-tools` rustup component]: https://internals.rust-lang.org/t/llvm-tools-a-new-rustup-component-for-binary-inspection-objdump-nm-size-and-profiling-prota/7830

## Embedded Projects

If you have an embedded project or blog post you would like to have featured in the Embedded WG Newsletter, make sure to mention it on the tracking issue for [the next newsletter], we would love to show it off!

* [rudihorn] shared [light-cli], a lightweight, no_std, and heapless CLI tool
* [Paolo Teti] shared [ti-hercules-bsp], a board support package for Texas Instruments TMS570 MCUs, used by safety critical industries such as automotive and aerospace
* [Marcel Buesing] posted their driver crate for the [bme680] environmental sensor
* [Roy Smeding] is working on support for the [stm32f334] chip from STMicro
* The [Embedded WG]'s own [Jonathan Soo] announced his project, [Bobbin SDK], a set of tools to make it easier to share code between different chips from the same or different vendors
* [Eitan Mosenkis] did [a major update] of their [esp-rs] script which produces a project to compile Rust code for the ESP8266 via the [mrustc] Rust to C compiler.
* [Hanno Braun] released v0.2 of [lpc82x-hal], which includes a radical simplification of the API, allowing for stronger compile-time state guarantees. Check out the [lpc82x-hal announcement] for more info!

[rudihorn]: https://github.com/rudihorn
[light-cli]: https://github.com/rudihorn/light-cli

[Paolo Teti]: https://github.com/paoloteti
[ti-hercules-bsp]: https://github.com/paoloteti/ti-hercules-bsp

[Marcel Buesing]: https://github.com/marcelbuesing
[bme680]: https://github.com/marcelbuesing/bme680

[Jonathan Soo]: https://github.com/jcsoo
[Bobbin SDK]: http://www.bobbin.io/blog/post/bobbin_sdk_richer_hardware/

[Roy Smeding]: https://github.com/roysmeding
[stm32f334]: https://github.com/roysmeding/stm32f334/

[Eitan Mosenkis]: https://github.com/emosenkis
[a major update]: https://users.rust-lang.org/t/rust-on-esp8266/12933/8
[esp-rs]: https://github.com/emosenkis/esp-rs
[mrustc]: https://github.com/thepowersgang/mrustc

[lpc82x-hal]: https://github.com/braun-robotics/rust-lpc82x-hal
[lpc82x-hal announcement]: https://users.rust-lang.org/t/lpc82x-hal-0-2-rust-on-lpc82x-microcontrollers/18144

### `embedded-hal` Ecosystem Crates

As part of the [Weekly Driver Initiative], crates that are part of the `embedded-hal` ecosystem are now tracked in the [Awesome Embedded Rust] repository. Here is a current snapshot of what is available there:

| Type                      | Status    | Count |
| :---                      | :-----    | :---- |
| [Device Crates]           | released  | 14    |
| [HAL Impl Crates]         | released  | 11    |
| [Board Support Crates]    | released  | 6     |
| [Driver Crates Released]  | released  | 9     |
| [Driver Crates WIP]       | WIP       | 30  |

[Awesome Embedded Rust]: https://github.com/rust-embedded/awesome-embedded-rust
[Weekly Driver Initiative]: https://github.com/rust-lang-nursery/embedded-wg/issues/39
[Device Crates]: https://github.com/rust-embedded/awesome-embedded-rust#device-crates
[HAL Impl Crates]: https://github.com/rust-embedded/awesome-embedded-rust#hal-implementation-crates
[Board Support Crates]: https://github.com/rust-embedded/awesome-embedded-rust#board-support-crates
[Driver Crates Released]: https://github.com/rust-embedded/awesome-embedded-rust#driver-crates
[Driver Crates WIP]: https://github.com/rust-embedded/awesome-embedded-rust#wip

## Help Wanted

* We are seeking [input about the user interface] the [`cargo-binutils`] subcommands should expose. These subcommands provide access to the LLVM tools provided by the `llvm-tools` rustup component mentioned above.
* Are you using embedded Rust in production? We are [collecting commercial testimonials] about embedded Rust for the webpage the embedded WG will have on the revamped rust-lang.org website. Even if you can't give details about the product you are building we would still love to hear from you!

[input about the user interface]: https://github.com/japaric/cargo-binutils/issues
[`cargo-binutils`]: https://github.com/japaric/cargo-binutils

[collecting commercial testimonials]: https://github.com/rust-lang-nursery/embedded-wg/issues/108
