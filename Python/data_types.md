# Data Types

- [Data Types](#data-types)
  - [Text Type: `str`](#text-type-str)
  - [Numeric Types: `int`, `float`, `complex`](#numeric-types-int-float-complex)
  - [Sequence Types: `list`, `tuple`, `range`](#sequence-types-list-tuple-range)
    - [List](#list)
      - [Transform a nested list into a simple list](#transform-a-nested-list-into-a-simple-list)
  - [Mapping Type: `dict`](#mapping-type-dict)
  - [Set Types: `set`, `frozenset`](#set-types-set-frozenset)
  - [Boolean Type: `bool`](#boolean-type-bool)
  - [Binary Types: `bytes`, `bytearray`, `memoryview`](#binary-types-bytes-bytearray-memoryview)

## Text Type: `str`

## Numeric Types: `int`, `float`, `complex`

## Sequence Types: `list`, `tuple`, `range`

### List

#### Transform a nested list into a simple list

```python
from functools import reduce

nested_list = [[1], [2], [3, 5, 6], [4, 3, 12, 33]]

simple_list = reduce(lambda x,y: x+y, nested_list)
```

## Mapping Type: `dict`

## Set Types: `set`, `frozenset`

## Boolean Type: `bool`

## Binary Types: `bytes`, `bytearray`, `memoryview`
