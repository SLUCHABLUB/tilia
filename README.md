# Tilia

A UI theme based on [Rosé Pine](https://rosepinetheme.com).

## Colours

There are two sets of colours, one for "dark mode" and one for "light mode".
Which one is considered default depends of the application being themed.

The dark colours are based on the [main Rosé Pine colour scheme](https://rosepinetheme.com/palette)
and the light colours are based on the [Rosé Pine Dawn colour scheme](https://rosepinetheme.com/palette).

The below table shows the colours used in the theme.
Each colour is given a name with which it will be referred to by later.
The colours are defined using sRGB hex-codes.
The last column lists the Rosé Pine colour which the colour is based on.

| Colour                 | Dark      | Light     | Derived from   |
| :--------------------: | :-------: | :-------: | :------------: |
| _Primary Background_   | `#191724` | `#faf4ed` | Base           |
| _Secondary Background_ | `#1f1d2e` | `#fffaf3` | Surface        |
| _Tertiary Background_  | `#26233a` | `#f2e9e1` | Overlay        |
|                        |           |           |                |
| _Hover_                | `#21202e` | `#f4ede8` | Highlight Low  |
| _Selection_            | `#403d52` | `#dfdad9` | Highlight Med  |
| _Border_               | `#524f67` | `#cecacd` | Highlight High |
|                        |           |           |                |
| _Disabled_             | `#6e6a86` | `#9893a5` | Muted          |
| _Unimportant_          | `#908caa` | `#797593` | Subtle         |
| _Text_                 | `#e0def4` | `#575279` | Text           |
|                        |           |           |                |
| _Red_                  | `#eb6f92` | `#b4637a` | Love           |
| _Orange_               | `#ebbcba` | `#d7827e` | Rose           |
| _Yellow_               | `#f6c177` | `#ea9d34` | Gold           |
| _Green_                | `#a7bf90` | `#818c53` | Iris*          |
| _Cyan_                 | `#9ccfd8` | `#56949f` | Foam           |
| _Blue_                 | `#31748f` | `#286983` | Pine           |
| _Purple_               | `#c4a7e7` | `#907aa9` | Iris           |

_Background_ will be used to refer to either the _primary_ _secondary_ or _tertiary background_ colour depending on context.
If an element is placed on a background image, the _primary background_ colour should be used.
However, if an element is placed on an another element with the _primary_ or _secondary background_ colour, it should use the _secondary_ or _tertiary background_ respectively.
Avoid nesting elements further.

The derivation of _Green_ is explained below.

### Usage

> TODO

### Derivation

> TODO

### Code

Tilia, as opposed to Rosé Pine, does not specify what colours to use for what kinds of tokens in code.
In this repository however, you will find the specification of the _Tilia Arrow_ theme (in light and dark variants).

## Elements

Sizing will be specified in _logical pixels_, henceforth referred to as "pixels".
For reference, this theme was created on a laptop with ca. 100 pixels per inch.

### Background

See [the wallper read-me](wallpapers/README.md)

Depending on the application, the primary background may either have the _primary background_ colour or be one of the wallpapers in the `wallpapers` directory.
The wallpaper should match set of colours chosen.

### Text

Do not put text directly on a wallpaper.
The text needs to be put inside a box.

### Boxes

A box is a rounded rectangle that contains other elements.

Boxes should have:
- A radius of 6 pixels.
- A background with the _background_ colour.
- A border with a thickness of 2 pixels.

The colour of the border can be determined from the below table.

| Colour    | If the box or it's contained element...                                         |
| :-------: | :------------------------------------------------------------------------------ |
| _Purple_  | is _selected_ or _active_ (only if it can be _deselected_ or _deactivated_).    |
| _Red_     | represents an error or severe warning.                                          |
| _Orange_  | represents a warning of severity between _Yellow_ and _Red_.                    |
| _Yellow_  | represents a warning.                                                           |
| _Cyan_    | 's state is "good", but not as "good" as _Green_.                               |
| _Green_   | 's state is "good".                                                             |
| _Border_  | does not have state.                                                            |

_Orange_ and _Cyan_ should only be used if extra granularity is needed.

Boxes should have at least 6 pixels of space between them.
If the space is greater than 6 pixels it should be because the boxes are aligned differently.

## Text

The font used for text should be the [JetBrains Mono Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono).
Where a monospace font is needed, such as in text editors, [JetBrains Mono Nerd Font _Mono_](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono) ought to be used.
The variant with ligatures should be used unless there is a good reason not to.

TODO: specify text sizes

## Recommendations

It is recommended that interfaces:

- Automatically switch between the light and dark colours at sunrise and sundown.
- Provide a way to switch between light and dark colours.
- Pick a random wallpaper matching the set of colours.
- Provide a way to switch between wallpapers.

## Legal

This specification is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0).
Any code in this repository is licensed under the [GNU General Public License (version 3 or later)](https://www.gnu.org/licenses/gpl-3.0.html).

This theme is in no way affiliated with the [Rosé Pine organisation](https://github.com/rose-pine).
It utilises similar colours as the [Rosé Pine theme](https://rosepinetheme.com) which is licensed under the MIT license.
