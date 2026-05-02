# void-scripts

A small collection of scripts I use on Void Linux systems.

## Scripts

- `vkinstall`: installs or updates a manually built kernel for systemd-boot. It copies the kernel image and config to `/boot`, generates an initramfs, creates a loader entry, and can update `/usr/src/linux` to point at the source tree.
- `vkpurge`: custom replacement for Void Linux's `vkpurge`, intended for cleaning up manually installed kernels that are not managed by xbps. It can list or remove detected kernels, supports dry-run mode, and will not remove the currently running kernel.

## Related Tools

- [`xdeb-ng`](https://github.com/Gur0v/xdeb-ng): my Rust rewrite of `xdeb` for converting Debian `.deb` packages into Void Linux `.xbps` packages. The project is called `xdeb-ng`, but the binary is still `xdeb`. It keeps the original workflow while adding clearer subcommands, dry runs, better inspection, libc-aware dependency resolution, stricter safety checks, and safer conflict handling.
