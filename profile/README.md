# nustack

We are building **Nu** — a programming model where a program is an interaction over named resources, and the hard properties of real software (distribution, reactivity, durability, atomicity, observability) fall out as tree transformations, not framework layers.

- **Ref** names a resource — a db row, a UI widget, a remote endpoint, an in-memory slot.
- **Interaction** describes what to do with Refs — read, write, compute, branch, iterate, compose.
- **Context** binds Refs to concrete backends — swap it and the same program runs against RocksDB, an in-memory dict, a browser tab, or another machine.

## Repos

**Core**

- [nu](https://github.com/nustackdev/nu) — the model, its runtime, and the in-tree fabrics (`nu.mem`, `nu.virtuals`, `nu.nudle`, `nu.distributed`)

**Infra** — independent libraries Nu builds on; each knows nothing about Nu.

- [virtuals](https://github.com/nustackdev/virtuals) — virtual Python collections over any storage (RocksDB, LMDB, in-memory, text). Substrate for durable Shapes.
- [invisibles](https://github.com/nustackdev/invisibles) — transparent remote method invocation. Sync stays sync, async stays async.
- [composables](https://github.com/nustackdev/composables) — async service composition and lifecycle. Wires substrates, transports and coordinators together.

**Tools**

- [lens](https://github.com/nustackdev/lens) — live data explorer for Nu Shapes.
- [nulog](https://github.com/nustackdev/nulog) — Nu-native structured logger. A log line is a Nu WRITE; a query is a Nu Query.

## Getting started

```bash
pip install nu[default]
```

Then head to [nustackdev/nu](https://github.com/nustackdev/nu) for the model, examples, and the fabric catalog.

## Status

Alpha. APIs will break. Two production systems already run on Nu — a Solana trading platform and a reactive knowledge base.
