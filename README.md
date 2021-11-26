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

- [Libraries](https://gitlab.com/aiocat/snug#libraries)
- [Defining a Key](https://gitlab.com/aiocat/snug#defining-a-key)
- [Types](https://gitlab.com/aiocat/snug#types)
- [Objects](https://gitlab.com/aiocat/snug#objects)
- [Arrays](https://gitlab.com/aiocat/snug#arrays)

### Libraries

- [**JavaScript**: snug.js](https://gitlab.com/snuglibs/snug.js)
- [**Python3**: snugthon](https://gitlab.com/snuglibs/snugthon)

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
  - **Example(s)**: `420`, `1337`, `1_000_000` (1,000,000), `1_0_00_____0` (10,000)
- `float`: The float data type represents decimal real number.
  - **Example(s)**: `42.111`, `835.2`, `.62`, `1.`
- `string`: The string data type represents char set.
  - **Example(s)**: `"Hello, World!"`, `"Hayloft"`, `"Oh Ana"`
- `array`: The array data type is used to define multiple variables of the same or different type.
  - **Example(s)**: `[1 2 3 4]`, `[1 "Another Type" .3 yes]`
- `nil`: The nil (null, none) data type is used to define null value.
  - **Example(s)**: `nil`

### Objects

Actually, objects can resemble **Common Lisp** to you. Check the syntax below:

```snug
(<object-name> # ... # )
```

Object literals contains key/value pairs. Value must be valid snug type. An example:

```snug
(info title "Hello World" views 5921 tags ["C++" "Programming"])
```

#### Anonymous Objects

Anonymous objects are mostly used for adding object to the array.

```snug
(? # ... #)
```

Check the example below:

```snug
users [
    (? name "bob" id 0 age 21) # First anonymous object #
    (? name "aiocat" id 1 age 16) # Second anonymous object #
    (? name "john" id 2 age 19) # Last anonymous object #
]
```

### Arrays

_The array data type is used to define multiple variables of the same or different type._

Array syntax for snug is:

```snug
<key> [<value 1> <value 2> # ... #]
```

Array elements are seperated with spaces. Check the example below:

```snug
favorite-numbers [2 4 13 42]
```

... and you can use different types in same array:

```snug
collected-datas ["Hello" 1 4.3 258_23 yes nil]
```
