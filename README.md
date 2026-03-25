# runtime-intel

Meta-project for code intelligence, repository mapping, and runtime integration tooling under `RogerNavelsaker/*`.

This umbrella groups the repos that help agents understand codebases or integrate runtime-specific behavior, without mixing them into the Nix packaging layer. It now serves as the shared workspace entrypoint for the binary/source side of that work.

## Repositories

| Repository | Focus |
| --- | --- |
| [code-intel-ts](https://github.com/RogerNavelsaker/code-intel-ts) | TypeScript code intelligence CLI |
| [code-intel-rust](https://github.com/RogerNavelsaker/code-intel-rust) | Rust code intelligence CLI |
| [context-mode-cli](https://github.com/RogerNavelsaker/context-mode-cli) | CLI binary for context-mode workflows |
| [context-mode-mcp](https://github.com/RogerNavelsaker/context-mode-mcp) | MCP server binary for context-mode workflows |
| [nixos-cli](https://github.com/RogerNavelsaker/nixos-cli) | Bun CLI wrapper for the Flox-provisioned NixOS MCP server |
| [pi-context-mode](https://github.com/RogerNavelsaker/pi-context-mode) | Pi runtime integration for context-mode |
| [pi-os-eco](https://github.com/RogerNavelsaker/pi-os-eco) | Pi runtime integration for Overstory-managed sessions |
| [repo-map](https://github.com/RogerNavelsaker/repo-map) | Repository mapping CLI |
| [toolflow-mcp](https://github.com/runtime-intel/toolflow-mcp) | Pipe-oriented MCP server with config-loaded verbs and plugins |

## Scope

- Group runtime binaries, source repos, and integration layers together
- Keep runtime extensions visible as first-class infrastructure, not ad hoc patches
- Separate runtime integration work from `nixpkg-*` packaging repositories

## Shared Workspace

- Preferred layout: clone this repo as `~/Repositories/@runtime-intel` and keep the underlying repos as ignored child directories inside `@runtime-intel/`
- Shell: Flox + `direnv` via [manifest.toml](/home/rona/Repositories/@runtime-intel/.flox/env/manifest.toml) and [.envrc](/home/rona/Repositories/@runtime-intel/.envrc)
- Workspace file: [runtime-intel.code-workspace](/home/rona/Repositories/@runtime-intel/runtime-intel.code-workspace)
- Bootstrap missing sibling repos with `./scripts/bootstrap`
- Inspect workspace state with `./scripts/status`
- Submodules are intentionally not used

## Notes

- `nixpkg-code-intel-ts`, `nixpkg-code-intel-rust`, and `nixpkg-repo-map` moved to [@nixpkgs](/home/rona/Repositories/@nixpkgs).
- `code-intel-ts`, `code-intel-rust`, and `repo-map` now exist as standalone source repos in this workspace.
- The stray `mcp-nixos-upstream-1774376952/` scratch clone was removed.
- `nixos-mcp-upstream` was removed because it is not used in this workspace.
- `nixos-mcp` was removed because this workspace consumes `utensils/nixos-mcp` directly as a Flox-installed Nix package instead of using a local checkout.
- `nixos-mcp-cli` has been replaced by the owned [nixos-cli](https://github.com/RogerNavelsaker/nixos-cli) repo.

## Related Meta Projects

- [nixpkgs](/home/rona/Repositories/@nixpkgs) for packaged Nix wrappers
- [nix-repos](https://github.com/RogerNavelsaker/nix-repos) for Nix workspace tooling and shared infrastructure
