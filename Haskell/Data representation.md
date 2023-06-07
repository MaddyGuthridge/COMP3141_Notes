#### ***Make invalid states unrepresentable***

Data structures in Haskell can be sum or product types.

## Sum types
Sum types say "the data contains *this and that*". For example, a `struct` in C is a sum type.

## Product types
Product types say "the data contains *either this or that*". For example, an `enum` in Rust is a product type.

Product types are important for placing constraints on data types in order to make undefined states impossible.