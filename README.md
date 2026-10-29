<!-- THIS FILE IS AUTO GENERATED -->

# Tilia

A design language based on [Rosé Pine](https://rosepinetheme.com).

## Colours

There are two sets of colours, one for "dark mode" and one for "light mode".

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
| _Green_                | `#a7c090` | `#808c53` | Iris*          |
| _Cyan_                 | `#9ccfd8` | `#56949f` | Foam           |
| _Blue_                 | `#31748f` | `#286983` | Pine           |
| _Purple_               | `#c4a7e7` | `#907aa9` | Iris           |
|                        |           |           |                |

*The derivation of _Green_ is explained below.

### Usage

#### Foreground Colours

The _text_ colour should be used for most text and icons. If the text or icon is not active, or somehow deselected, _unimportant_ should be used instead.

_Disabled_ should be used for elements that cannot currently be interacted with.

#### Background Colours

The primary background should be used for the primary background of a window.

_Background_ will be used to refer to either the _primary_, _secondary_, or _tertiary background_ colour depending on context. If an element is placed on a background image, the _primary background_ colour should be used. However, if an element is placed on another element with the _primary_ or _secondary background_ colour, it should use the _secondary_ or _tertiary background_ respectively. Avoid nesting elements further.

If the foreground (text or icon) colour is one of the "rainbow" colours, and light mode is used, the background should use that colours associated background colour.

Popups, such as menus, tooltips, notifications, and launchers, should use the _tertiary background_ regardless of what they are placed on.

#### Highlight Colours

_Hover_ should be used as the background of an element that is hovered by the cursor, a caret, or the like.
_Selection_ should be used as the background of an element that is selected.
_Border_ should be used for borders and other lines that separate elements.

The _Hover_ colour in the table is only meant for the _primary background_.
On any _background_, the hover colour is obtained by interpolating 50 % of the way from the _background_ to _Selection_ in Oklab.

### Derivation

#### Green

Rosé Pine has no green colour, so _Green_ is derived in the [Oklab](https://bottosson.github.io/posts/oklab) colour space.
It has the same lightness as _Purple_ and its _a_ and _b_ components are those of the _primary background_ minus those of _Purple_.
This makes it roughly complementary to _Purple_.

#### Associated Background Colours

The background associated with a rainbow colour depends on which _background_ it is placed on.
In light mode it is obtained by interpolating 10 % of the way from the _background_ to the rainbow colour in Oklab.
In dark mode it is the _background_ itself.

#### Tints

Some elements, such as lines in a diff or search results, need a background that is coloured by a rainbow colour while still being readable.
Such a background is called a _tint_.
A tint is obtained by interpolating in Oklab from the _background_ to the rainbow colour, in the same way as the associated background colours.
Unlike associated background colours, tints are used in both light and dark mode.

| Strength | Interpolation | Used For                                                    |
| :------- | :-----------: | :---------------------------------------------------------- |
| Weak     | 20 %          | whole lines, such as added lines                            |
| Strong   | 40 %          | parts of lines, such as added words, and search results     |

Tints are not elements and do not count towards the nesting of backgrounds.
An element placed on a tint should treat the tint as its _background_.
For example, a token placed on a tinted line should have its associated background derived from the tint.

### Code

Tilia, as opposed to Rosé Pine, does not specify what colours to use for what kinds of tokens in code.
In this repository however, you will find the specification of the _Tilia Arrow_ theme (in light and dark variants).

## Elements

Sizing will be specified in _logical pixels_, henceforth referred to as "pixels".

### Background

See [the wallpaper read-me](wallpapers.md)

Depending on the application, the primary background may either have the _primary background_ colour or be one of the wallpapers in the `wallpapers` directory.
The wallpaper should match the set of colours chosen.

### Text

Do not put text directly on an image.
The text needs to be put inside a box.

### Boxes

A box is a rounded rectangle that contains other elements.

Boxes should have:
- A corner radius of 6 pixels.
- A background with the appropriate _background_ colour.
- A border with a thickness of 2 pixels.

The colour of the border can be determined from the below table.

| Colour    | If the box or its contained element...                                   |
| :-------: | :----------------------------------------------------------------------- |
| _Purple_  | is _selected_, _active_, or _focused_ (only if it can lose that state*). |
| _Red_     | represents an error or severe warning.                                   |
| _Orange_  | represents a warning of severity between _Yellow_ and _Red_.             |
| _Yellow_  | represents a warning.                                                    |
| _Cyan_    | 's state is "good", but not as "good" as _Green_.                        |
| _Green_   | 's state is "good".                                                      |
| _Border_  | does not have state.                                                     |

*A box that is dismissed when it loses focus, such as a launcher, counts as being able to lose that state.

_Orange_ and _Cyan_ should only be used if extra granularity is needed.

Boxes should have at least 6 pixels of space between them.
If the space is greater than 6 pixels it should be because the boxes are aligned differently.

Boxes should have at least 6 and 12 pixels of padding between their border and their contents in the vertical and horizontal directions respectively.

## Text

The font used for text should be the [JetBrains Mono Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono).
Where text needs to be aligned, such as in code and terminals, [JetBrains Mono Nerd Font _Mono_](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono) ought to be used.
Elsewhere the non-_Mono_ variant should be used, since its icons are allowed to be wider than other characters.
The variant with ligatures should be used unless there is a good reason not to.

### Sizes

Text should have a font size of 13 **pixels**. If larger text is desired, such as for headings, font sizes that are powers of two times 13 pixels should be used.

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
