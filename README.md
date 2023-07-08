# Vanilla OS Nvidia Image
Containerfile for building a Vanilla OS Desktop+Nvidia image.

This image is based on top of vanillaos/desktop and offers the default
Vanilla OS Desktop experience with GNOME and Nvidia drivers.

## Build

```bash
sh prepare.sh
podman image build -t vanillaos/nvidia .
```
