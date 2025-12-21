# Tilia Arrow

## Tokens

Colours should be distributed according to the table bellow.

| Colour        | Token Kind                                                 | Example(s)            |
| :------------ | :--------------------------------------------------------- | :-------------------- |
| _Text_        | miscellaneous tokens                                       | `foo`                 |
| _Unimportant_ | operators, brackets                                        | `+`, `.`, `()`, `{}`  |
|               |                                                            |                       |
| _Red_         |                                                            |                       |
| _Orange_      | keywords, escape characters in strings, certain operators* | `struct`, `\n`        |
| _Yellow_      | comments                                                   | `// commentary`       |
| _Green_       | strings                                                    | `"text"`, `'E'`       |
| _Cyan_        | functions (including macros)                               | `printf`, `println!`  |
| _Blue_        | other literals                                             | `42`, `6.28`, `false` |
| _Purple_      | types                                                      | `String`              |

*Most operators should use the _Unimportant_ colour.
However, certain important/noteworthy operators should use the _Orange_ colour.
Examples include the try (`?`) operator in Rust.
If the operator can cause a control-flow break then it should generally use _Orange_.

Note that all foreground colours must be accompanied by their respective background colours in light mode.

## File colours

Files and directories should also be coloured.
Each segment in a path should be coloured differently according to the table bellow.
In code it is likely to become messy if all paths are coloured so there it generally recommended to colour them as if they were normal strings.
However, in the output of commands such as `ls`, colouring paths can be informative.

> Note that whether the examples are valid may depend on the system.
> The descriptions in the second column have precedence over the examples.

| Colour        | File Kind                                            | Example(s)*             |
| :------------ | :--------------------------------------------------- | :---------------------- |
| _Text_        | "normal" files                                       | `foo.txt`               |
| _Unimportant_ | path separators                                      | `/`, `\`                |
|               |                                                      |                         |
| _Red_         | broken symbolic links, other likewise erroneous file |                         |
| _Orange_      | symbolic links, mount points                         | `/bin/sh`, `/mnt`       |
| _Yellow_      | devices                                              | `/dev/sda`, `/dev/null` |
| _Green_       |                                                      |                         |
| _Cyan_        | executables                                          | `/bin/bash`             |
| _Blue_        | directories                                          | `~/Downloads`, `~`      |
| _Purple_      |                                                      |                         |

*Only the last segment in an example path should necessarily have the given colour.

## Version control

"Concepts" in version control should be coloured according to the table bellow.

| Colour    | Concept                                                   |
| :-------- | :-------------------------------------------------------- |
| _Red_     | deletion, removal                                         |
| _Orange_  | modification, simultaneous removal and deletion, renaming |
| _Green_   | addition                                                  |
