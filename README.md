# YoWSL

Yet another Windows Subsystem for Linux tweaker.

**This project is in the very very early stage of development.**

## Features

* Register a WSL distro from a `.tar.gz` file
* Unregister a WSL distro
* Get the configuration of a registered WSL distro
* Set the configuration of a registered WSL distro
* Launch a registered WSL distro

## Installation

You can download pre-built binaries from [the downloads page](https://bitbucket.org/ykomatsu/yowsl/downloads/).

## Running

```
> # To register:
> New-Item -Name MyUbuntu -ItemType Directory
> yowsl.exe register MyUbuntu -s install.tar.gz -d MyUbuntu
```

```
> # To launch:
> yowsl.exe launch MyUbuntu
```

```
> # To get the configuration:
> yowsl.exe get-configuration MyUbuntu
[MyUbuntu]
version = 1
default_uid = 0
flags = 7 # 0b111 -> ENABLE_INTEROP (1) | APPEND_NT_PATH (2) | ENABLE_DRIVE_MOUNTING (4)
default_environment_values = ["HOSTTYPE=x86_64", "LANG=en_US.UTF-8", "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games", "TERM=xterm-256color"]
```

```
> # To set the configuration:
> yowsl.exe set-configuration MyUbuntu -u 1000
```

```
> # To unregister:
> yowsl.exe unregister MyUbuntu
```

## License

YoWSL is distributed under the terms of the Apache License, Version 2.0.
See `LICENSE-APACHE-2-0` for details.
