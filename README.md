# runtime-intel

Meta-project for code intelligence, repository mapping, and runtime integration tooling under `RogerNavelsaker/*`.

This umbrella groups the repos that help agents understand codebases or integrate runtime-specific behavior, without mixing them into the general CLI packaging layer.

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

## Related Meta Projects

- [agent-clis](https://github.com/RogerNavelsaker/agent-clis) for packaged CLI wrappers
- [nix-repos](https://github.com/RogerNavelsaker/nix-repos) for Nix workspace tooling and shared infrastructure
