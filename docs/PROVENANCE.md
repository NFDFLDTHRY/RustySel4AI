# Provenance register — C01/P01

## Canonical source at arrival

| Field | Observation |
|---|---|
| Repository | [NFDFLDTHRY/RustySel4AI](https://github.com/NFDFLDTHRY/RustySel4AI), named by the owner |
| Branch | `main`, sole branch observed through the connected GitHub API |
| HEAD | `f16e023beb0edf6ff4a023e51d1c2e274c3ccb7a` (`Initial commit`) |
| Tree | `b2bc0b658356c10caef2069904f715ad896b76df` |
| Tracked paths | `README.md` and `LICENSE` only |
| Working status | `[UNK]` for any other person's checkout. Remote Git objects do not expose an uncommitted working tree; no local checkout was supplied. |
| Code provenance | `[OBS]` No implementation source or binary is tracked at this pinned tree. This does not audit future commits or external machines. |

The original `README.md` contains only `# RustySel4AI` with no trailing newline (13 bytes; blob `dee479cc754070b6b711adbf810a1c85f269f51e`; SHA-256 `ac7c2b60f8df7cb608713d7cc3569e879da6bedf27a6168428ecbe1442d70649`). The original `LICENSE` is Apache License 2.0 text (blob `261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64`; SHA-256 `c71d239df91726fc519c6eb72d318ec65820627232b2f796219e87dcf35d0ab4`). The C01 candidate preserves the LICENSE bytes.

## C01 candidate

All new project prose and the external bootstrap gate for this cycle were authored for RustySel4AI. No code was copied from FactTest, laceArc, LLVM, seL4, Blender, or another repository. The standard Apache license text is legal material retained from the owner's initial commit, not runtime implementation.

The external bootstrap tool is a temporary construction tool, not system code. Its interpreter and the connected GitHub service sit outside the project's implementation boundary. They may attest only the checked documentary mutation and must be replaced or requalified before admitting implementation.

Before the first executable artifact, extend this register to enumerate each source crate, generated file, linked object, Rust `core`/builtins component, entry code, firmware dependency, and toolchain with origin, version, hash, rights, and admission decision. `[GAP]` No binary provenance audit or laptop inspection exists yet.

## Reference boundary

FactTest demonstrates a prior factory/compiler construction line, and laceArc records Lace research. Neither repository is this repository's canonical base. Their implementations and contracts may be examined as references but are not imported or grandfathered into RustySel4AI.
