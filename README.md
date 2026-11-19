# win-MetalUI

A [Scoop](https://scoop.sh) bucket for the `metalui` command-line tool of
[MetalUI](https://github.com/mburger89/MetalUI), a GPU-accelerated UI framework for Swift.

## Install

```powershell
scoop bucket add win-metalui https://github.com/mburger89/win-MetalUI
scoop install win-metalui/metalui
```

Building the apps `metalui` creates needs a Swift toolchain: `winget install Swift.Toolchain`.

## Update and uninstall

```powershell
scoop update metalui
scoop uninstall metalui
```

## Bumping a release

The manifest `bucket/metalui.json` has `checkver` (latest GitHub release) and `autoupdate`
(release zip URL from `$version`, hash from the `.sha256` asset). With Scoop's tooling:

```powershell
.\bin\checkver.ps1 -App metalui -Update
```

or by hand: edit `version`, the `64bit` URL and `hash` to match the new release.
