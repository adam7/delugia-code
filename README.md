# Cascadia Code + Nerd Fonts 
Can we add Nerd Fonts to the [Cascadia Code](https://github.com/microsoft/cascadia-code) font using a GitHub Action?

Inspired by [Scott Hanselman](https://www.hanselman.com/blog/PatchingTheNewCascadiaCodeToIncludePowerlineGlyphsAndOtherNerdFontsForTheWindowsTerminal.aspx) and [Alistair Young](https://github.com/microsoft/cascadia-code/issues/10?WT.mc_id=-blog-scottha#issuecomment-532969414).

The answer, it turns out, is yes.

I wrote a [blog post with more details](https://admcpr.com/2019/10/07/automating-the-patching-of-cascadia-code-to-include-nerd-fonts/) about how this works.

[![Actions Status](https://github.com/adam7/delugia-code/workflows/Generate%20Fonts/badge.svg)](https://github.com/adam7/delugia-code/actions)

### How to use
You can download the patched font from the [Releases page](https://github.com/adam7/delugia-code/releases) of this repo and install them as you would any other font. Once installed the font can be referenced as `Delugia Nerd Font`. So if, for example, you want to use it in Windows Terminal you should add this line to your profiles.json

`"fontFace" : "Delugia Nerd Font",`

### Help!
I know basically nothing about patching fonts so all contributions are 🦸‍ welcome. 
