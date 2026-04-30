# Local Development

## Summary

1.  [Runtime Choice](#runtime-choice)
2.  [Preview](#preview)
3.  [Build Check](#build-check)
4.  [Docker Mount Note](#docker-mount-note)
5.  [Troubleshooting](#troubleshooting)

## Runtime Choice

The default local runtime is Docker. This keeps Ruby and Jekyll out of the host
environment and makes the preview reproducible across machines.

## Preview

```bash
docker compose up --build
```

Open:

```text
http://localhost:4000
```

## Build Check

```bash
docker build -t marcosgvjunior-github-io .
docker run --rm marcosgvjunior-github-io bundle exec jekyll build --trace
```

## Docker Mount Note

The compose file intentionally does not bind-mount `.:/site`. In some
Docker-outside-of-Docker environments, the Docker daemon does not see the same
workspace path as the development shell. A bind mount can then hide the files
copied into the image and make Jekyll fail to find `Gemfile`.

The trade-off is that local preview is stable but not true live reload. Rebuild
the container after content or layout changes.

## Troubleshooting

- If port `4000` is busy, stop the old container with `docker compose down`.
- If the page does not refresh after edits, rebuild with
  `docker compose up --build`.
- If Jekyll cannot find `Gemfile`, confirm that the compose file is not mounting
  an empty workspace over `/site`.
