# Astrolabe Releases

This repository hosts releases for the **Astrolabe** desktop application — a 3D dependency graph visualization tool for Lean 4 formal mathematics projects.

🌐 **Website**: [astrolean.io](https://astrolean.io)

## Download

Download the latest version from the [Releases](https://github.com/Lean-Astrolabe/Astrolabe-Releases/releases) page.

| Platform | File | Architecture |
|----------|------|--------------|
| macOS (Apple Silicon) | `Astrolabe_x.x.x_aarch64.dmg` | M1/M2/M3 |
| macOS (Intel) | `Astrolabe_x.x.x_x64.dmg` | Intel |
| Windows | `Astrolabe_x.x.x_x64-setup.exe` | 64-bit |
| Linux | 🚧 Coming soon | — |

## Installation Guide

### macOS

Since Astrolabe is not yet signed with an Apple Developer certificate, macOS will block the app by default. Follow these steps to open it:

#### Method 1: Right-click to Open (Recommended)

1. Download the `.dmg` file and open it
2. Drag `Astrolabe.app` to your **Applications** folder
3. **Right-click** (or Control-click) on `Astrolabe.app`
4. Select **"Open"** from the context menu
5. Click **"Open"** in the dialog that appears
6. The app will now open and be remembered as safe

#### Method 2: System Preferences

If Method 1 doesn't work:

1. Try to open `Astrolabe.app` (it will be blocked)
2. Open **System Preferences** → **Privacy & Security**
3. Scroll down to find the message about Astrolabe being blocked
4. Click **"Open Anyway"**
5. Enter your password if prompted
6. Click **"Open"** in the confirmation dialog

#### Intel Mac Additional Step

For Intel Macs, you may need to remove the quarantine attribute:
```bash
xattr -cr /Applications/Astrolabe.app
```

### Windows

Since Astrolabe is not yet signed with a Windows certificate, Windows Defender SmartScreen may block the installer.

1. Download the `.exe` installer
2. When you see "Windows protected your PC", click **"More info"**
3. Click **"Run anyway"**
4. Follow the installation wizard

### Linux

🚧 **Coming soon** — Linux support is in development.

## Requirements

- A Lean 4 project with `lakefile.lean`
- Run `lake build` at least once before using Astrolabe (to generate `.ilean` files)

## Getting Started

1. Open Astrolabe
2. Select your Lean 4 project folder
3. Wait for the dependency graph to load
4. Explore your theorems and definitions in 3D!

## Troubleshooting

### "App is damaged and can't be opened" (macOS)

Run this command in Terminal:
```bash
xattr -cr /Applications/Astrolabe.app
```

### No nodes appear in the graph

Make sure you have run `lake build` in your Lean project to generate `.ilean` files.

### App crashes on startup

Please report the issue with your system information at [Issues](https://github.com/Lean-Astrolabe/Astrolabe-Releases/issues).

## Feedback & Support

- 🐛 **Bug Reports**: [GitHub Issues](https://github.com/Lean-Astrolabe/Astrolabe-Releases/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/Lean-Astrolabe/Astrolabe-Releases/discussions)
- 🌐 **Website**: [astrolean.io](https://astrolean.io)

## License

Astrolabe is proprietary software. See [LICENSE](LICENSE) for details.
