- A computer science bachelor's student who likes a good type system.
- I maintain [Mapv](https://github.com/debarchito/mapv) as an embeddable and
  hackable tool to learn and experiment with register machines in
  [OCaml](https://ocaml.org). To make tinkering even more fun, it comes equipped
  with built-in tracers and a visualizer built using
  [raylib](https://www.raylib.com). It implements a rather complex generational
  heap and garbage collection strategy with a NIF (native implemented functions;
  thanks Erlang) interface to expose native OCaml functions and values to the
  VM.
- I am currently researching and building
  [Miru](https://github.com/debarchito/miru). It is a statically typed Lisp+ML
  hybrid that uses algebraic effect handlers for all non-local control flow
  (even errors are just a subset of effects that discard their continuations).
  The primary objective is to combine the type safety of OCaml with the
  ergonomics of [Clojure](https://clojure.org) with differences drawn where it
  makes sense. It was and still is heavily inspired by
  [Shen](https://shen-language.github.io) and
  [Koka](https://koka-lang.github.io/koka/doc/index.html).
- I also like reproducible systems and almost all\[0] of my projects can be
  scaffolded using [Nix](https://nixos.org).
  - Check my bespoke bootstrapping framework
    [.bootstrap](https://github.com/debarchito/.bootstrap) if you want to get
    started with NixOS and NixOps in general.
  - It implements the [Dendritic](https://github.com/mightyiam/dendritic)
    pattern, packages a lot of software not in
    [nixpkgs](https://github.com/nixos/nixpkgs) such as
    [Helium](https://github.com/debarchito/.bootstrap/blob/main/modules/packages/helium.nix),
    CLAP plugins like
    [NeuralRack](https://github.com/debarchito/.bootstrap/blob/main/modules/packages/neuralrack.nix)
    and
    [Ratatouille](https://github.com/debarchito/.bootstrap/blob/main/modules/packages/ratatouille.nix)
    that can load [NeuralAmpModeler](https://www.neuralampmodeler.com) files and
    other WaveNET based formats, CUDA-enabled
    [Blender](https://github.com/debarchito/.bootstrap/blob/main/modules/packages/blender.nix)
    and
    [OBS-Studio](https://github.com/debarchito/.bootstrap/blob/main/modules/packages/obs-studio.nix)
    among other things.
  - I also maintain my artifacts cache registry @
    [debarchito.cachix.org](https://debarchito.cachix.org) which makes it easy
    to distribute packages built on GitHub Actions and/or SourceHut Builds.
  - The repository also implements a simple templating engine _creatively_ named
    [generate](https://github.com/debarchito/.bootstrap/blob/main/modules/packages/generate.nix)
    since nixpkgs's default templating system leaves a lot to be desired
    (parameter substitution is one of them). It can scaffold idiomatic projects
    for OCaml (using [opam-nix](https://github.com/tweag/opam-nix)), Rust (using
    [crane](https://github.com/ipetkov/crane) for better cache utilization), and
    Python (using [uv2nix](https://github.com/pyproject-nix/uv2nix)). For
    example, get started with a Rust project using:
    ```fish
    nix run sourcehut:~debarchito/.bootstrap#generate \
        rust ./hello-world \
        name="hello-world" description="Say hello to the world!"

    # You can build and/or run the demo application directly using Nix:
    nix build ./hello-world
    ./result/bin/hello-world
    # or:
    nix run ./hello-world

    # The development shells come pre-configured with direnv:
    cd hello-world && direnv allow
    ```
- If you own an Arturia
  [MiniFuse 1](https://www.arturia.com/store/audio-interfaces/minifuse-1) or
  [MiniFuse 2](https://www.arturia.com/store/audio-interfaces/minifuse-2), you
  can try [mfctl](https://github.com/debarchito/mfctl) to control these
  interfaces from your terminal. It's a partial replacement for the
  Windows/macOS-only
  [MiniFuse Control Center](https://www.arturia.com/support/downloads-manuals/product/mfcc)
  on Linux. It also includes a kernel module for non-sudo use-cases.
- If you play [Minecraft](https://www.minecraft.net), you might be interested in
  [minework](https://github.com/debarchito/minework) to help you manage your
  mods, modpacks, etc. I didn't find a satisfying tool to manage it all from the
  terminal, so I did it myself. I'm still adding QoL things like interactive
  fields with special fallback support for headless/non-interactive environments
  like servers.
- Some of my old experiments include
  [reinforced-shrine-adventure](https://github.com/debarchito/reinforced-shrine-adventure),
  which was an original story-based game turned training ground for an custom
  PPO agent to find the best ending.
- I also write prose and poetry, a collection of which can be found in my
  [digital garden](https://debarchito.is-a.dev/ddg).

\[0] Some old projects are yet to be Nix-ified.

Feel free to email me at [debarchiton@proton.me](mailto:debarchiton@proton.me)
if you want to talk about type systems, compilers, functional programming, free
software, game emulation, FPGAs, digital sovereignty, space, archaeology,
progressive music, or just about anything.

Of note, this GitHub profile is largely a discoverability asset. I also use it
when I want to fork repositories on GitHub or contribute to projects. Other than
that, I do most of my development on
[git.sr.ht/~debarchito](https://git.sr.ht/~debarchito). I do enjoy the
mailing-list aspect of decentralized VCS :D.
