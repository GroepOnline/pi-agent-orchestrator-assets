# pi-agent-orchestrator-assets

Canonical binary showcase-media repository for [`GroepOnline/pi-agent-orchestrator`](https://github.com/GroepOnline/pi-agent-orchestrator). Large MP4/GIF/PNG assets live here so the extension repository remains clone-light while the public package page can still ship real product media.

## Relationship to the main repository

- **Source/runtime/docs:** [`GroepOnline/pi-agent-orchestrator`](https://github.com/GroepOnline/pi-agent-orchestrator)
- **Binary showcase source of truth:** this repository
- **Public showcase site:** <https://orchestrator.chefgroep.online/>
- **Stable package video URL:** <https://groeponline.github.io/pi-agent-orchestrator/assets/dashboard_preview.mp4>

The main repository owns scripts, rendering logic, documentation, release policy, and the `pi.video` manifest field. This repository owns the resulting heavyweight media. Do not duplicate large media into the npm package.

## Layout

```text
images/
  dashboard_preview.mp4
  dashboard_preview.gif
  dashboard_preview.svg
  product_film.mp4
  showcase_*.mp4
  showcase_*.gif
  orchestrator_banner.png
  orchestrator_architecture.png
```

## Use from an orchestrator checkout

```bash
git clone git@github.com:GroepOnline/pi-agent-orchestrator-assets.git ../pi-agent-orchestrator-assets
cd ../pi-agent-orchestrator
npm run assets:link
```

Or set `ORCHESTRATOR_MEDIA_DIR` to this repository root (or its `images/` directory).

## Publishing contract

1. Render or capture from the real `pi-agent-orchestrator` implementation.
2. Store heavyweight outputs in this repository under `images/`.
3. Keep lightweight SVG previews and documentation references in the main repo where useful.
4. Run the main repository's media verification before release.
5. Keep stable public URLs in the main package manifest and README; this repo remains the binary source of truth.

When a showcase asset is replaced, preserve its purpose and filename when the public URL is intended to remain stable.
