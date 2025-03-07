<div align="center"><em>Mach is still early stages - see <a href="https://machengine.org/#early-stages">what we have today</a> and <a href="https://twitter.com/machengine">stay tuned</a></em></div>

# Mach: game engine & graphics toolkit for the future

Written in [Zig](https://ziglang.org/), Mach is for creating games, graphical applications, and desktop/mobile apps:

- Data-driven, tooling oriented
- Composable
- Competitive with Unity and Unreal in spirit (a fully fledged editor in the future, etc.)

<a href="https://user-images.githubusercontent.com/3173176/173177664-2ac9e90b-9429-4b09-aaf9-b80b53fee49f.gif"><img align="left" src="https://user-images.githubusercontent.com/3173176/173177664-2ac9e90b-9429-4b09-aaf9-b80b53fee49f.gif" alt="example-advanced-gen-texture-light" height="190px"></img></a>
<a href="https://user-images.githubusercontent.com/3173176/163936001-fd9eb918-7c29-4dcc-bfcb-5586f2ea1f9a.gif"><img align="left" src="https://user-images.githubusercontent.com/3173176/163936001-fd9eb918-7c29-4dcc-bfcb-5586f2ea1f9a.gif" alt="example-boids" height="190px"></img></a>
<a href="https://user-images.githubusercontent.com/3173176/173177646-a3f0982c-f07b-496f-947b-265bdc71ece9.gif"><img src="https://user-images.githubusercontent.com/3173176/173177646-a3f0982c-f07b-496f-947b-265bdc71ece9.gif" alt="example-textured-cube" height="190px"></img></a>

[Example showcase](https://machengine.org/gpu/)

## Cross-platform graphics in ~60 seconds

```sh
git clone https://github.com/hexops/mach
cd mach/
zig build run-example-boids
```

Cross-platform graphics, a unified shader language & compute shaders.

(Requires [zig 0.10.x](https://ziglang.org/) | [known issues](https://github.com/hexops/mach/blob/main/doc/known-issues.md#known-issues))

## Libraries

Mach has many libraries you can use for game development in Zig - **you don't have to use the entire engine.** All our libraries aim to have the same zero-fuss installation, cross compilation, and platform support:

- [mach-glfw](https://github.com/hexops/mach-glfw): Ziggified GLFW bindings with 100% API coverage
- [mach-freetype](https://github.com/hexops/mach-freetype): Ziggified Freetype 2 & HarfBuzz bindings
- [mach-gpu-dawn](https://github.com/hexops/mach-gpu-dawn): Google's Dawn WebGPU implementation, cross-compiled with Zig into a single static library
- [mach-system-sdk](https://github.com/hexops/mach-system-sdk): More libraries for cross-compilation with Zig

## Join the community

* [#hexops:matrix.org Matrix chat](https://matrix.to/#/#hexops:matrix.org) and [Discord server](https://discord.gg/XNG3NZgCqp), come discuss the future of game engines & graphics in Zig!
* [machengine.org](https://machengine.org)
* Follow [@machengine on Twitter](https://twitter.com/machengine) for updates.

Contributors are very welcome! There are lots of places you can help out with little knowledge, so feel free to join the Matrix chat and say hi!

## Sponsor development

<img align="left" src="https://user-images.githubusercontent.com/3173176/163940979-6a1c1e5a-690d-4e6c-ad74-e1407ba7c867.png" width="150px"></img>

No, it’s not Tom from myspace - it’s me, @slimsag! It’s taken [almost a year to get here](https://devlog.hexops.com/2022/mach-v0.1-zig-graphics-in-60s) - staring at broken CI pipelines, C++ compiler errors, [buying hardware](https://twitter.com/slimsag/status/1507506138144681986) to test every OS+arch possible, and more.

There are few things in life that I am more serious about than this work. I dedicate ~48 hours/week to my dayjob, and ~50h/week to Zig building Mach and running [zigmonthly.org](https://zigmonthly.org). After three years of aggressively pushing for progress in this exact way, [I have no plans to slow down anytime soon.](https://devlog.hexops.com/2021/i-write-code-100-hours-a-week)

## Supported platforms

Mach is still early stages, so far we have support for building from the following OS to the following targets:

| Building for     | From macOS x86_64 | From macOS M1/aarch64 | From Linux x86_64 | From Windows x86_64 |
| ---------------- | ----------------- | --------------------- | ----------------- | ------------------- |
| macOS x86_64     | ✅                | ✅                    | ✅                | ✅                  |
| macOS M1/aarch64 | ✅                | ✅                    | ✅                | ✅                  |
| Linux x86_64     | ✅                | ✅                    | ✅                | ✅                  |
| Windows x86_64   | ✅                | ✅                    | ✅                | ✅                  |
| iOS              | 🏃                | 🏃                    | 🏃                | 🏃                  |
| Android          | 🏃                | 🏃                    | 🏃                | 🏃                  |
| Web (Wasm)       | 🏃                | 🏃                    | 🏃                | 🏃                  |

- ✅ Tested and verified via CI.
- ✔️ Should work, not tested via CI yet.
- 🏃 Planned or in progress.
- ⚠️ Implemented, but has known issues (e.g. bugs in Zig.)

## Supported Zig version

Zig has switched to the self-hosted compiler recently. This is a huge milestone, but currently means that Zig nightly versions are a little bit unstable. For now, we suggest using a slightly older Zig version before the switch to the self-hosted compiler.

Currently tested with: 0.10.0-dev.3842+36f4f32fa

You can download binary releases of this version at:

* **linux-x86_64**: https://ziglang.org/builds/zig-linux-x86_64-0.10.0-dev.3842+36f4f32fa.tar.xz)
* **windows-x86_64**: https://ziglang.org/builds/zig-windows-x86_64-0.10.0-dev.3842+36f4f32fa.zip
* **macos-x86_64** (Intel): https://ziglang.org/builds/zig-macos-x86_64-0.10.0-dev.3842+36f4f32fa.tar.xz
* **macos-aarch64** (Apple Silicon): https://ziglang.org/builds/zig-macos-aarch64-0.10.0-dev.3842+36f4f32fa.tar.xz

You can subscribe to [issue #180](https://github.com/hexops/mach/issues/180) for how we're tracking towards support for the latest nightly version of Zig.

## Contributing

Mach is maintained as a monorepo. When changes are merged to this repository, we use some git-fu to pick out the commits to subdirectories and push them to sub-repositories automagically. Changes to the `glfw/` directory in this repository get pushed to the separate [mach-glfw](https://github.com/hexops/mach-glfw) repository after being merged here, for example.

Please prefix commits / pull requests with the project name (`glfw: fix an issue`, `gpu: fix an issue`, `examples: fix an issue`, etc.) and if possible only one project per commit. If you don't know how to do this, no worries, we can help - just send your PR anyway!
