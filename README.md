# pi-agent-orchestrator-assets

Binary showcase media for [`pi-agent-orchestrator`](https://github.com/OnlineChefGroep/pi-agent-orchestrator).

Keep large `*.mp4` / `*.gif` files here so the extension repository stays clone-light.

## Layout

```
images/
  dashboard_preview.mp4
  product_film.mp4
  …
```

## Use from the orchestrator checkout

```bash
# sibling clone
git clone git@github.com:OnlineChefGroep/pi-agent-orchestrator-assets.git ../pi-agent-orchestrator-assets
cd ../pi-agent-orchestrator
npm run assets:link
```

Or set `ORCHESTRATOR_MEDIA_DIR` to this repository root (or its `images/` directory).
