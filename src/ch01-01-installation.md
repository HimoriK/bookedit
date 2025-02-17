## Installation

Download Rust through `rustup`, a command line tool for managing Rust versions and associated tools. 

> Note: If you prefer not to use `rustup` for some reason, see 
> [Other Rust Installation Methods page][otherinstall] for more options.

> ### Command Line Notation
>
> Throughout the book, some commands are used in the
> terminal. PowerShell-specific examples will use `>` rather than `$`.

### Installing `rustup` on Linux or macOS

If you’re using Linux or macOS, open a terminal and enter the following command:

```console
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

The command downloads a script and installs the `rustup`
tool with the latest stable version of Rust. If the install is successful, the following line will appear:

```text
Rust is installed now. Great!
```

You will also need a *linker*, which is a program that Rust uses to join its
compiled outputs into one file. It is likely you already have one. If you get
linker errors, you should install a C compiler, which will typically include a
linker. A C compiler is also useful because some common Rust packages depend on
C code and will need a C compiler.

On macOS, you can get a C compiler by running:

```console
$ xcode-select --install
```

Linux users should generally install GCC or Clang, according to their
distribution’s documentation. For example, if you use Ubuntu, you can install
the `build-essential` package.

### Installing `rustup` on Windows

On Windows, go to [https://www.rust-lang.org/tools/install][install] to install Rust. 
At some point in the installation, you’ll receive a message explaining that you’ll also 
need the MSVC build tools for Visual Studio 2013 or later.

To acquire the build tools, you’ll need to install [Visual Studio
2022][visualstudio]. When asked which workloads to install, include:

* “Desktop Development with C++”
* The Windows 10 or 11 SDK

The rest of this book uses commands that work in both *cmd.exe* and PowerShell.

### Troubleshooting

To check whether you have Rust installed correctly, open a shell and enter this
line:

```console
$ rustc --version
```

You should see the version number, commit hash, and commit date for the latest
stable version that has been released, in the following format:

```text
rustc x.y.z (abcabcabc yyyy-mm-dd)
```

If you see this information, you have installed Rust successfully! If you don’t
see this information, check that Rust is in your `%PATH%` system variable as
follows.

In Windows CMD, use:

```console
> echo %PATH%
```

In PowerShell, use:

```powershell
> echo $env:Path
```

In Linux and macOS, use:

```console
$ echo $PATH
```

If Rust still isn’t working, ask for help from other Rustaceans (a
silly nickname we call ourselves) on [the community page][community].

### Updating and Uninstalling

Once Rust is installed via `rustup`, updating to a newly released version is
easy. From your shell, run the following update script:

```console
$ rustup update
```

To uninstall Rust and `rustup`, run the following uninstall script from your
shell:

```console
$ rustup self uninstall
```

### Local Documentation

Run `rustup doc` to open the local documentation
in your browser. 

If you need to learn a type or function provided by 
the standard library, check the API documentation!

[otherinstall]: https://forge.rust-lang.org/infra/other-installation-methods.html
[install]: https://www.rust-lang.org/tools/install
[visualstudio]: https://visualstudio.microsoft.com/downloads/
[community]: https://www.rust-lang.org/community
