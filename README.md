# 🤖 claudemgr/android

Template specifications for CasjaysDev Android projects. Each file is a master template — copied into a generated project as `AI.md` — covering the full project lifecycle from layout and build system through CI/CD, testing, signing, and release.

## Templates

| File | App type | When to use |
|------|----------|-------------|
| `APPLICATION.md` | Kotlin Android application | Any new or existing Android app — phone-first, with opt-in wear/tv/auto/widget form factors; Compose by default, views for existing apps |

## Files

| File | Purpose |
|------|---------|
| `APPLICATION.md` | Android application template — source of truth for Android projects (PARTs 0–14) |
| `README.md` | This file |
| `LICENSE.md` | Repository license (WTFPL) |

## Highlights

- All builds run inside Docker via `casjaysdev/android:latest` — no host SDK, Gradle, or JDK
- Store targets default to F-Droid + provider releases (GitHub/GitLab/Gitea/Forgejo); Google Play is opt-in
- Applicability matrix in `IDEA.md` gates the conditional PARTs (database, network, notifications, background work, backup/sync, media)
- `applicationId` is treated as frozen forever; existing apps keep their shipped identity

## Related

`IDEA.md` and `CLAUDE.md` are not stored here — they are generated inside each project that uses this template. Global implementation conventions live in `~/.claude/memory/` (dockerfile_conventions.md, cicd_conventions.md, testing_conventions.md, etc.).

## License

This repository (the template itself) is licensed under **WTFPL** — see [LICENSE.md](LICENSE.md).

Projects generated from this template are licensed under **MIT** (each generated project ships its own `LICENSE.md`).
