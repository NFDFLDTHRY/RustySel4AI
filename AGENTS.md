# RustySel4AI working entry

Read in order: [README.md](README.md) -> [docs/LAW.md](docs/LAW.md) -> [docs/SYSTEM.md](docs/SYSTEM.md) -> [docs/CONTRACTS.md](docs/CONTRACTS.md) -> [docs/CYCLES.md](docs/CYCLES.md) -> [docs/HANDOFF.md](docs/HANDOFF.md). Check [docs/PROVENANCE.md](docs/PROVENANCE.md) and [docs/EVIDENCE.md](docs/EVIDENCE.md) before making an evidence claim.

The repository is at **C01/P01**. P02-P06 are plans only. The only accepted implementation content at this point is none. Treat every `[NEW]` diagram or candidate target as a proposal, never as a running system.

Before any change, pin the branch, HEAD, tree, and working status; read the latest handoff and the contract consumers affected. Preserve other work. Route every change through the current approved factory. If that factory is absent, build and attack an original bootstrap outside the canonical checkout; use its independent gate and receipt to admit only a bounded workpiece. An agent never writes directly to the canonical tree as an ordinary edit.

Use the status vocabulary `[OBS]` inspected, `[RUN]` executed, `[NEW]` proposed, `[GAP]` missing, `[ERR]` contradiction/failure, and `[UNK]` unknown. Record prediction and actual result separately. A container probe is not a laptop or kernel result.

Do not import, vendor, translate, wrap, or link foreign implementation code into this project. LLVM, seL4, Blender, FactTest, and laceArc may inform questions and test designs; none is project implementation by default. Rust `core`, compiler builtins, startup objects, firmware interfaces, and generated objects need a provenance decision before any binary claim.

The current intended native path is x86-64 with a candidate UEFI x64 boot handoff. Machine-specific firmware, devices, memory map, interrupt controller, and storage interfaces remain `[UNK]` until inventoried on the owner's laptop. Wasm is another possible target. Do not revive a browser-only or wasm64-only restriction.
