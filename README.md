# Tilia

> A [Rosé Pine](https://rosepinetheme.com) based theme.

## Colours

There are two sets of colours, one for "light mode" and one for "dark mode".
Which one is considered default depends of the application being themed.

The light colours is based on the [Rosé Pine Dawn colour scheme](https://rosepinetheme.com/palette)
and the dark colours are based on the [main Rosé Pine colour scheme](https://rosepinetheme.com/palette).

The below table shows the colours used in the theme.
Each colour is given a name with which it will be referred to by later.
The colours are defined using sRGB hex-codes.
The last column lists the Rosé Pine colour which the colour is based on.

| Name                   | Light     | Dark      | Derived From   |
| :--------------------: | :-------: | :-------: | :------------: |
| *Border*               | `#cecacd` | `#524f67` | Highlight High |
| *Text*                 | `#575279` | `#e0def4` | Text           |
| *Primary Background*   | `#faf4ed` | `#191724` | Base           |
| *Secondary Background* | `#faf4ed` | `#191724` | Base           |
| *Tertiary Background*  | `#faf4ed` | `#191724` | Base           |
|                        |           |           |                |
| *Accent*               | `#907aa9` | `#c4a7e7` | Iris           |
| *Good*                 | `#286983` | `#31748f` | Pine           |
| *OK*                   | `#56949f` | `#9ccfd8` | Foam           |
| *Warning*              | `#ea9d34` | `#f6c177` | Gold           |
| *Bad*                  | `#b4637a` | `#eb6f92` | Love           |

*Background* will be used to refer to either the *primary* *secondary* or *tertiary background* colour depending on context. If an element is placed on a background image, the *primary background* colour should be used. However, if an element is placed on an another element with the *primary* or *secondary background* colour, it should use the *secondary* or *tertiary background* respectively. Avoid nesting elements further.

## Elements

Sizing will be specified in *logical pixels*, henceforth referred to as "pixels".
For reference, this theme was created on a laptop with a 

### Background

> This theme was designed using wallpapers from Rosé Pine.
> These are however not (yet) licensed and can therefore not be distributed here.

Depending on the application, the primary background may either have the *primary background* colour or be one of the wallpapers in the `wallpapers` directory.
The wallpaper should match set of colours chosen.

### Text

Do not put text directly on a wallpaper.
The text needs to be put inside a box.

### Boxes

A box is a rounded rectangle that contains other elements.

Boxes should have:
- A radius of 6 pixels.
- A background with the *background* colour.
- A border with a thickness of 2 pixels.

The colour of the border can be determined from the below table.

| Colour    | If the box or it's contained element...                                         |
| :-------: | :------------------------------------------------------------------------------ |
| *Iris*    | is "selected" or "active", but only if it can be "deselected" or "deactivated". |
| *Bad*     | Represents an error or severe warning.                                          |
| *Warning* | Represents a warning.                                                           |
| *OK*      | 's state is "good", but not as "good" as for the *good* colour.                 |
| *Good*    | 's state is "good".                                                             |
| *Border*  | Otherwise.                                                                      |

Boxes should have at least 6 pixels of space between them.
If the space is greater than 6 pixels it should be because the boxes are aligned differently.

## Text

The font used for text should be the [JetBrains Mono Nerd Font Mono](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono).

TODO: specify text sizes

## Recommendations

It is recommended that interfaces:

- Automatically switch between the light and dark colours at sunrise and sundown.
- Provide a way to switch between light and dark colours.
- Pick a random wallpaper matching the set of colours.
- Provide a way to switch between wallpapers.

## Legal

This specification is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0)

This theme is in no way affiliated with the [Rosé Pine](https://github.com/rose-pine) organisation.
It utilises similar colours as the Rosé Pine theme [which seems to be licensed under the MIT license](https://github.com/rose-pine/rose-pine-theme/blob/e9388ed927c91d0f47726c410c3bb7964199dc48/license).
