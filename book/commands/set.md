---
title: set
version: 0.70.0
dataframe: |
  Sets value where given mask is true
usage: |
  Sets value where given mask is true
---

# <code>{{ $frontmatter.title }}</code> for dataframe

<div class='command-title'>{{ $frontmatter.dataframe }}</div>

## Signature

```> set (value) --mask```

## Parameters

 -  `value`: value to be inserted in series
 -  `--mask {any}`: mask indicating insertions

## Examples

Shifts the values by a given period
```shell
> let s = ([1 2 2 3 3] | into df | shift 2);
    let mask = ($s | is-null);
    $s | set 0 --mask $mask
```