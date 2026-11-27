# dwl-guile

**Project:** Dynamic tiling Wayland compositor configurable in Guile Scheme, based on dwl and libguile, with a REPL.  
**Repository:** [donfelohke/dwl-guile](https://github.com/donfelohke/dwl-guile)  
**Human author / maintainer:** Felix Lwova · Don Feloh · [@donfelohke](https://github.com/donfelohke)

This is a supporting technical project in the WARENA engineering ecosystem. It is not a separate brand, commercial service or new practice domain.

## Identity relationship

- **GRIT → WARENA:** libre-first systems engineering and infrastructure.
- **GLORY → GENJE / GENJENESS:** creative greatness, Genge-rooted sound, livecoding, movement, choreography and authored expression; FELOH remains the human author.
- **GENJE:** independent embodied creative practice; its relationship to WARENA is expressed by **GENJE ZA WARENA**.
- **GRACE → NAKEBUSEN:** distinct beauty and loc-care practice; **ONLY NAKEBUSEN TRANSACTS**.

**FELOH** — Authorship · Intellectual work · Creative direction  
**NAKEBUSEN** — Beauty · Heritage · Craft · Enterprise  
**IKAI** — Reflective computing · Perception · Memory · Human experience  
**WARENA** — Libre technology · Infrastructure · Systems engineering · Digital sovereignty  
**GENJE** — Music · Movement · Performance · Creative expression

## Current identity clarification · 26 November 2026

The current pillar mapping is **GRACE → NAKEBUSEN; GRIT → WARENA; GLORY → GENJE / GENJENESS**. FELOH remains the human author and creative/technical decision-maker. This repository remains a supporting WARENA engineering project, not a separate practice or commercial interface. See the [shared identity clarification](https://github.com/donfelohke/feloh-corpus/blob/main/docs/IDENTITY-CANONICAL-CLARIFICATION-2026-11-26.md).

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

See the [shared ecosystem alignment note](https://github.com/donfelohke/feloh-corpus/blob/main/docs/ECOSYSTEM-ALIGNMENT-2026-11-24.md) for cross-project boundaries and the [repository provenance note](docs/ASSET-AND-DOCUMENTATION-PROVENANCE-2026-11-24.md) for upstream and documentation attribution.


## Documentation index

See the [repository provenance note](docs/ASSET-AND-DOCUMENTATION-PROVENANCE-2026-11-24.md) and the [shared ecosystem alignment note](https://github.com/donfelohke/feloh-corpus/blob/main/docs/ECOSYSTEM-ALIGNMENT-2026-11-24.md) for documentation and source-of-record links.
