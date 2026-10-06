*This project has been created as part of the 42 curriculum by rmanzana*

# C++ Module 07 — C++ templates

## Description

Eighth module of the 42 C++ piscine. It introduces **templates**: writing functions and classes once, for any type, and letting the compiler generate the concrete version for each type they are used with. Templates are the foundation of the C++ Standard Template Library used in the next modules.

All the code follows the **C++98** standard and compiles with `c++ -Wall -Wextra -Werror -std=c++98`.

## Exercises

| Exercise | Program | Description |
|---|---|---|
| `ex00` — Start with a few functions | `whatever` | Function templates `swap()`, `min()` and `max()`, which work with any type that supports the comparison operators. When both values are equal, `min` and `max` return the second one. |
| `ex01` — Iter | `iter` | A function template `iter(array, length, function)` that applies a function to every element of an array of any type. It has overloads for `const` and non-`const` arrays, so it works both with functions that modify the elements and with functions that only read them. |
| `ex02` — Array | `array` | A class template `Array<T>` similar to a fixed-size `std::vector`: it allocates its elements with `new T[n]()` (value-initialised), supports deep copies, gives access through `operator[]` and throws an exception when the index is out of bounds, and returns its size with `size()`. The implementation lives in a `.tpp` file included by the header. |

## Key concepts

- **Function templates** and **class templates**: `template <typename T>`.
- **Template instantiation:** the compiler generates code for every type a template is used with, so the implementation must be visible where it is used — hence templates are written in headers (or `.tpp` files included by them).
- **Template overloading** for `const` / non-`const` versions.
- **Value initialisation** with `new T[n]()`.
- **Deep copy** and **bounds checking** with exceptions.

## Instructions

Each exercise has its own `Makefile`:

```bash
cd ex02
make
./array
```

`make clean`, `make fclean` and `make re` are available in every exercise.

## Resources

- [cplusplus.com — Templates](https://cplusplus.com/doc/oldtutorial/templates/)
- [cppreference — Templates](https://en.cppreference.com/w/cpp/language/templates)
- [LearnCpp.com — Function templates](https://www.learncpp.com/cpp-tutorial/function-templates/) and [Class templates](https://www.learncpp.com/cpp-tutorial/class-templates/)
- [isocpp.org FAQ — Why can't I separate the definition of my template class from its declaration?](https://isocpp.org/wiki/faq/templates#templates-defn-vs-decl)
