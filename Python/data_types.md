
# Data Types

## Text Type: `str`

## Numeric Types: `int`, `float`, `complex`

## Sequence Types: `list`, `tuple`, `range`

### List

#### Transform a nested list into a simple list

`from functools import reduce
nested_list = [[1], [2], [3, 5, 6], [4, 3, 12, 33]]
simple_list = reduce(lambda x,y: x+y, nested_list)`

## Mapping Type: `dict`

## Set Types: `set`, `frozenset`

## Boolean Type: `bool`

## Binary Types: `bytes`, `bytearray`, `memoryview`

