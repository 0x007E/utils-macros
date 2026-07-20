[![Version: 1.0 Release](https://img.shields.io/badge/Version-1.0%20Release-green.svg)](https://github.com/0x007e/utils-macros) ![Build](https://github.com/0x007e/utils-macros/actions/workflows/release.yml/badge.svg) [![License GPLv3](https://img.shields.io/badge/License-GPLv3-lightgrey)](https://www.gnu.org/licenses/gpl-3.0.html)

# `Macro Utils`

[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/0x007E/utils-macros)

This utility can be used to manipulate preprocessor strings by injecting given data.

## File Structure

```
utils/
└── macros/
    └── stringify.c
```

> The library is completely patform independent and can be usesd across a wide range of c-compilers.

## Downloads

The library can be downloaded (`zip` or `tar`), cloned or used as submodule in a project.

| Type      | File               | Description              |
|:---------:|:------------------:|:-------------------------|
| Library   | [zip](https://github.com/0x007E/utils-macros/releases/latest/download/library.zip) / [tar](https://github.com/0x007E/utils-macros/releases/latest/download/library.tar.gz) | MACRO library that implements preprocessor string manipulation |

### Using with `git clone`

```sh
mkdir -p ./utils/
git clone https://github.com/0x007E/utils-macros.git ./utils
mv ./utils/utils-macros ./utils/macros
```

### Using as `git submodule`

```sh
git submodule add https://github.com/0x007E/utils-macros.git ./utils/macros
```

## Programming

```c
#include "../lib/utils/macros/stringify.h"

#define INJECTED_STRING test
#define MANIPULATED_STRING _STR(../hal/INJECTED_STRING/test/test.h)

#include MANIPULATED_STRING

int main(void)
{
    // Work with defined library
}
```

---

R. GAECHTER