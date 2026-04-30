# pwx-image-base-python-3-10

This project provides a Python 3.10 base environment image, managed by Kaptain. It is built on top of `python:3.10.20-slim` and includes essential utilities for cloud-native workflows.

## Features

- **Base Image:** `python:3.10.20-slim`
- **System Packages:** `ca-certificates`, `netbase`, `tzdata`.
- **Kaptain Integration:** Uses `KaptainPM.yaml` for build configuration and metadata.

## Structure

- `src/docker/Dockerfile`: The main Dockerfile definition.
- `KaptainPM.yaml`: Kaptain package manager configuration defining the build type and environment layers.
- `.github/workflows/build.yaml`: CI/CD configuration using Kube-Kaptain GitHub Actions for automated builds.

## Building

This project is designed to be built using [Kaptain](https://kaptain.org).

```bash
kaptain build
```

## Usage

The image is intended to be used as a base for other Python-based applications that require standard cloud-native tooling.

```dockerfile
FROM pwx-image-base-python-3-10:latest
# Your application code here
```

## Maintenance

The GitHub Action automatically builds and pushes the image on changes to the `main*` branches.
