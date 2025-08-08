# OPTO Logic Device Tree Overlays

This repository contains device tree overlays for the OPTO Logic display
modules, specifically designed for the Verdin AM62 and iMX8MP Toradex platforms.

These device tree overlays follow the structure provided by Toradex's overlays:
 - https://git.toradex.com/cgit/device-tree-overlays.git/

## Obtaining the sources

You may clone this git repository on the branch corresponding to your Linux
kernel architecture and version. For example:
 - `linux-toradex-ti-6.6.y`
 - `linux-toradex-nxp-6.6.y`

## Supported Hardware

We currently support the following Toradex SoMs:
 - `verdin-am62`
 - `verdin-imx8mp`

These may be combined with the following OPTO Logic displays:
 - `7-inch` with capacitive touchscreen

## Compiling with Yocto

This repository is intended to be used with the Yocto build system. The recipes
`device-tree-overlays-optologic*.bb` from the
[meta-optologic](https://github.com/optologic/meta-optologic) layer contains the
necessary instructions to compile the overlays when building images.

## Compiling with TorizonCore Builder

If you plan on integrating these overlays into a TorizonOS image, you can use
our Torizon [configurations
repository](https://github.com/optologic/torizon-optologic).
