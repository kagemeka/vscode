# VSCode LSP Settings 



# Python LSP
install `Python` extension.



# Go LSP
install `Go` extension and its dependencies



# Dart LSP
install `Dart` extension.



# Rust LSP

1. install extension `Rust` and `rust-analyzer`
2. set rustupPath in your settings.json
 
```json
"rust-client.rustupPath": "$HOME/.cargo/bin/rustup",
```

- use in a Docker container
  1. open vscode settings and selsect User/Workspace tab
  2. search `Rust-client: Rustup Path` -> `$HOME/.cargo/bin/rustup`
  3. reload vscode



# Swift LSP
## build official extension 

- see also official references
  - https://github.com/apple/sourcekit-lsp
  - https://github.com/apple/sourcekit-lsp/blob/main/Documentation/Development.md
  - https://github.com/apple/sourcekit-lsp/tree/main/Editors
  - https://github.com/apple/sourcekit-lsp/tree/main/Editors/vscode


- generate the extension installer
  1. prerequisites
    - install nodejs to be able to use npm command. 
  2. generate the installer `sourcekit-lsp-vscode-dev.vsix`.
'''sh
$ git clone https://github.com/apple/sourcekit-lsp.git \
  && cd sourcekit-lsp/Editors/vscode/ \
  && npm install \
  && npm run dev-package \
  && mv sourcekit-lsp-development.vsix /root/
'''

- install sourcekit-lsp extension
  1. open command palette(`Ctrl` + `Shift` + `P`)
  2. search `Extensions: Install from VSIX` to install the vscode extension from a vsix file.
  3. select `/root/sourcekit-lsp-vscode-dev.vsix`
  
- set language server paths
  1. open vscode settings and select User/Workspace tab
    - search `Sourcekit-lsp: Server Path` -> `${SOURCEKIT_TOOLCHAIN_PATH}/usr/bin/sourcekit-lsp`
      - e.g., if you install swift as `/usr/local/swift`, replace `${SOURCEKIT_TOOLCHAIN_PATH}` with `/usr/local/swift`
    - search `Sourcekit-lsp: Toolchain Path` -> `${SOURCEKIT_TOOLCHAIN_PATH}`
    - search`Sourcekit-lsp Trace: Server` -> `verbose` (Optional)

- reload vscode 


## install unofficial extension
install Extension `SourceKit-LSP - Unofficial CI build`


# Haskell LSP
- install 
  - Haskell
  - Haskell Syntax Highlighting
  - haskell-linter


# OCaml LSP 
- run `opam install -y ocaml-lsp-server`
- install `OCaml Platform` 
- for detail, see [here](https://ocaml.org/learn/tutorials/up_and_running.html).



# Scala LCP
- install `Scala (Metals)`.
- for detail, see [here](https://docs.scala-lang.org/getting-started/index.html)
