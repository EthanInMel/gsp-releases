# gsp releases

Prebuilt binaries of `gsp`, the GitSteam packaging and index tool.

Each release is tagged `gsp-v<version>` and contains:

- `gsp-linux-x64`: static x86-64 Linux binary (musl), used by index repository workflows
- `gsp-windows-x64.exe`: Windows x64 binary
- `SHA256SUMS`: SHA-256 checksums for the files above

Always check the checksum before running a downloaded binary:

```bash
curl -fsSLO https://github.com/EthanInMel/gsp-releases/releases/download/gsp-v<version>/gsp-linux-x64
curl -fsSLO https://github.com/EthanInMel/gsp-releases/releases/download/gsp-v<version>/SHA256SUMS
sha256sum -c --ignore-missing SHA256SUMS
```

Index workflows pin both the version and the SHA-256 of `gsp-linux-x64`.

This repository contains release binaries only. There is no source code here.
