# Comparison: Intersections

## Intersection on one side of the comparison

```py
x = "x" * 1_000_000_000
reveal_type(x)  # revealed: LiteralString

if x != "abc":
    reveal_type(x)  # revealed: LiteralString & ~Literal["abc"]

    reveal_type(x != "abc")  # revealed: Literal[True]
    reveal_type(x == "something else")  # revealed: bool

    reveal_type(x == "abc")  # revealed: Literal[False]
    reveal_type(x == "something else")  # revealed: bool
```
