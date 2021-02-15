# Cascadia Code + Nerd Fonts 
Can we add Nerd Fonts to the [Cascadia Code](https://github.com/microsoft/cascadia-code) font using a GitHub Action?

Inspired by [Scott Hanselman](https://www.hanselman.com/blog/PatchingTheNewCascadiaCodeToIncludePowerlineGlyphsAndOtherNerdFontsForTheWindowsTerminal.aspx) and [Alistair Young](https://github.com/microsoft/cascadia-code/issues/10?WT.mc_id=-blog-scottha#issuecomment-532969414).

The answer, it turns out, is yes.

I wrote a [blog post with more details](https://admcpr.com/2019/10/07/automating-the-patching-of-cascadia-code-to-include-nerd-fonts/) about how this works.

[![Actions Status](https://github.com/adam7/delugia-code/workflows/Generate%20Fonts/badge.svg)](https://github.com/adam7/delugia-code/actions)

> ⚠ Cascadia now [bundles Powerline symbols](https://github.com/microsoft/cascadia-code/issues/10) so you almost definitely don't need to use this. Just grab the PL version from the latest [Cascadia release](https://github.com/microsoft/cascadia-code/releases). 

> ⚠ Cascadia is now also part of Nerd Fonts' [prepatched font repository](https://github.com/ryanoasis/nerd-fonts#patched-fonts). You can grab it there, and it is almost what you find as Delugia font here. There are some small differences, see below.

### What is Nerd Fonts anyway?
[Nerd Fonts](https://www.nerdfonts.com) takes popular programming fonts and adds a bunch of Glyphs. They include all the absolutely [indispensable symbols](https://github.com/ryanoasis/nerd-fonts/wiki/Glyph-Sets-and-Code-Points) all nerds need in their favorite fonts.
Go to their [repository](https://github.com/ryanoasis/nerd-fonts) or have a look at the [overview](https://www.nerdfonts.com/#cheat-sheet).

Typically they come in two flavours:
* Powerline (adds the symbols needed to have a basic [Powerline](https://github.com/powerline) and some more.)
* Complete (adds even more Powerline symbols and all other symbols Nerd Fonts has collected.)

_Powerline_ includes these symbols:
* Powerline Symbols
* [Seti-UI](https://atom.io/themes/seti-ui#current_icons)
* [Devicons](http://vorillaz.github.io/devicons/)

_Complete_ includes these symbols additionally:
* [Powerline Extra Symbols](https://github.com/ryanoasis/powerline-extra-symbols)
* [Pomicons](https://github.com/gabrielelana/pomicons)
* [Font Awesome](https://github.com/FortAwesome/Font-Awesome) and [Extension](https://github.com/AndreLZGava/font-awesome-extension)
* [Power Symbols](https://unicodepowersymbol.com/)
* [Material Design Icons](https://github.com/Templarian/MaterialDesign)
* [Font Logos](https://github.com/Lukas-W/font-logos)
* [Octicons](https://github.com/github/octicons)

### Which font faces are available
Cascadia now bundles a version without ligatures, called Cascadia Mono, in addition to Cascadia Code which has ligatures.

These three faces are generated from Cascadia Code:
* **Delugia Nerd Font Powerline** _Basic glyphs, monospaced font_
* **Delugia Nerd Font Complete** _All Nerd Fonts glyphs, monospaced font_
* **Delugia Nerd Font Book** _All Nerd Fonts glyphs, proportional font (not recommended for coding/console)_

And the following two faces are generated from Cascadia Mono and don't have ligatures:
* **Delugia Mono Nerd Font Powerline** _Basic glyphs, monospaced font_
* **Delugia Mono Nerd Font Complete** _All Nerd Fonts glyphs, monospaced font_

### How is Delugia special?
Compared with other patched versions of Cascadia you will find
* Added symbols ``≢`` (0u2262), ``≣`` (0u2263), ``❯`` (0u276F), and ``⚡`` (0u26A1) used with some popular Powerline setups

### How to use
You can download the patched font from the [Releases page](https://github.com/adam7/delugia-code/releases) of this repo and install them as you would any other font. Once installed the font can be referenced as `Delugia Nerd Font`. So if, for example, you want to use it in Windows Terminal you should add this line to your profiles.json

`"fontFace" : "Delugia Nerd Font",`

### Installation with [scoop.sh](https://scoop.sh)
You can use [scoop.sh](https://scoop.sh) to install and update the font. At first install [scoop](https://github.com/lukesampson/scoop) and add extra bucket for [nerd-fonts](https://github.com/matthewjberger/scoop-nerd-fonts): 
1) `iwr -useb get.scoop.sh | iex`
2) `scoop bucket add nerd-fonts`
3) `scoop install sudo`
4) `sudo scoop install Delugia-Nerd-Font` or `sudo scoop install Delugia-Nerd-Font-Complete`

### Help!
I know basically nothing about patching fonts so all contributions are 🦸‍ welcome. 
