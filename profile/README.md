<div align="center">

# 🪸 Coral

### A reef of independent Docker modules that extend Jellyfin with modern UX.
### Each one alive on its own — thriving together.

[![License: MIT](https://img.shields.io/badge/License-MIT-coral.svg?style=flat-square&color=ff6b6b)](https://opensource.org/licenses/MIT)
[![Docker](https://img.shields.io/badge/Docker-ghcr.io%2Fget--coral-2dd4bf?style=flat-square&logo=docker&logoColor=white)](https://github.com/orgs/Get-Coral/packages)
[![Website](https://img.shields.io/badge/Website-getcoral.dev-ff6b6b?style=flat-square)](https://getcoral.dev)
[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-2dd4bf?style=flat-square&logo=github-sponsors)](https://github.com/sponsors/ElianCodes)

---

## The Modules

| Module | What it does | Status |
|--------|-------------|--------|
| [🎬 Aurora](https://github.com/Get-Coral/aurora) | High-end cinematic Jellyfin frontend | 🟢 In Progress |
| [🎤 KAPOW!](https://github.com/Get-Coral/kapow) | Karaoke queue manager for bars & events | 🟡 MVP Built |
| [📖 Fathom](https://github.com/Get-Coral/fathom) | Modern reading app from your NAS | ⚪ Planned |
| [📺 Marquee](https://github.com/Get-Coral/marquee) | Ambient now-playing display | ⚪ Planned |
| [🎶 Encore](https://github.com/Get-Coral/encore) | Guest media request system | ⚪ Planned |
| [🗂️ Librarian](https://github.com/Get-Coral/librarian) | Smart media management layer | ⚪ Planned |
| [🎞️ Reel](https://github.com/Get-Coral/reel) | Synchronized watch parties | ⚪ Planned |

---

## Three Rules

**🐳 Docker native** — Every module ships as a container. One Compose file, one command, running on your NAS.

**🪸 Jellyfin as source of truth** — Modules never share a database. Communication happens through the Jellyfin API.

**🔓 MIT forever** — No paid tier, no SaaS, no cloud dependency. Sponsor if it brings you value.

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

## Contributing

All modules are open to contributions. Each repo has its own `CONTRIBUTING.md`.
Found a bug across modules? Open an issue in the relevant repo.
Have an idea for a new module? Start a discussion in this repo.

---

<sub>Built by <a href="https://elian.codes">@ElianCodes</a> · Originally born at Comic Sans bar in Ghent 🍺</sub>

</div>
