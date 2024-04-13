# Demo CMake Tools Bashrc

Issue: https://github.com/microsoft/vscode-cmake-tools/issues/3705

1.  Configure the project on the command-line:

    ```bash
    git clone https://github.com/hwhsu1231-demo/demo-cmake-tools-bashrc.git
    cd demo-cmake-tools-bashrc
    cmake --preset default
    ```

2.  Configure the project in the VSCode with CMake Tools:

    ```bash
    code .
    ```

    And then:

    1.  Press `Ctrl+Shift+P`.
    2.  Type `CMake: Select Configure Preset` and select `default`.
    3.  Type `CMake: Delete Cache and Reconfigure`.
