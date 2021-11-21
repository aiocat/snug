<div align="center">

![Snug Logo](./images/snug.png)

# Snug

Most simple way to create config files.

</div>

## Example Syntax

```snug
# This is a comment! #
title "Hello World"
views 4826
is-public yes
owners ["User1" "User2"] # This is an array. #

(content # This is an object. #
text "Hello everyone, how are you?"
sha256-hash "0cfb86e2b382029d9c7ee32e98f855c1e870b688766da19caee32122894db03b"
color 12648430)

allow-edit no
```

## License

This project is distributed with [MIT](/LICENSE) license

<hr>

## Learn Snug

### Defining a Key

Snug has really easy way to declare a new key. Check the syntax below:

```snug
<key-name> <value-name>
```

Cool right? Snug also has a _flexible_ syntax. You can make a config like this:

```snug
key-one "Hello" key-two "hi." key-three 1337
```

Say goodbye to indentation syntax, semicolons and if you want to write worst syntax, new lines.

### Types

- `bool`: The boolean data type represents only one bit of information either yes or no.
  - **Example(s)**: `yes`, `no`
- `int`: The int (integer) data type represents number.
  - **Example(s)**: `420`, `1337`, `1_000_000` (1,000,000), `1_0_00_____0` (1,000)
- `float`: The float data type represents decimal real number.
  - **Example(s)**: `42.111`, `835.2`, `.62`, `1.`
- `string`: The string data type represents char set.
  - **Example(s)**: `"Hello, World!"`, `"Hayloft"`, `"Oh Ana"`
- `array`: The array data type is used to define multiple variables of the same or different type.
  - **Example(s)**: `[1 2 3 4]`, `[1 "Another Type" .3 yes]`
- `nil`: The nil (null, none) data type is used to define null value.
  - **Example(s)**: `nil`