# Rust Crash Course

  > !IMPORTANT! | This course is still being created, you can use it, but it isn't 10% finished.

## Information
This is a crash course in the Rust programming language, I am learning this in public and will be keeping all my files here for you all to read and learn from.

[Book Used](https://doc.rust-lang.org/book/)

## Foreward
I started learning Rust thanks to [Francesco Ciull]() and his first livestream in the [Rust From Zero]() series on his [YouTube channel]() on Thursday 8th December 2022.

### Lesson 1 - Installing and Hello World
#### Installing Rust
To get started we have to do a little bit of installing. To install on Windows is a bit harder so for this course, I'll be using Linux, you can follow these steps on Windows using WSL or by following the Windows install instructions in the book used.

To install Rust, we use a tool called `rustup`.

To install `rustup`,
```bash
$ curl --proto '=https' --tlsv1.3 https://sh.rustup.rs -sSf | sh
```
This command downloads a script and starts the installation of the `rustup` tool, which installs the latest stable version of Rust. Password may be needed. If it was successful, this will appear:
```bash
Rust is installed now. Great!
```
#### Updating and Uninstall
To update and uninstall rustup, use the following commands:
```bash
$ rustup update
```
```bash
$ rustup self uninstall
```

For local documentation run `rustup doc`.

### Hello World Program
To start with we are going to be programming a Hello World program.
To do this we are going to use the following code:
```rust
fn main() {
    println!("Hello, world!");
}
```

---

Let's go through the code now.


```rust
fn main() {

}
```
This  is a function called main. All the code for the function go inside the squigly brackets.

```rust
println!("Hello, world!");
```
This is the print command, the `!` tells us that it is text. The `;` on the end acts like it does in JavaScript, basically saying that the command has finished, and to move on.

### Hello Cargo
Cargo is Rust's build system and package manager. Much like `npm` for JavaScript and `pip` for Python. Cargo does many things for Rust developers including:
  - Building your code
  - Downloading the libraries your code depends on
    -  Building those dependencies

Now, the difference between this section and the last is that this one is all done through Cargo.

To start lets create a new project:
```bash
cargo new hello_cargo
```

 > This command also initialises a git repo, if you don't want this to happen, use the `--vcs` flag. Run `cargo new --help` to see all available options.

 This command creates a new project inside a directory called `hello_cargo`. This directory contains two files and a folder.

It should look a bit like this:

  - hello_cargo
    - src/
      - main.rs
    - Cargo.lock
    - Cargo.toml

Let's take a look in `Cargo.toml`:
```toml
[package]
name = "hello_cargo"
version = "0.1.0"
edition = "2021"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]

```
