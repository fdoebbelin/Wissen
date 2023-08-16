# Dependencies

Cargo (package manager) and rustc (compiler) will be available on your system after installing Rust. For these tools you need the following packages for them to work properly, according to the GitHub repository:

    git
    curl (on Unix)
    pkg-config (on Unix, used to figure out the libssl headers/libraries)
    OpenSSL headers (only for Unix, this is the libssl-dev package on Ubuntu)
    a C compiler (e.g. GCC)

When using Cargo to create a new project, a Git repository will be initialized, and Rust also requires a C compiler for building the binary of the app.

```
$ sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev git
```