Why Rust？

## Rust历史

Rust最初是由Mozilla员工Graydon Hoare设计、开发的个人项目。Mozilla在2009年开始赞助该项目并于2010年宣布。但第一个稳定版本，Rust 1.0于2015年5月15日发布。

## 初始目标

Rust的目标是成为创建高并发和高安全的系统的优秀语言。此外，Rust旨在同时提供速度和安全。

> “Rust是一门系统编程语言，专注于三个目标：安全，速度和并发”。——Rust文档

Rust是非常年轻和非常现代化的语言。它是一种编译型编程语言，使用[LLVM](https://en.wikipedia.org/wiki/LLVM)作为后端。并且Rust是多范式编程语言，它支持命令式过程，并发actor，面向对象和纯函数式风格。它还支持静态和动态风格的泛型编程和元编程(ML)。

> 🔎 Rust最独特和引人注目的特性之一是所有权(Ownership)，用于实现内存安全。Rust会乐观地创建内存指针，在编译时使用引用(reference)和借用(borowing)来检查内存指针的有限访问。它通过检查生命周期(lifetime)来自动编译时内存管理。

影响

Rust的设计元素受到众多编程语言启发。

- 抽象机器模型：**C**
- 数据类型：**C**，**SML**，**OCaml**，**Lisp**，**Limbo**
- 可选绑定：**Swift**
- Hygienic宏：**Scheme**
- 函数式编程：**Haskell**，**OCaml**，**F#**
- 属性：**ECMA-335**
- 内存模型和内存管理：**C++**，**ML Kit**，**Cyclone**
- Type Classses：**Haskell**
- Crate：在**ECMA**-335 CLI模型中的汇编
- 通道和并发：**Newsqueak**，**Alef**，**Limbo**
- 消息传递和线程故障：**Erlang**

等等

Rust默认情况下不使用自动垃圾回收系统(GC)。

Rust编译器在编译时观察代码，有助于防止用诸如C/C++语言编写时可能的很多类型错误。

