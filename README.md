# XDesk apt repository

The packages XDesk's built-in Ubuntu 26.04 gets from XDesk: `xdesk-core` (what the system needs to run inside the
XDesk app) and, later, `xdesk-mesa` (Ubuntu's Mesa rebuilt with Adreno's KGSL). Sources and build scripts:
[n2ray/xdesk](https://github.com/n2ray/xdesk), `linux/`.

```
Types: deb
URIs: https://n2ray.github.io/xdesk-apt
Suites: resolute
Components: main
Signed-By: /usr/share/keyrings/xdesk-archive.asc
```

The app installs the version of `xdesk-core` it needs on its own, so a release here reaches every installed system:
it is published only by hand (Actions → Publish). `xdesk-mesa` is checked every day (Actions → xdesk-mesa): a new
Mesa from Ubuntu is rebuilt on its own and an issue says so; it reaches phones once it is tested and published
(this repository is pinned above Ubuntu's, so until then they keep the published one). The signing key lives only in this repository's Actions secret
`XDESK_APT_KEY`; its public half is `xdesk-archive.asc` (here and in the app).
