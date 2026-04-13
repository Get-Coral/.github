<div align="center">

# 🪸 Coral

### A reef of independent Docker modules that extend Jellyfin with modern UX.
### Each one alive on its own — thriving together.

[![License: MIT](https://img.shields.io/badge/License-MIT-ff6b6b?style=flat-square)](https://opensource.org/licenses/MIT)
[![Docker](https://img.shields.io/badge/Docker-ghcr.io%2Fget--coral-2dd4bf?style=flat-square&logo=docker&logoColor=white)](https://github.com/orgs/Get-Coral/packages)
[![npm](https://img.shields.io/badge/npm-%40get--coral-ff6b6b?style=flat-square&logo=npm&logoColor=white)](https://www.npmjs.com/org/get-coral)
[![Website](https://img.shields.io/badge/Website-getcoral.dev-2dd4bf?style=flat-square)](https://getcoral.dev)
[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-ff6b6b?style=flat-square&logo=github-sponsors)](https://github.com/sponsors/ElianCodes)

---

## The Modules

| Module | What it does | Status |
|--------|-------------|--------|
| [🎬 Aurora](https://github.com/Get-Coral/aurora) | High-end cinematic Jellyfin frontend | 🟢 In Progress |
| [🎤 KAPOW!](https://github.com/Get-Coral/KAPOW) | Karaoke queue manager for bars & events | 🟡 MVP Built |
| [📖 Fathom](https://github.com/Get-Coral/fathom) | Modern reading app from your NAS | ⚪ Planned |
| [📺 Marquee](https://github.com/Get-Coral/marquee) | Ambient now-playing display | ⚪ Planned |
| [🎶 Encore](https://github.com/Get-Coral/encore) | Guest media request system | ⚪ Planned |
| [🗂️ Librarian](https://github.com/Get-Coral/librarian) | Smart media management layer | ⚪ Planned |

## Shared Packages

| Package | What it does |
|---------|-------------|
| [📦 create-coral](https://www.npmjs.com/package/create-coral) | Scaffold a new Coral module from the official template |
| [📦 @get-coral/jellyfin](https://www.npmjs.com/package/@get-coral/jellyfin) | TypeScript Jellyfin API client |
| [📦 @get-coral/biome-config](https://www.npmjs.com/package/@get-coral/biome-config) | Shared Biome configuration for Coral repositories |
| [📦 @get-coral/tsconfig](https://www.npmjs.com/package/@get-coral/tsconfig) | Shared TypeScript configuration for Coral repositories |

---

## Three Rules

**🐳 Docker native** — Every module ships as a container. One Compose file, one command, running on your NAS.

**🪸 Jellyfin as source of truth** — Modules never share a database. Communication happens through the Jellyfin API.

**🔓 MIT forever** — No paid tier, no SaaS, no cloud dependency. Sponsor if it brings you value.

</div>

---

## Get Started

```yaml
# docker-compose.yml
services:
  kapow:
    image: ghcr.io/get-coral/kapow:latest
    ports: ["3000:3000"]
    environment:
      JELLYFIN_URL: http://your-nas:8096
      JELLYFIN_API_KEY: your_key
  db:
    image: postgres:alpine
```

---

<div align="center">

## Contributing

All modules are open to contributions. Each repo has its own `CONTRIBUTING.md`.
Found a bug? Open an issue in the relevant module repo.
Have a module idea? Start a [discussion](https://github.com/Get-Coral/.github/discussions).

---

<sub>Built by <a href="https://elian.codes">@ElianCodes</a> · Born at Comic Sans bar in Ghent 🍺</sub>

</div>
