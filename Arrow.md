# Tilia Arrow

## Tokens

Colours should be distributed according to the table below.

| Colour        | Token Kinds                                                | Examples                                   |
| :------------ | :--------------------------------------------------------- | :----------------------------------------- |
| _Text_        | miscellaneous tokens                                       | `foo`                                      |
| _Unimportant_ | operators*, brackets, documentation                        | `+`, `.`, `()`, `{}`, `/// documentation`  |
|               |                                                            |                                            |
| _Red_         | erroneous tokens                                           |                                            |
| _Orange_      | keywords, escape characters in strings, certain operators* | `struct`, `\n`                             |
| _Yellow_      | comments                                                   | `// commentary`                            |
| _Green_       | string and character literals                              | `"text"`, `'E'`                            |
| _Cyan_        | other literals                                             | `42`, `6.28`, `false`                      |
| _Blue_        | functions (including macros), URLs                         | `printf`, `println!`                       |
| _Purple_      | types                                                      | `String`, `u8`                             |

*Most operators should use the _Unimportant_ colour.
However, certain important/noteworthy operators should use the _Orange_ colour.
Examples include the try (`?`) operator in Rust.
If the operator can cause a control-flow break then it should generally use _Orange_.

Note that all foreground colours must be accompanied by their respective background colours in light mode.

Certain tokens should also be given certain other styling according to the table below:

| Style      | Token Kinds           | Examples                             |
| ---------- | --------------------- | ------------------------------------ |
| Bold       | bolded text, headings | `**text**`, `# text`                 |
| Italic     | italic text           | `_text_`                             |
| Underlined | underlined text, URLs | `<u>text</u>`, `https://example.org` |

### More examples

- XML/HTML tags
    Since they usually have some form of function, and since they aren't really "keywords",
    I'd go with _Blue_, but it's debatable.
- List markers and the like in e.g. Markdown
    They fill the same function as operators or other such punctuation, so _Unimportant_ it is.
- Attributes
    The surrounding punctuation (such as `#[]` or `@`) should be given the _Unimportant_ colour.
    However, the function/macro/keyword part of it should be highlighted as such.
- Labels
    Labels such as `'loop` in Rust, `error:` in C or `::continue::` in Lua can be sort of as values at compile time.
    They can be passed to keywords or other constructs to represent "values" (positions or lifetimes in the code).
    As such they should be highlighted as other miscellaneous literals with _Cyan_.

## File colours

Files and directories should also be coloured.
Each segment in a path should be coloured differently according to the table below.
In code it is likely to become messy if all paths are coloured so there it generally recommended to colour them as if they were normal strings.
However, in the output of commands such as `ls`, colouring paths can be informative.

> Note that whether the examples are valid may depend on the system.
> The descriptions in the second column have precedence over the examples.

| Colour        | File Kind                                             | Example(s)*             |
| :------------ | :---------------------------------------------------- | :---------------------- |
| _Text_        | "normal" files                                        | `foo.txt`               |
| _Unimportant_ | path separators                                       | `/`, `\`                |
|               |                                                       |                         |
| _Red_         | broken symbolic links, other likewise erroneous files |                         |
| _Orange_      | devices                                               | `/dev/sda`, `/dev/null` |
| _Yellow_      |                                                       |                         |
| _Green_       | symbolic links, mount points                          | `/bin/sh`, `/mnt`       |
| _Cyan_        |                                                       |                         |
| _Blue_        | executables                                           | `/usr/bin/bash`         |
| _Purple_      | directories                                           | `~/Downloads`, `~`      |

*Only the last segment in an example path should necessarily have the given colour.

## Version control

"Concepts" in version control should be coloured according to the table below.

| Colour    | Concept                                                   |
| :-------- | :-------------------------------------------------------- |
| _Red_     | deletion, removal                                         |
| _Orange_  | modification, simultaneous addition and removal, renaming |
| _Green_   | addition                                                  |

> TODO: Background colours here.
