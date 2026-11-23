# XDesk apt repository

The image a new XDesk built-in Ubuntu 26.04 starts from (Releases, Actions → Image), and the packages it gets from XDesk: `xdesk-core`, what the system needs to run inside the
XDesk app (with the Adreno GPU drivers: lfdevs' Mesa over Ubuntu's, see `xdesk-gpu`). Sources and build scripts:
[n2ray/xdesk](https://github.com/n2ray/xdesk), `linux/`.

```
Types: deb
URIs: https://n2ray.github.io/xdesk-apt
Suites: resolute
Components: main
Signed-By: /usr/share/keyrings/xdesk-archive.asc
```

The app installs the version of `xdesk-core` it needs on its own, so a release here reaches every installed system:
it is published only by hand (Actions → Publish). The signing key lives only in this repository's Actions secret
`XDESK_APT_KEY`; its public half is `xdesk-archive.asc` (here and in the app).
