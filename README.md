# biglinux-meta-audio-config

**Empty transitional package.** It installs nothing and can be uninstalled.

The old `biglinux-meta-audio-config` (1.0.1, 2022) pulled audio codecs and
installed realtime limits for the `audio` group, udev rules and a
`big-audio-config` boot service. That service forced `vm.swappiness=10` and
`vm.vfs_cache_pressure=100` on every boot, overriding the current BigLinux
memory tuning, so the package was dropped from the ISOs.

A package that simply disappears from the repository stays installed forever
on systems that are never reinstalled. Upgrading to this empty version removes
the old files (the service is disabled first); after that, remove it with:

```bash
sudo pacman -R biglinux-meta-audio-config
```

## License

GPL-3.0-or-later. See [LICENSE](LICENSE).
