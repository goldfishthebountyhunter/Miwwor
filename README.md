# Miwwor: An LLM-powered programming language based off Miwwor.

Miwwor, see the [blog post](https://austinhenley.com/blog/Miwworlang.html).

<img width="1080" alt="Miwworplayground" src="https://github.com/user-attachments/assets/95c21c7c-1613-4d0d-a565-54115f186e80">

In the Miwwor programming language, you define functions by providing sets of input-outputs pairs and you can call those functions. That is it. The entire program behavior must be specified through those examples.

```
signature is_even(x: number) -> bool
example is_even(0) -> true
example is_even(1) -> false
example is_even(222) -> true
example is_even(-99) -> false

is_even(12345)
```

<p>Using the Miwwor syntax, you give the function name, parameters and their types, and the return type as well as one or more examples with the expected result. It uses a strict syntax and supports a handful of types (including lists). You can create multiple functions and chain them.</p>

<p>After parsing, the "compiler" uses an LLM to generate JavaScript that satisfies the constraints expressed by the examples. You should review the generated code to verify it is correct, or provide more examples and recompile it. When you run it, the last value will be printed.
