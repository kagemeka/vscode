# VSCode LSP Settings 


# Rust Configuration

1. Install Extension `Rust`
  - Don't install `rust-analyzer`

2.  add the below line to the your settings.json

```json
"rust-client.rustupPath": "$HOME/.cargo/bin/rustup",
```

- on Docker
  1. open vscode settings and selsect User/Workspace tab
  2. search `Rust-client: Rustup Path` -> `$HOME/.cargo/bin/rustup`
  3. reload vscode



# Swift
 
1. install sourcekit-lsp extension 
   1. open command palette(`Ctrl` + `Shift` + `P`)
   2. search `Extensions: Install from VSIX`
   3. select `/root/sourcekit-lsp/Editors/vscode/out/sourcekit-lsp-vscode-dev.vsix`
   4. reload vscode

2. set language server 
   1. open vscode settings and select User/Workspace tab
     - search `Sourcekit-lsp: Server Path` -> `/usr/local/swift-toolchain/usr/bin/sourcekit-lsp`
     - search`Sourcekit-lsp Trace: Server` -> `verbose` (Optional)
   2. reload vscode 