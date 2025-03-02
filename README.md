# Vanilla OS Nvidia Alternative Image

Containerfile for building a Vanilla OS Desktop + Nvidia image modified to use an older driver.

This image is based on top of [`vanillaos/nvidia`](https://github.com/Vanilla-OS/nvidia-image/pkgs/container/nvidia) and offers the default Vanilla OS Desktop experience with GNOME and Older Nvidia drivers.

## Build

> [!NOTE]
> The fsguard compiled plugin `.so` file should be downloaded from the [latest release](https://github.com/Vanilla-OS/vib-fsguard/releases/latest) and be placed under a `plugins` directory beside the `recipe.yml` file.

```bash
vib build recipe.yml
podman image build -t vanillaos/nvidia-alternative .
```

## Verify Image Build Provenance Attestation

All the image builds/pushes are attested for build provenance and integrity using the [attest-build-provenance](https://github.com/actions/attest-build-provenance) action. The attestations can be verified [here](https://github.com/Vanilla-OS/nvidia-image/attestations) or by having the latest version of [GitHub CLI](https://github.com/cli/cli/releases/latest) installed in your system. Then, execute the following command:

```sh
gh attestation verify oci://ghcr.io/vanilla-os/nvidia-alternative:main --owner Vanilla-OS
```
