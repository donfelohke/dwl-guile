# dwl-guile

**Project:** Dynamic tiling Wayland compositor configurable in Guile Scheme, based on dwl and libguile, with a REPL.  
**Repository:** [donfelohke/dwl-guile](https://github.com/donfelohke/dwl-guile)  
**Human author / maintainer:** Felix Lwova · Don Feloh · [@donfelohke](https://github.com/donfelohke)

This is a supporting technical project in the WARENA engineering ecosystem. It is not a separate brand, commercial service or new practice domain.

## Identity relationship

- **GRIT → WARENA:** libre-first systems engineering and infrastructure.
- **GLORY → DON FELOH:** human authorship and creative agency.
- **GENJE:** independent embodied creative practice; its relationship to WARENA is expressed by **GENJE ZA WARENA**.
- **GRACE → NAKEBUSEN:** distinct beauty and loc-care practice; **ONLY NAKEBUSEN TRANSACTS**.

**FELOH** — Authorship · Intellectual work · Creative direction  
**NAKEBUSEN** — Beauty · Heritage · Craft · Enterprise  
**IKAI** — Reflective computing · Perception · Memory · Human experience  
**WARENA** — Libre technology · Infrastructure · Systems engineering · Digital sovereignty  
**GENJE** — Music · Movement · Performance · Creative expression

## Build prerequisites and local build

The checked-in Makefile discovers development dependencies through `pkg-config` and invokes `wayland-scanner` for protocol sources. The current Makefile package modules are:

- `wlroots`
- `wayland-server` and `wayland-client`
- `xkbcommon`
- `libinput`
- `guile-3.0`
- `pixman-1`

A working build environment also needs a C compiler, GNU Make, `pkg-config`, Wayland protocols data and the `wayland-scanner` executable. Optional XWayland support is disabled in the checked-in `config.mk`; enabling it changes the dependency set. Resolve the exact compatible versions against the source revision and the target distribution rather than assuming that any current wlroots release is interchangeable.

From a checkout, inspect the configuration and attempt a local build:

```sh
make
```

The default target is `dwl`. The Makefile does not currently define a test target, so a successful compile is not a runtime or compositor-session validation. Record the distribution, compiler, Guile and wlroots versions, complete build output and any patches when reporting a build result.

The Makefile's `install` target changes the built binary's name before installing it under the configured prefix. Review that target and the destination before using it; the command above only builds and does not install.

## Scope and evidence

This README is an orientation to the repository identity and project purpose. Consult the source tree, existing documentation and LICENSE for implementation details, build instructions, supported configurations and contribution requirements. Do not infer release status, compatibility or deployment from the repository description alone.

## Related WARENA research

- [Reproducible Systems and Real-Time I/O Validation](https://github.com/donfelohke/WARENA/blob/main/docs/REPRODUCIBLE-SYSTEMS-AND-REALTIME-IO-VALIDATION-2026-11-24.md) — shared research and proposed validation methods; not a claim that this compositor or service has completed those tests.
- [Camera, Display and Real-Time I/O at Scale](https://github.com/donfelohke/WARENA/blob/main/docs/CAMERA-DISPLAY-REALTIME-IO-SCALE-RESEARCH-2026-11-24.md) — relevant native media and display pipeline context.

**Freedom Is a System.**


## Ecosystem alignment · 2026-11-24

See [the alignment note](doc/ECOSYSTEM-ALIGNMENT-2026-11-24.md) for this repository's role, cross-project boundaries and documentation standards.


## Shared identity alignment · 26 November 2026

This repository is a supporting WARENA engineering project. **GRIT → WARENA** is the current pillar mapping; FELOH remains the human author, GRACE → NAKEBUSEN and GLORY → GENJE / GENJENESS. This repository is not a separate brand or commercial service. See the [current shared identity clarification](https://github.com/donfelohke/feloh-corpus/blob/main/docs/IDENTITY-CANONICAL-CLARIFICATION-2026-11-26.md). **ONLY NAKEBUSEN TRANSACTS.**


## Documentation index

See [docs/README.md](docs/README.md) for the current repository documentation map and source-of-record links.
