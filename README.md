# Navi updates

Signed firmware releases for Navi, the fairy desk companion. This repository
holds release files only; the source code is private.

Each release has two files:

- `manifest.json`: the version, size and SHA-256 of the firmware, signed with
  Navi's private release key (ECDSA P-256).
- `firmware.bin`: the firmware itself.

Navi checks the latest release about once a day. She installs an update only
if the manifest's signature matches the public key built into her firmware,
the download matches the signed size and SHA-256, and the version is newer.
She asks her owner first: the update appears on her About screen, and it
installs only after a press of her BOOT button.
