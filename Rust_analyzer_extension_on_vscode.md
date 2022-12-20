# When Rust Language Service (RLS) revoked setup the "rust-analyzer" to instead

1. Check out your rustup installation, if you not installed complete mode please install "rust-analyzer" component.
    ```Bash
    > rustup component add rust-analyzer
    ```
2. Install VSCode extension "rust-analyzer".
3. If when you turned up the vscode statues bar notifice you, the "rust-analyzer" server bootup failed, please add "rust-analyzer.server.path" into "rust-analyzer" extensions setting json file.
    ```Json
    "rust-analyzer.server.path": "<Your rust-analyzer.exe path>"
    ```
4. It have to attention you the rust workspace error, you should create a "Cargo.toml" file into your Rust projects parent folder.
5. Next, please type projects folder names into upon toml file
    ```Toml
    [workspace]

    members = [
        "object_name_1",
        "object_name_2",
        "object_name_2",
        #...
    ]
    ```
6. Restart your VSCode and enjoy.