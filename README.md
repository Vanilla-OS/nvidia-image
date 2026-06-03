# Vanilla OS GNOME NVIDIA Image

Containerfile for building a Vanilla OS GNOME + NVIDIA image.

This image is based on top of [`vanillaos/gnome`](https://github.com/Vanilla-OS/desktop-image/pkgs/container/gnome) and offers the default Vanilla OS Desktop experience with GNOME and NVIDIA drivers.

## Build

```bash
vib build recipe.yml
podman image build -t vanillaos/gnome-nvidia .
```

## Verify Image Build Provenance Attestation

All the image builds/pushes are attested for build provenance and integrity using the [attest-build-provenance](https://github.com/actions/attest-build-provenance) action. The attestations can be verified [here](https://github.com/Vanilla-OS/nvidia-image/attestations) or by having the latest version of [GitHub CLI](https://github.com/cli/cli/releases/latest) installed in your system. Then, execute the following command:

```sh
gh attestation verify oci://ghcr.io/vanilla-os/gnome-nvidia:latest --owner Vanilla-OS
```
