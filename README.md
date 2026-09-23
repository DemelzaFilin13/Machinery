# Machinery Model Viewer

This repository contains a static `<model-viewer>` page for the Machinery
model. The page loads the GLB model and its local poster, environment, and AR
image assets from the repository root.

## Local preview

Serve the repository root over HTTP (rather than opening `index.html` directly)
so that the model and module load consistently:

```powershell
python -m http.server 8000
```

Then open <http://localhost:8000/> in a browser and stop the server with
`Ctrl+C`.

## GitHub Pages

The workflow in `.github/workflows/pages.yml` deploys the repository root on
pushes to `main`. After Pages is enabled for the repository, the site is
available at:

`https://<owner>.github.io/<repository>/`

Keep `Big_Bucket.glb` and the other image and stylesheet assets committed;
they are required by the viewer at runtime.
