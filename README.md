# RoMacShade Effects

RoMacShade is an independent graphics project with a versioned ReShade shader and preset library, plus an experimental iOS/iPadOS LiveContainer build.

## Downloads

- [iOS Preview v1](https://github.com/hesm4tt/RoMacShade-Effects/releases/tag/ios-preview-v1) includes the modified Roblox IPA, standalone arm64 dylib, effect pack, file index, and checksums.
- [iOS Effect Library v1](https://github.com/hesm4tt/RoMacShade-Effects/releases/tag/ios-effects-v1) provides the effect pack used by the in-app library restore action.
- [Install and LiveContainer instructions](INSTALL.md).

The iOS preview is experimental and tied to the Roblox build used to prepare it. The modified IPA is unsigned for ordinary iOS installation and must be re-signed by LiveContainer. Use the standalone dylib with a Roblox app copy in your own LiveContainer setup.

Apple does not document a supported end-user export workflow for turning a third-party App Store app into an IPA. Install Roblox with your Apple ID and use only an IPA obtained through a method you are authorized to use. The install guide explains how to use that copy with LiveContainer.

The app embeds the effect library for offline use. Its restore action downloads the versioned pack and validates its SHA-256 digest before installation. The library includes ReShade effects, helper includes, textures, 17 supplied Extravi presets, and two RoMacShade samples. Preset import and effect support depend on the host renderer and available depth data.

## Credits and rights

RoMacShade is not affiliated with or endorsed by Roblox. Roblox and its app remain separate works with their own rights and terms. The maintainer is responsible for obtaining permissions needed for the included package and assets.

Third-party sources retain their original notices. ReShadeFX, SPIRV-Cross, and SweetFX license texts are in [licenses](licenses/). qUINT credits Pascal Gilcher / Marty McFly; Extravi presets credit Extravi; other shaders retain their embedded author and license notices. No license for reusing RoMacShade code or branding is granted here unless a separate license is provided.
