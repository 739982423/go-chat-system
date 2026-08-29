# go-chat-system

A chat system implemented in **Go**. In essence, it can be considered a simple chat room application.

## Project Overview

This repository contains the complete source code of the project, including:

1. **Server-side code** — located in the `server` directory.
2. **Client-side code** — located in the `client` directory.
3. **Shared utilities and message format definitions** — located in the `commom` directory.

The `go.mod` and `go.sum` files are used for **Go dependency management**.

* **Go version:** `1.17`

## Quick Start

The server has already been deployed on an **Alibaba Cloud ECS instance**, so you can directly run `client.exe` in the project directory to connect to the chat server.

The server is deployed using a **Docker container** with the following environment:

* Go `1.17`
* Redis `6.26`

The corresponding Docker image is also publicly available on Alibaba Cloud Container Registry.

Pull the Docker image with:

```bash
docker pull registry.cn-beijing.aliyuncs.com/pj_project/go_project:01
```

After obtaining the image, the server can be deployed using the corresponding Docker configuration.

## Build from Source

If you prefer to compile the project yourself, follow these steps.

### 1. Install Go

Install **Go 1.17** on your system.

On Linux, you can download the official `.tar.gz` archive, extract it, and add the `bin` directory inside the extracted Go directory to your `PATH` environment variable.

For example:

```bash
export PATH=$PATH:/path/to/go/bin
source ~/.bashrc
```

### 2. Prepare the Project Directory

Place all project files inside a directory named:

```text
finalProject
```

The resulting directory structure should be similar to:

```text
finalProject/
├── client/
├── server/
├── commom/
├── go.mod
└── go.sum
```

### 3. Build the Client

From the `finalProject` directory, run:

```bash
go build -o client finalProject/client/main
```

This will compile the client and generate an executable named `client`.

### 4. Build the Server

The server can be compiled in the same way. Replace the `client` path with `server`:

```bash
go build -o server finalProject/server/main
```

This will generate the server executable named `server`.
