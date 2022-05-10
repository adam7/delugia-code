![delugia image](/delugia_book.png)
# Cascadia Code + Nerd Fonts
Can we add Nerd Fonts to the [Cascadia Code](https://github.com/microsoft/cascadia-code) font using a GitHub Action?

Inspired by [Scott Hanselman](https://www.hanselman.com/blog/PatchingTheNewCascadiaCodeToIncludePowerlineGlyphsAndOtherNerdFontsForTheWindowsTerminal.aspx) and [Alistair Young](https://github.com/microsoft/cascadia-code/issues/10?WT.mc_id=-blog-scottha#issuecomment-532969414).

The answer, it turns out, is yes.

I wrote a [blog post with more details](https://admcpr.com/2019/10/07/automating-the-patching-of-cascadia-code-to-include-nerd-fonts/) about how this works.

[![Actions Status](https://github.com/adam7/delugia-code/workflows/Generate%20Fonts/badge.svg)](https://github.com/adam7/delugia-code/actions)

> ⚠ Cascadia is now part of Nerd Fonts' [prepatched font repository](https://github.com/ryanoasis/nerd-fonts#patched-fonts). You can grab it there, and it is almost what you find as Delugia font here. There are some small differences, see below.

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

These three font versions are generated from Cascadia Code:
* **Delugia Powerline** _Basic powerline glyphs, monospaced font_
* **Delugia Complete** _All Nerd Fonts glyphs, monospaced font_
* **Delugia Book** _All Nerd Fonts glyphs, proportional font (not recommended for coding/console)_

And the following two faces are generated from Cascadia Mono and don't have ligatures:
* **Delugia Mono Powerline** _Basic powerline glyphs, monospaced font_
* **Delugia Mono Complete** _All Nerd Fonts glyphs, monospaced font_

All of these are available in light, regular, and bold weights. Complemented by matching italic fonts.

### How is Delugia special?
Compared with other patched versions of Cascadia you will find
* Added symbols ``≢`` (0u2262), ``≣`` (0u2263), ``❯`` (0u276F), and ``⚡`` (0u26A1) used with some popular Powerline setups
* All added symbols centered on visual middle of the font (not a bit higher)
* Light and bold weight
* Italic faces

### How to use
You can download the patched fonts from the [Releases page](https://github.com/adam7/delugia-code/releases) of this
repo and install them as you would any other font. Once installed the font can be referenced as `Delugia *`.
So if, for example, you want to use it in Windows Terminal you should add this line to your profiles.json

`"fontFace" : "Delugia Complete",`

### Installation with [Chocolatey](https://chocolatey.org/install)
You can install your preferred version, or versions, of Delugia using the standard Chocolatey incantations.

* `choco install nerd-fonts-delugiamono-powerline`
* `choco install nerd-fonts-delugiabook`
* `choco install nerd-fonts-delugiapowerline`
* `choco install nerd-fonts-delugiacomplete`
* `choco install nerd-fonts-delugiamono-complete`

### Installation with [scoop.sh](https://scoop.sh)
_Scoop installation needs to be repaired after a naming change, I guess._

You can use [scoop.sh](https://scoop.sh) to install and update the font. At first install [scoop](https://github.com/lukesampson/scoop) and add extra bucket for [nerd-fonts](https://github.com/matthewjberger/scoop-nerd-fonts): 
1) `iwr -useb get.scoop.sh | iex`
2) `scoop bucket add nerd-fonts`
3) `scoop install sudo`
4) `sudo scoop install Delugia-Nerd-Font` or `sudo scoop install Delugia-Nerd-Font-Complete`

### Example for Delugia on the command line

![Delugia Powerline](/delugia_powerline.png)

### Help!
I know basically nothing about patching fonts so all contributions are 🦸‍ welcome. 

### Note
The naming changed a bit when we added the light and bold fonts.
To reduce the font name length the 'Nerd Font' has been dropped out of the (file) names.
The actual naming scheme changed to accommodate the new fonts and for your convenience we pack
fonts that one particular user might want to use together in a zip archive.
