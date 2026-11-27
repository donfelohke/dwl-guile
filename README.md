# dwl-guile

A Guile-configurable fork of the dwl dynamic tiling Wayland compositor, integrating GNU Guile and a REPL for programmable configuration.

**Maintainer:** Felix Lwova · Don Feloh · [@donfelohke](https://github.com/donfelohke)  
**Ecosystem role:** Supporting WARENA engineering project — not a separate brand or commercial service.

## Project scope

This repository explores a Scheme-programmable compositor built on dwl and libguile. It is a supporting systems-engineering project within WARENA's GNU/Linux and reproducible-computing work.

The project is not a standalone desktop distribution, a supported production desktop release or a promise of compatibility with every wlroots/Wayland stack. Verify the exact source revision and dependency versions on the target system.

## Build

The checked-in Makefile uses `pkg-config` and `wayland-scanner`. The current package modules include:

- `wlroots`
- `wayland-server` and `wayland-client`
- `xkbcommon`
- `libinput`
- `guile-3.0`
- `pixman-1`

A build environment also needs a C compiler, GNU Make, `pkg-config`, Wayland protocols data and `wayland-scanner`. Optional XWayland support is disabled in the checked-in `config.mk`; enabling it changes the dependency set.

Inspect the configuration and source revision before building:

```sh
make
```

The default target builds `dwl`. The Makefile does not currently define a test target. A successful compile therefore does not establish a working compositor session, runtime stability, input/display compatibility or a validated Guile REPL workflow.

The Makefile's `install` target renames the built binary before installing it under the configured prefix. Review the target and destination before installation; the command above does not install.

## Validation record

For each build or runtime report, record:

- commit SHA and any local patches;
- distribution, kernel and architecture;
- compiler, wlroots, Wayland, Guile and protocol versions;
- exact build command and complete output;
- compositor launch/session outcome;
- input, output, keybinding and REPL tests;
- known limitations and recovery procedure.

Do not report a build or runtime result without the environment and evidence that produced it.

## Upstream and provenance

This repository derives from dwl and related upstream components. Preserve their licences, copyright notices and attribution. Treat this repository as a fork/configuration effort, not as ownership of upstream work. Record the exact upstream base and local delta in the provenance documentation before describing compatibility or claiming a clean rebase.

See [asset and documentation provenance](docs/ASSET-AND-DOCUMENTATION-PROVENANCE-2026-11-24.md).

## WARENA relationship

- [WARENA](https://github.com/donfelohke/WARENA) owns the CAPABILITY systems-engineering context and technical policy.
- [home-service-dwl-guile](https://github.com/donfelohke/home-service-dwl-guile) provides a separate GNU Guix Home integration.
- [FELOH Corpus](https://github.com/donfelohke/feloh-corpus) governs shared identity, evidence and provenance.

WARENA is libre-first, local-first and human-controlled. GNU is foundational but not an exclusive technology boundary. **Freedom Is a System.**

**ONLY NAKEBUSEN TRANSACTS.** This repository is not a commercial checkout or booking interface.

## Documentation and contribution

- [Documentation index](docs/README.md).
- [GNU Guix Home integration](https://github.com/donfelohke/home-service-dwl-guile).

Preserve upstream history and document each material local change. Prefer a small, reviewable patch over a wholesale replacement of upstream code.

## Canonical alignment · 27 November 2026

See [dwl-guile ecosystem alignment](doc/ECOSYSTEM-ALIGNMENT-2026-11-24.md) for the dated cross-project definitions, evidence boundaries and repository-specific responsibilities.
