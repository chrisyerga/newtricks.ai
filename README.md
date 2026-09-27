# newtricks.ai

Public website for newtricks.ai. For now it is a small Caddy container that sends a temporary (302) redirect to https://lindale.tech.

Pushing to `main` builds the image and deploys it to milo through Porch (see `PORCH.md`).

## Replacing the redirect with the Astro site

Follow the `../abbot` setup: add the Astro project, turn the `Dockerfile` into a Node build stage plus a `caddy file-server` runner stage, and add `npm ci` / `npm run build` steps to the workflow. Keep the service id, container name, and port unchanged so Porch routing stays the same.
