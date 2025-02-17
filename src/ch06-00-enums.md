# Enums and Pattern Matching

*enumerations*, also referred to as *enums*.
Enums allow you to define a type by enumerating its possible *variants*. First
we’ll define and use an enum to show how an enum can encode meaning along with
data. Next, we’ll explore a particularly useful enum, called `Option`, which
expresses that a value can be either something or nothing. Then we’ll look at
how pattern matching in the `match` expression and how the `if let`
construct is another convenient idiom available to handle enums.
