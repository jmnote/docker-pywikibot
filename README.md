# Pywikibot Docker Image

[![Build](https://github.com/jmnote/docker-pywikibot/actions/workflows/build.yml/badge.svg)](https://github.com/jmnote/docker-pywikibot/actions/workflows/build.yml)
[![Docker Pulls](https://img.shields.io/docker/pulls/jmnote/pywikibot)](https://hub.docker.com/r/jmnote/pywikibot)
[![GitHub Container Registry](https://img.shields.io/badge/GHCR-jmnote%2Fpywikibot-blue)](https://github.com/jmnote/docker-pywikibot/pkgs/container/pywikibot)

This repository provides the Docker build configuration for [Pywikibot](https://www.mediawiki.org/wiki/Manual:Pywikibot), automatically tracking upstream tags from [wikimedia/pywikibot](https://github.com/wikimedia/pywikibot).

Each image matches a tag of this repository named after the Pywikibot release (`X.Y.Z`):

- **Tag** (weekly, Sundays 00:00 UTC): tags this repository with the latest stable upstream release if it is not tagged yet, then starts **Build** on the new tag.
- **Build** (on a tag): builds that upstream release, pushes multi-architecture images to both **Docker Hub** and **GitHub Container Registry (GHCR)**, and creates the GitHub release of the tag. `latest` (image and release) moves only for the highest tag.

To build a release by hand, push its tag (`git tag 11.8.0 && git push origin 11.8.0`), or run Build on an existing tag.

## Features

- **Multi-Architecture:** Supports `linux/amd64` and `linux/arm64`.
- **Automated Builds:** Tags and builds new upstream releases weekly.
- **Semantic Versioning:** Provides `latest`, major (`X`), minor (`X.Y`), and patch (`X.Y.Z`) tags.

## Image Registries

You can pull the image from either registry:

### Docker Hub
```bash
docker pull jmnote/pywikibot:latest
```

### GitHub Container Registry
```bash
docker pull ghcr.io/jmnote/pywikibot:latest
```
