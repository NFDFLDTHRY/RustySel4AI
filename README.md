# RustySel4AI

RustySel4AI is an **AI-first operating-system research and construction project**. This repository currently holds the C01/P01 project baseline. It does not yet contain an operating system, compiler, kernel, filesystem, model, or executable runtime.

The working loop is human intent -> AI-authored ASCII system description -> bounded factory workpiece -> independent verification -> accepted repository change -> execution evidence -> revised description. Intended structure and observed behavior retain separate IDs.

Start with [AGENTS.md](AGENTS.md), then read [the project law](docs/LAW.md), [the whole-system map](docs/SYSTEM.md), [the contract and gap register](docs/CONTRACTS.md), and [the current handoff](docs/HANDOFF.md). [C01 cycle record](docs/CYCLES.md), [provenance](docs/PROVENANCE.md), and [evidence](docs/EVIDENCE.md) show what has actually been checked.

The first physical target is the owner's x86-64 laptop. A freestanding UEFI x64 handoff is the current **candidate boot path**, subject to a machine inventory and authority review. A hosted x86-64 Linux probe is a separate, earlier experiment. Wasm remains an optional compilation target; no browser or Wasm width defines the system.

All project implementation is intended to be original first-party Rust with `#![no_std]` and no external implementation code. External design references and build tools are kept outside the implementation boundary; linked and generated code must be audited before admission. No implementation has been admitted yet.
