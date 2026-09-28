# charly-comfyui

The `charly-comfyui` family — the ComfyUI image-generation command skills.

The `charly-comfyui` candy is a **concept candy**: it ships no install content
and owns the `comfyui` family of `skill:` entities whose names have no namesake
candy. It currently carries the `comfyui-layer` skill (the ComfyUI
image-generation service). `candy/plugin-marketplace` regenerates the standalone
[opencharly/marketplace](https://github.com/opencharly/marketplace) corpus from
these entities, so the skills are authored here and projected there.

## What it provides

| Property | Value |
|---|---|
| Layer / candy | `charly-comfyui` (concept candy) |
| Install content | none — a `true` no-op `plan:` |
| Owns | 1 `skill:` entity: `comfyui-layer` |
| Projected to | `marketplace/comfyui/skills/` |
| Service / port | none |

## How to use it

This repo is consumed as a **skill source**, not as an image layer. Edit the
`skill:` entities in `charly.yml`; the marketplace regeneration projects them
into `/charly-comfyui:*` pages. To reference the repo directly:

```yaml
my-box:
  candy:
    base: fedora
    candy:
      - '@github.com/opencharly/layer-charly-comfyui:v2026.243.2059'
```

## Layout

- `charly.yml` — the `charly-comfyui:` concept candy entity plus the
  `comfyui-layer-skill:` entity.
- `.github/workflows/tag-on-merge.yml` — CalVer tag + `CHANGELOG/` on merge.
- `README.md` — this user overview.

## Related

- Owning skill: `/charly-comfyui:comfyui-layer`
- Authoring reference: `/charly-image:layer`
- [`opencharly/marketplace`](https://github.com/opencharly/marketplace) — the projected corpus
- [`opencharly/charly`](https://github.com/opencharly/charly) — the charly CLI and image builder
- [`opencharly/opencharly`](https://github.com/opencharly/opencharly) — the umbrella
