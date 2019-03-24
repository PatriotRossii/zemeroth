# Zemeroth [![mit license][img_license]](#license) [![line count][img_loc]][loc]

[img_license]: https://img.shields.io/badge/License-MIT_or_Apache_2.0-blue.svg
[img_loc]: https://tokei.rs/b1/github/ozkriff/zemeroth

Zemeroth is a turn-based hexagonal tactical game written in [Rust].

[Rust]: https://www.rust-lang.org

![tiny screenshot (I don't have any logo yet)](https://i.imgur.com/WYHNPKem.png)

**News**: [@ozkriff on twitter](https://twitter.com/ozkriff) |
[ozkriff.github.io](https://ozkriff.github.io) |
[devlog on imgur](https://imgur.com/a/SMVqO)

**Status**:
[![travis status][img_travis-ci]][travis-ci]
[![appveyor status][img_appveyor-ci]][appveyor-ci]
[![dependency status][img_deps-rs]][deps-rs]

[img_travis-ci]: https://img.shields.io/travis/ozkriff/zemeroth/master.svg?label=Linux|OSX
[img_appveyor-ci]: https://img.shields.io/appveyor/ci/ozkriff/zemeroth/master.svg?label=Windows
[img_deps-rs]: https://deps.rs/repo/github/ozkriff/zemeroth/status.svg

[loc]: https://github.com/Aaronepower/tokei
[travis-ci]: https://travis-ci.org/ozkriff/zemeroth
[appveyor-ci]: https://ci.appveyor.com/project/ozkriff/zemeroth
[deps-rs]: https://deps.rs/repo/github/ozkriff/zemeroth

## Precompiled Binaries

Precompiled binaries for Linux, Windows and macOS:
<https://github.com/ozkriff/zemeroth/releases>

## Screenshots

!["big" screenshot](https://i.imgur.com/yPfO8eH.png)

!["campaign" screenshot](https://i.imgur.com/6FB77lz.png)

## Gifs

![main gameplay animation](https://i.imgur.com/HqgHmOH.gif)

## Videos

<https://www.youtube.com/user/ozkriff619/videos>

## Building from Source

```bash
# Clone this repo
git clone https://github.com/ozkriff/zemeroth
cd zemeroth

# Assets are stored in a separate repo.
# Zemeroth expects them to be in `assets` directory.
git clone https://github.com/ozkriff/zemeroth_assets assets

# Compile a release version (debug builds give low FPS at the moment)
cargo build --release

# Run it
cargo run --release
```

## WebAssembly

```bash
cargo install cargo-web
./utils/wasm/build.sh
cargo web start
```

Then open `http://localhost:8000` in your browser.

The WASM version of the game uses
[not-fl3/good-web-game](https://github.com/not-fl3/good-web-game):

> [Note](https://github.com/ggez/ggez/issues/71#issuecomment-459875258)
> that good-web-game is not really GGEZ's backend,
> but a separate web-targeted engine with a similar API
> that @not-fl3 uses for his prototypes.
>
> Zemeroth uses good-web-game for its web version as a quick-n-dirty
> immediate solution until a proper WASM support arrives to GGEZ
> (there're no plans of making good-web-game some kind of official GGEZ backend).
>
> The currently implemented subset of GGEZ API is quite limited
> and while it may be used for something else that Zemeroth,
> it will probably require a lot of work to do (contributions are welcome ;) ).

## Dependencies

The key external dependency of Zemeroth is [ggez] game engine.

This repo contains a bunch of helper crates:

- [zcomponents] is a simple component storage
- [ggwp-zgui] is a simple and opinionated ggez-based GUI library
- [ggwp-zscene] is a simple scene and declarative animation manager

[ggez]: https://github.com/ggez/ggez
[zcomponents]: ./zcomponents
[ggwp-zscene]: ./ggwp-zscene
[ggwp-zgui]: ./ggwp-zgui

## Contribute

If you want to help take a look at issues with `help-wanted` label attached:

<https://github.com/ozkriff/zemeroth/labels/help-wanted>

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license,
shall be dual licensed as above, without any additional terms or conditions.

## License

Zemeroth is distributed under the terms of both
the MIT license and the Apache License (Version 2.0).

See [LICENSE-APACHE] and [LICENSE-MIT] for details.

[LICENSE-MIT]: LICENSE-MIT
[LICENSE-APACHE]: LICENSE-APACHE
