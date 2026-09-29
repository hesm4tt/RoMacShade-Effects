# RoMacShade iOS Preview

This preview provides an arm64 iOS/iPadOS shader overlay build, a standalone LiveContainer tweak, and the matching effects library. It was built on 2026-09-29. The Roblox integration is experimental and tied to the supplied Roblox app build; a Roblox update can make it incompatible.

## Release files

- `RoMacShade-Roblox.ipa` is the prebuilt modified app package. It embeds RoMacShade and does not include MaxeysVisuals. It is unsigned for normal iOS installation and must be re-signed by LiveContainer.
- `RoMacShade.dylib` is the standalone arm64 tweak for use with your own Roblox app copy in LiveContainer.
- `RoMacShade-effects.rmpack` and `RoMacShade-effects.json` are the shader, texture, and preset library. The app also embeds this library for offline use.
- `third-party-licenses.zip` contains applicable third-party license texts. Individual shader and preset files retain their own notices.
- `SHA256SUMS` lists SHA-256 digests for the release files.

Verify downloaded files from the folder containing the release assets:

    shasum -a 256 -c SHA256SUMS

## Use the prebuilt IPA in LiveContainer

1. Download `RoMacShade-Roblox.ipa` from this release and import it into LiveContainer.
2. Long-press the imported app card, open Settings, and run Force Sign.
3. Launch the app. Open a 3D experience and tap the floating R control to open the RoMacShade menu.

LiveContainer may show a signature error on first launch. In the app settings, run Force Sign again. The prebuilt IPA has not been tested on every iOS/LiveContainer version.

## Use your own Roblox IPA

1. Install Roblox from the App Store using your Apple ID. Apple does not document a supported end-user workflow for exporting a third-party App Store app as an IPA. Use only a copy obtained through a method you are authorized to use; do not share Apple ID credentials.
2. Import that IPA into LiveContainer.
3. In LiveContainer's Tweaks area, create or choose a tweak folder for Roblox and add `RoMacShade.dylib`.
4. Use LiveContainer's Sign action for the tweak. In Roblox's app-specific Settings, choose that tweak folder.
5. Run Force Sign for the app if LiveContainer requests it, then launch Roblox.

This uses LiveContainer's per-app tweak loading, so you do not need to edit the App Store IPA on disk. LiveContainer documents app-specific tweak folders and signing in its [App Settings guide](https://livecontainer.github.io/docs/guides/app-settings) and [installation and signing FAQ](https://livecontainer.github.io/docs/faq/installing-livecontainer).

## Effect and preset notes

The effect library contains ReShade shaders, helper includes, textures, 17 supplied Extravi presets, and two RoMacShade samples. Original author notices are retained in the library. The overlay supports effect toggles, ReShade INI import, and preset selection.

Some ReShade effects require depth data or APIs that a particular Roblox renderer/device may not expose. Unsupported effects may fail to compile or produce no visible result.

## Credits and terms

RoMacShade uses ReShadeFX and SPIRV-Cross; their license texts are in `third-party-licenses.zip` and the repository's `licenses/` folder. SweetFX-derived sources retain the MIT notice. qUINT credits Pascal Gilcher / Marty McFly. Extravi presets credit Extravi. Other included effects retain their embedded author and license notices. The app and Roblox remain separate works with their own rights and terms.