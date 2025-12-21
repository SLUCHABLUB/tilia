# Tilia

A UI theme based on [Rosé Pine](https://rosepinetheme.com).

## Colours

There are two sets of colours, one for "light mode" and one for "dark mode".
Which one is considered default depends of the application being themed.

The light colours is based on the [Rosé Pine Dawn colour scheme](https://rosepinetheme.com/palette)
and the dark colours are based on the [main Rosé Pine colour scheme](https://rosepinetheme.com/palette).

The below table shows the colours used in the theme.
Each colour is given a name with which it will be referred to by later.
The colours are defined using sRGB hex-codes.
The last column lists the Rosé Pine colour which the colour is based on.

| Name                   | Light     | Dark      | Derived From    |
| :--------------------: | :-------: | :-------: | :-------------: |
| _Border_               | `#cecacd` | `#524f67` | Highlight High  |
| _Text_                 | `#575279` | `#e0def4` | Text            |
| _Primary Background_   | `#faf4ed` | `#191724` | Base            |
| _Secondary Background_ | `#faf4ed` | `#191724` | Surface         |
| _Tertiary Background_  | `#faf4ed` | `#191724` | Overlay         |
|                        |           |           |                 |
| _Red_                  | `#b4637a` | `#eb6f92` | Love            |
| _Orange_               | `#d7827e` | `#ebbcba` | Rose            |
| _Yellow_               | `#ea9d34` | `#f6c177` | Gold            |
| _Green_                | `#818C53` | `#a7bf90` | Iris (inverted) |
| _Cyan_                 | `#56949f` | `#9ccfd8` | Foam            |
| _Blue_                 | `#286983` | `#31748f` | Pine            |
| _Purple_               | `#907aa9` | `#c4a7e7` | Iris            |

_Background_ will be used to refer to either the _primary_ _secondary_ or _tertiary background_ colour depending on context.
If an element is placed on a background image, the _primary background_ colour should be used.
However, if an element is placed on an another element with the _primary_ or _secondary background_ colour, it should use the _secondary_ or _tertiary background_ respectively.
Avoid nesting elements further.

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
