# OPTO Logic Device Tree Overlays

This repository contains device tree overlays for the OPTO Logic display
modules, specifically designed for the Verdin AM62 and iMX8MP Toradex platforms.

These device tree overlays follow the structure provided by Toradex's overlays:
 - https://git.toradex.com/cgit/device-tree-overlays.git/

## Obtaining the sources

You may clone this git repository on the branch corresponding to your Linux
kernel architecture and version. For example:
 - [`linux-toradex-ti-6.6.y`](https://github.com/optologic/device-tree-overlays-optologic/tree/linux-toradex-ti-6.6.y)
 - [`linux-toradex-nxp-6.6.y`](https://github.com/optologic/device-tree-overlays-optologic/tree/linux-toradex-nxp-6.6.y)

## Supported Hardware

We currently support the following Toradex SoMs:
 - `verdin-am62`
 - `verdin-imx8mp`

These may be combined with the following OPTO Logic displays:
 - `5-inch` with capacitive touchscreen
 - `7-inch` with capacitive touchscreen
 - `10-inch` with capacitive touchscreen

## Driver support

Make that your Linux configuration enables, or includes as modules the following
touchscreen drivers:

- `ilitek_ts_i2c` for the 5-inch display
- `ili210x` for the 7-inch and 10-inch displays

## Compiling with Yocto

This repository is intended to be used with the Yocto build system. The recipes
`device-tree-overlays-optologic*.bb` from the
[meta-optologic](https://github.com/optologic/meta-optologic) layer contains the
necessary instructions to compile the overlays when building images.

## Compiling with TorizonCore Builder

If you plan on integrating these overlays into a TorizonOS image, you can use
our Torizon [configurations
repository](https://github.com/optologic/torizon-optologic).

## Contribute or Contact

Please submit any patches and bug reports about this repository to the maintainer:

Maintainer: OPTO Logic Technology S.A. <support@optologic.ch>
