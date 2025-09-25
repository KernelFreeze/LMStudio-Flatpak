# LM Studio Flatpak

Unofficial Flatpak packaging recipe for LM Studio.

## Quick Start
- Build locally: `flatpak-builder --user --install-deps-from=flathub builddir ai.lmstudio.LMStudio.yml`
- Launch after install: `flatpak run ai.lmstudio.LMStudio`
- Export a repository: `flatpak-builder --user --repo=repo --force-clean builddir ai.lmstudio.LMStudio.yml`

## Project Notes
- `ai.lmstudio.LMStudio.yml` is the manifest; adjust module URLs, hashes, and finish args when updating upstream releases.
- `apply_extra.sh` runs inside the sandbox to unpack the AppImage into `/app/extra/bin`.
- Runtime data persists via `--persist` directories listed in the manifest.

