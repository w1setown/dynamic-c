# 🧠 Assignment: Build a Dynamic Array (Vector) in C

## 📋 Overview

In this assignment, you will implement your own dynamic array (also known as a vector) in **pure C**. A dynamic array grows or shrinks in size during runtime, and will give you hands-on experience with `malloc`, `realloc`, `free`, pointers, and structs — the building blocks of memory management in C.

---

## 🎯 Objectives

- Implement a dynamic array (vector) for integers
- Understand how dynamic memory allocation works in C
- Practice working with structs, pointers, and heap memory
- Design a small reusable C module with a clean API

---

## ✅ Requirements

### Functional Requirements
- [ ] Define a `Vector` struct with `data`, `size`, and `capacity`
- [ ] Implement the following core functions:
  - `void vector_init(Vector *vec)`
  - `void vector_push(Vector *vec, int value)`
  - `int  vector_get(Vector *vec, size_t index)`
  - `void vector_free(Vector *vec)`
- [ ] Implement **automatic resizing** when the array is full
- [ ] Prevent memory leaks with proper cleanup

### Technical Constraints
- ❌ No C++ (`new`, `class`, `std::vector`, etc.)
- ✅ Must use only C standard library functions: `malloc`, `realloc`, `free`, `printf`, etc.
- ✅ Use `.h` and `.c` files to separate declaration and implementation

---

## 🧪 Example Usage

```c
#include "vector.h"

int main() {
    Vector vec;
    vector_init(&vec);

    for (int i = 0; i < 10; ++i) {
        vector_push(&vec, i * 10);
    }

    for (size_t i = 0; i < vec.size; ++i) {
        printf("%d ", vector_get(&vec, i));
    }

    vector_free(&vec);
    return 0;
}
