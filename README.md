# hookworks

A Claude Code marketplace for mods by Alex Zhao. This repository holds only the catalog, `.claude-plugin/marketplace.json`; each mod lives in its own repository.

## Add the marketplace

```sh
claude plugin marketplace add alexzhaobin/hookworks
```

Then install any mod below with `claude plugin install <mod>@hookworks`, or in one step from inside Claude Code:

```
/plugin install <mod> --marketplace alexzhaobin/hookworks
```

## Mods

| Mod | What it does | Install |
| --- | --- | --- |
| [token-usage-anatomy](https://github.com/alexzhaobin/token-usage-anatomy) | Shows how every prompt turns into input, output, cache-read and cache-write tokens: a chart above the prompt and an offline viewer page. No network, no telemetry. | `claude plugin install token-usage-anatomy@hookworks` |

Each entry installs from its repository's `main` branch, which holds released versions only.

## Adding or updating a mod

Edit the mod's entry in `.claude-plugin/marketplace.json` and check it:

```sh
claude plugin validate --strict .
```

CI runs the same check on every push.

## License

MIT, see [LICENSE](LICENSE).
