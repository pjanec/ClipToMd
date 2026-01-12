# ClipToMd for Windows

**ClipToMd** is a lightweight Windows system tray utility that processes your clipboard content. It effectively converts rich HTML content (like code copied from **VS Code**, **Cursor**, or generic web pages) into clean, plain-text **Markdown**, ready for pasting into documentation, issue trackers, or chat apps.

## Features

*   **Smart Auto-Conversion**: 
    *   **VS Code / Cursor (Default)**: Automatically detects and converts content copied from code editors like VS Code or Cursor or Antigravity (stripping local `vscode-file://` links while keeping text).
    *   **All HTML (Optional)**: Can be toggled to automatically convert *any* HTML content copied to the clipboard.
*   **Manual Hotkey**: Press `Ctrl` + `Alt` + `M` (customizable) to instantly convert current clipboard content.
*   **Clean Output**: Uses [ReverseMarkdown](https://github.com/mysticmind/reversemarkdown-net) to produce high-quality GitHub Flavored Markdown.
*   **System Tray App**: Runs silently in the background.
    *   **Info Bubbles**: Provides unobtrusive notifications upon successful conversion.
    *   **Double-click** the tray icon to toggle the tool Active/Inactive.

## Prerequisites

*   [.NET Desktop Runtime](https://dotnet.microsoft.com/download/dotnet) (Version 9.0 or later recommended).
*   Windows OS.

## Installation & Build

1.  Clone the repository:
    ```bash
    git clone https://github.com/yourusername/ClipToMd.git
    cd ClipToMd
    ```

2.  Build the project:
    ```powershell
    dotnet build -c Release
    ```

3.  Run the executable:
    ```powershell
    .\bin\Release\net9.0-windows\ClipToMd.exe
    ```

## Usage

1.  **Run** the application. You will see a small blue "M" icon in your system tray.
2.  **Right-click** the tray icon to configure auto-conversion modes:
    *   **Auto: VS Code Only** (Checked by default): Automatically converts when you copy from VS Code.
    *   **Auto: All HTML** (Unchecked by default): Automatically converts any HTML content found in the clipboard.
3.  **Copy** something!
    *   If Auto-mode matches, you'll see a small "Auto-Converted" bubble.
    *   Otherwise, press `Ctrl` + `Alt` + `M` to manually convert.
4.  **Paste** (`Ctrl` + `V`) your perfectly formatted Markdown.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](LICENSE)
