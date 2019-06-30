# Cargo，Crates和基本的项目结构

## Cargo

Cargo是Rust内置的包管理器和build系统。它主要用于：

- 创建新项目:`cargo new`
- 更新项目依赖：`cargo update`
- 构建项目：`cargo build`
- 在不构建的情况下，分析项目是否有错误：`cargo check`
- 构建和运行项目：`cargo run`
- 运行测试：`cargo test`
- 通过rustdoc生成项目文档：`cargo doc`

除了这些cargo命令，特别地，用cargo可直接发布crate。

- `cargo login`： 获取API令牌
- `cargo package`：将本地创建上传到crate.io
- `cargo publish`：将本地创建上传到crate.io并上传crate

## Crate

一个crate就是一个包。crate可以通过[Cargo](https://crates.io/)来分享。

一个crate可以生成可执行文件或库，换句话说，crate可是二进制crate或库crate。

1、`cargo new crate_name --bin` 或`cargo new crate_name`：生成**可执行crate**

2、`cargo new crate_name --lib`：生成一个**库crate**

第一个命令创建：

```
├── Cargo.toml
└── src
	└── main.rs
```

第二个命令创建：

```
├── Cargo.toml
└── src
	└── lib.rs
```

**Cargo.toml**(大写C)是配置文件，包含了Cargo需要编译项目的所有元数据。

**src**文件夹是存放源代码的地方

每个crate有一个隐式的crate根/入口。**main.rs**是二进制crate的crate根，**lib.rs**是库crate的crate根。

```
💡当我们用cargo build或cargo run构建一个二进制crate时，可执行文件将存放在target/debug文件夹。但当我们用cargo build --release构建一个发行版，它将存放在target/release文件夹。
```

## 项目结构

这是[Cargo文档](https://doc.rust-lang.org/cargo/guide/#project-layout)介绍的推荐项目布局，

```
.
├── Cargo.lock
├── Cargo.toml
├── benches
│   └── large-input.rs
├── examples
│   └── simple.rs
├── src
│   ├── bin
│   │   └── another_executable.rs
│   ├── lib.rs
│   └── main.rs
└── tests
    └── some-integration-tests.rs
```

- 源代码位于`src`目录。
- 默认库文件是`src/lib.rs`。
- 默认可执行文件是`src/main.rs`。
- 其他可执行文件可以放在`src/bin/*.rs`。
- 集成测试位于`tests`目录(单元测试在每个测试文件)。
- 例子位于`examples`目录。
- 性能测试位于`benches`目录。