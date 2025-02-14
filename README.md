# docker-anki-syncserver

[![Docker](https://github.com/sdvcrx/docker-anki-syncserver/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/sdvcrx/docker-anki-syncserver/actions/workflows/docker-publish.yml)
![Docker Image Version](https://img.shields.io/github/v/tag/sdvcrx/docker-anki-syncserver)

Docker image for deploying Official [Anki Sync Server](https://github.com/ankitects/anki/tree/main/docs/syncserver) for running a self-hosted sync server.

## Usage

Pull the Docker image from [ghcr.io](https://github.com/sdvcrx/docker-anki-syncserver/pkgs/container/anki-syncserver)

```bash
# latest docker version
docker pull ghcr.io/sdvcrx/anki-syncserver

# or by version
docker pull ghcr.io/sdvcrx/anki-syncserver:25.02
```

## Example

### CLI

Please reference [Anki Sync Server docs](https://github.com/ankitects/anki/tree/main/docs/syncserver#run-container) .

Example: 

```
docker run -d \
    -e "SYNC_USER1=admin:admin" \
    -p 8080:8080 \
    --mount type=volume,src=anki-sync-server-data,dst=/anki_data \
    --name anki-sync-server \
    ghcr.io/sdvcrx/anki-syncserver
```

## Development

This repo uses [GitHub Actions](https://github.com/sdvcrx/docker-anki-syncserver/blob/main/.github/workflows/check-update.yml) to keep the Anki Sync Server version up to date.
