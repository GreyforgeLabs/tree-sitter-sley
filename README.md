    # Tree-sitter Sley

    Tree-sitter grammar, highlight queries, and editor parser scaffolding for Sley source.

    Status: private Sley ecosystem scaffold. This repository is intentionally
    built as a detailed starting point before public release.

    ## Why This Exists

    Sley is an agent-native structural language. Source remains the human review
    projection, while the compiler exposes stable JSON surfaces for graph,
    lint, query, edit planning, verification, trace receipts, and ZJX handoff.

    `tree-sitter-sley` exists to make that loop easier for editor users, documentation authors, and review tool builders.

    ## Current Scope

    - Priority: `P0`
    - Utility class: `syntax grammar`
    - Default mode: local and deterministic
    - Write mode: disabled unless explicitly documented by the command
    - Network calls: none in tests or examples
    - Provider, deploy, spend, wallet, and secret access: not used

    ## Quick Start

    ```bash
    make smoke
    ```

    Useful commands:

    - `tree-sitter generate`
- `tree-sitter test`
- `npm run smoke`

    ## Consumed Sley Contracts

    This tool treats Loom, the Sley compiler, as the oracle. It consumes these
    Sley surfaces instead of duplicating compiler logic:

    - `human-reviewable .sley source`

    Details live in [`docs/contracts.md`](docs/contracts.md).

    ## Repository Layout

    - `assets/branding/` - repo mark, social card, banner, and generated PNGs
    - `docs/` - architecture, contract, brand, and SEO notes
    - `examples/` - minimal Sley fixtures for local smoke work
    - `test/` - smoke tests that avoid network and external systems
    - `Makefile` - `fmt`, `test`, and `smoke` entry points

    Includes `grammar.js`, highlight queries, corpus fixtures, and smoke checks that can run before Tree-sitter is installed.

    ## Release Policy

    This repository stays private until:

    - consumed Sley schema versions are declared;
    - deterministic local tests pass;
    - examples work against the current Sley compiler;
    - public-use branding is reviewed;
    - docs avoid private local paths;
    - write paths, if any, preview through `sley fix --dry-run` or
      `sley graft --dry-run` before mutation.

    ## SEO Surface

    Draft SEO title: `Tree-sitter Sley - Sley developer tooling`

    Draft description: Parse and highlight Sley source with Tree-sitter so modules, tasks, takes, effects, bindings, and checked calls are readable in editors.

    Future canonical URL: `https://sley.greyforge.tech/tools/tree-sitter-sley`

    GitHub URL while private: `https://github.com/GreyforgeLabs/tree-sitter-sley`

    ## License

    MIT. See [`LICENSE`](LICENSE).

    Autonomy, Engineered.
