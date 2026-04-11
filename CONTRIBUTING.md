# Contributing to Coral

Thanks for your interest in contributing. Coral is a solo-maintained open source project and contributions are genuinely appreciated.

## Before you start

- Check if an issue already exists for what you want to work on
- For new features, open an issue first to discuss before writing code
- For new module ideas, use the **New Module Idea** issue template and start a discussion — not every idea will be accepted, and that's okay

## The three rules

Every Coral module (and contribution to one) must respect these:

1. **Docker native** — ships as a container, configured via environment variables only
2. **Jellyfin as source of truth** — modules never share a database; they talk through the Jellyfin API
3. **MIT forever** — no paid features, no telemetry, no lock-in

## Running a module locally

Each module has its own `README.md` with local dev instructions. The general pattern is:

```bash
cp .env.example .env
# Fill in JELLYFIN_URL, JELLYFIN_API_KEY, JELLYFIN_USER_ID
pnpm install
pnpm dev
```

You'll need a running Jellyfin instance to test against. A local Docker instance works fine:

```bash
docker run -d --name jellyfin -p 8096:8096 jellyfin/jellyfin
```

## Using @get-coral/jellyfin

All modules use the shared Jellyfin client. Import from the package, not from local files:

```ts
import { createClient, getLibraryItems } from '@get-coral/jellyfin'
```

If you find a missing API endpoint, open an issue or PR in the [jellyfin](https://github.com/Get-Coral/jellyfin) repo rather than adding one-off fetch calls in your module.

## Commit convention

We use [Conventional Commits](https://www.conventionalcommits.org). This is required — release-please uses it to determine version bumps and generate changelogs automatically.

| Prefix | When to use | Version bump |
|--------|-------------|--------------|
| `feat:` | New feature or capability | Minor |
| `fix:` | Bug fix | Patch |
| `chore:` | Maintenance, deps, config | None |
| `docs:` | Documentation only | None |
| `refactor:` | Code change with no behaviour change | None |
| `feat!:` or `fix!:` | Breaking change | Major |

Examples:
```
feat: add subtitle track selection to playback session
fix: handle 401 refresh loop in playback auth
chore: bump @get-coral/jellyfin to 0.2.0
docs: add getLibraryItems options table to README
feat!: rename fromJellyfin to mapItem
```

## Pull requests

- Keep PRs focused — one thing per PR
- Reference the related issue with `Closes #N`
- Fill in the PR template fully
- All PRs are merged by squash — your commit history doesn't need to be clean

## CI

Every PR runs:
- `pnpm build` — TypeScript compilation + tsup bundle
- `pnpm check` — Biome lint + format

Both must pass before merging. Fix any issues locally with `pnpm check --write`.

## Questions?

Open a [Discussion](https://github.com/Get-Coral/.github/discussions) rather than an issue. The Help category is for support questions, Roadmap is for direction conversations.
