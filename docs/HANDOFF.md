# Continuation entry — C01/P01

Start with [README](../README.md) → [LAW](LAW.md) → [SYSTEM](SYSTEM.md) → [CONTRACTS](CONTRACTS.md) → [CYCLES](CYCLES.md) → [EVIDENCE](EVIDENCE.md) and [PROVENANCE](PROVENANCE.md). The current authorized work is **C01/P01 setup**. P02–P06 are planned in [CYCLES](CYCLES.md) and have not been executed.

## Current position

- Canonical repository: `https://github.com/NFDFLDTHRY/RustySel4AI`, branch `main`. Pinned starting `HEAD=f16e023beb0edf6ff4a023e51d1c2e274c3ccb7a`, `tree=b2bc0b658356c10caef2069904f715ad896b76df` ([O-001](EVIDENCE.md)). The observed baseline has only `README.md` and `LICENSE`.
- The P01 documentary candidate passed a bounded external bootstrap gate, a separate witness, and nine denial cases; the first denied check and its repair remain in [EVIDENCE](EVIDENCE.md). To establish publication, read current `main` HEAD/tree and compare its path/blob inventory with the task's final receipt. If the remote base changed, reconcile without resetting or overwriting others' work.
- The task container audit is [O-002](EVIDENCE.md); Rust tool startup failed [E-001](EVIDENCE.md). The owner's laptop, boot route, executable system, Lace, factory, and views have no observed implementation here. Tests for those claims are **NOT RUN**.
- The selected candidate native path is freestanding x86-64, PE/COFF UEFI application entry, UEFI x64 calling convention, then a separately designed private kernel handoff. Laptop support and the detailed hardware/boot contract remain `[UNK]`.

## Immediate continuation before any implementation

1. Re-read the C01 publication record and current `main` commit/tree before new work. The C01 external gate was scoped to documentary files only. A future executable delta requires its own audited station, denied-effect witnesses, independent judge, receipt, and fresh base pin.
2. Keep `docs/SYSTEM.md` and `docs/CONTRACTS.md` as the single current map. When evidence changes a relation, revise affected contracts and consumers together and retain the old claim and supersession in the cycle/evidence history.
3. Do not create speculative crates or import reference implementation. Before a code station exists, declare its I/O, read/change limits, invariants, checks, receipt, and trusted judge. A repair is tested immediately.

## Next experiment to prepare — T-001, native path acceptance

**Question:** Does the owner's actual x86-64 laptop support the selected UEFI x64 entry and a narrow, first-party handoff without hidden foreign implementation or unbounded device assumptions?

**Preconditions:** owner-approved access to the laptop or a reliable inventory supplied by its owner; accepted P01 law/map; a separately audited build toolchain and isolated station before any boot artifact is run. The existing task container cannot answer this question.

**Read-only first measurement:** record laptop model/firmware mode and version, Secure Boot state, CPU features, memory map and available firmware interfaces, storage/display/input routes, and the exact evidence source/time. Mark every unavailable field `[UNK]`. Compare these observations to the PE/COFF/UEFI x64 candidate contract; do not assume firmware support from container architecture.

**Later execution probe, only after the measurement closes the path:** define the smallest original Rust `no_std` UEFI entry with a declared ABI, input/output, resource and permission bounds, expected observation, independent build/linked-byte provenance check, and recovery path. Run it as its own station, record raw result and any denied effects, and distinguish firmware execution from kernel execution. A boot failure is evidence, not a reason to change the contract silently.

**Prediction:** an inventory may confirm a usable UEFI x64 path or expose incompatible firmware/boot policy; there is no observed result yet. **Status: NOT RUN.** `STALE_IF` the laptop, firmware, boot policy, compiler/linker output, or selected handoff changes.

## Decision at the next boundary

If T-001 supports the selected native path, specify B-50/K-50 and its first narrow station; if it contradicts the path, record `[ERR]`, revise [LAW](LAW.md), [SYSTEM](SYSTEM.md), [CONTRACTS](CONTRACTS.md), and consumers with the owner's decision. In either case, P02 Lace remains a plan until explicitly begun. The next cycle must carry forward raw evidence, receipts, unresolved conflicts, and `STALE_IF` conditions.
