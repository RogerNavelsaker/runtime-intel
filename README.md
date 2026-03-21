# runtime-intel

Meta-project for code intelligence, repository mapping, and runtime integration tooling under `RogerNavelsaker/*`.

This umbrella groups the repos that help agents understand codebases or integrate runtime-specific behavior, without mixing them into the general CLI packaging layer. It now also serves as the shared workspace entrypoint for that slice.

## Repositories

| Repository | Focus |
| --- | --- |
| [code-intel-ts](https://github.com/RogerNavelsaker/code-intel-ts) | TypeScript code intelligence tooling |
| [code-intel-rust](https://github.com/RogerNavelsaker/code-intel-rust) | Rust code intelligence tooling |
| [repo-map](https://github.com/RogerNavelsaker/repo-map) | Repository structure and mapping support |
| [os-eco-pi-extension](https://github.com/RogerNavelsaker/os-eco-pi-extension) | Pi runtime integration for Overstory-managed sessions |

## Scope

- Group code understanding and repo-shape tooling together
- Keep runtime extensions visible as first-class infrastructure, not ad hoc patches
- Separate runtime integration work from CLI packaging repositories

## Shared Workspace

- Preferred layout: clone this repo as `~/Repositories/@runtime-intel` and keep the underlying repos as sibling directories under `~/Repositories`
- Shell: Flox + `direnv` via [manifest.toml](/home/rona/Repositories/@runtime-intel/.flox/env/manifest.toml) and [.envrc](/home/rona/Repositories/@runtime-intel/.envrc)
- Workspace file: [runtime-intel.code-workspace](/home/rona/Repositories/@runtime-intel/runtime-intel.code-workspace)
- Bootstrap missing sibling repos with `./scripts/bootstrap`
- Inspect workspace state with `./scripts/status`
- Submodules are intentionally not used

## Related Meta Projects

- [agent-clis](https://github.com/RogerNavelsaker/agent-clis) for packaged CLI wrappers
- [nix-repos](https://github.com/RogerNavelsaker/nix-repos) for Nix workspace tooling and shared infrastructure
