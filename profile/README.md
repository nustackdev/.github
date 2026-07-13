# nustack

Assemble software, don't write it.

Nu program is an Interaction over Refs composed as a tree:

- **Ref** names any resource. A KV item, a UI widget, a remote endpoint, a memory slot.
- **Interaction** is the work over Refs. Read, write, compute, branch, iterate, compose.
- **Fabric** implements Refs against a concrete backend. Swap Fabrics, keep the tree.

Distribution, persistence, reactivity, atomicity, and observability come out as tree transformations.

50x less code for humans, 50x less tokens for agents, than writing it line by line in imperative Python.

## Repos

**Core**

- [interaction-model](https://github.com/nustackdev/interaction-model) - The model canonical spec.
- [nu](https://github.com/nustackdev/nu) - Python implementation of the model (`nu.m`, `nu.v`, `nu.ui`, `nu.invisibles`, `nu.ray`).

**Apps**

- [nulog](https://github.com/nustackdev/nulog). Structured logging as a Nu app.

## Start

```bash
pip install nu[default]
```

Full model and docs at [nustack.dev](https://nustack.dev).
