# hello_webserver

A simple multithreaded web server in **Rust**, based on **Chapter 20: Final Project: Building a Multithreaded Web Server** of *The Rust Programming Language* book.

This project implements a basic HTTP web server that listens for connections, parses requests, and serves static HTML content. It’s intended as a learning project and not a production-ready server. :contentReference[oaicite:1]{index=1}

## 🚀 Overview

This repository contains the source code for a minimal web server that:

- Listens on a TCP port (e.g., `127.0.0.1:8080`)
- Handles incoming HTTP requests
- Responds with static HTML pages
- Uses a thread pool to process connections concurrently

The implementation follows the patterns described in the Rust Book’s final project, focusing on understanding how a basic web server works under the hood. :contentReference[oaicite:2]{index=2}

## 📁 Repository Structure

```text
hello_webserver/
├── Cargo.toml
├── src/
│   └── main.rs
├── hello.html
├── 404.html
└── .gitignore

- `src/main.rs` — core Rust code implementing the web server
- `hello.html` — example HTML file served at the root
- `404.html` — served when a requested path is not found
- `Cargo.toml` — Rust project manifest and dependencies

## 📦 Requirements

Before running this project, make sure you have:

- **Rust** and **Cargo** installed — see the official Rust setup documentation.

To verify your installation, run:

```sh
rustc --version
cargo --version
```

## ▶️ Running the Server

Clone the repository:
```sh
git clone https://github.com/jackgris/hello_webserver.git
cd hello_webserver
```

Build and run using Cargo:
```sh
cargo run
```

Open a web browser and visit:
```sh
http://127.0.0.1:8080
```
You should see the content of `hello.html` displayed.

## 🧠 How It Works

This server demonstrates basic server behavior:

- Create a TCP listener bound to an address
- Accept connections in a loop
- For each connection, spawn a worker from a thread pool
- Read the request bytes and parse simple HTTP `GET` requests
- Send back HTTP responses with appropriate status and body

These ideas are explored in detail in *The Rust Programming Language* book’s final project.

## 🛠️ Extending the Server

Possible improvements include:

- Serving more file types
- Graceful shutdown
- Better request routing
- Adding logging and configuration

## 📚 Acknowledgements

This project is a direct implementation and study aid based on:

> *The Rust Programming Language* (Second Edition)
> by **Steve Klabnik** and **Carol Nichols**.
