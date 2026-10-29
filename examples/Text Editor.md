# Text Editor

How things should be highlighted in a typical text editor.

## Line numbers

These usually sit on a panel to the left of the main text area. This are should naturally have the secondary background colour. The foreground should be _unimportant_ for most of the numbers since they don't need to draw attention. The number on the carets' line(s) should however have the normal text colour such that it stands out.

## Caret Line

All lines that have carets on them should have the _Hover_ colour. This is because a caret is the analogue of the cursor to the line is practically "hovered" by the caret.

## Selection

Selected text should naturally have the _Selection_ colour as it's background and the foreground should remain _Text_.

## Brackets

When the caret is placed on a bracket the matching bracket should naturally be highlighted. It would make sense to use the _Hover_ colour but since the carets line is already using that, the background for the pair of brackets should use _Selection_.

## Indentation Guides

The most appropriate colour would be _Border_ since they segment parts of the text area.

## Arrow Specifics

### Searching

> TODO: Figure out a way to do backgrounds as with diff.

Search results should be highlighted yellow to be accentuated.
