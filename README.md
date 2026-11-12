<p align="center"><img src="maut-remote.png" width="128" alt="Maut Remote"></p>

# Maut Remote for Windows

Use your Windows PC from your iPhone: its screen, mouse and keyboard, and its terminals with Claude Code,
including a chat-style Reader for Claude's conversations. Made by Maut Solutions.

**[Download the latest installer](https://github.com/jmkq0056/maut-remote-windows/releases/latest)**

## Set up

1. Run `Maut-Remote-Setup-<version>.exe`. Windows may say "Windows protected your PC" because the installer
   isn't signed yet: choose **More info**, then **Run anyway**.
2. Maut Remote opens with a QR code and an 8-digit code. On your iPhone, open **Maut Remote** (TestFlight) and
   scan the code with the camera, or tap **Add** and type the code.
3. That's it. Maut Remote starts with Windows and sits in the tray (the reaper icon). Right-click it to show
   the pairing code again, turn off starting with Windows, or quit.
4. SSH: the installer also turns on Windows' own SSH server (keys only), and the app offers **Set Up SSH** with one
   tap, so the phone's SSH terminals reach the PC too, from anywhere.

## Updating

Download the newest installer and run it. It updates Maut Remote in place: no uninstalling, your pairing,
terminals and settings stay, and Maut Remote starts again by itself.

Your phone reaches the PC directly on the same Wi-Fi or over Tailscale, and through the Maut relay from any
other network.

## Privacy

Everything between your phone and your PC is **end to end encrypted** (the Noise protocol: X25519,
ChaCha20-Poly1305, SHA-256), keyed from the pairing your phone and PC share. When the relay carries your
connection it only passes on encrypted bytes: it can't see your screen, what you type, your terminals, your
files or your Claude chats, and it can't log in to your PC. All it sees is that a PC is online, when a phone
connects, IP addresses and how much data flows. Nobody but the phones you paired can connect, and each PC is
bound to its own relay key, so no one can take its place.

## Good to know (first version)

- Windows 10 (1809 or later) or Windows 11, 64-bit.
- Not yet: the lock and sign-in screen, and windows of programs running as administrator (UAC prompts):
  Windows keeps those out of reach of normal apps. Unlock the PC at the desk for now.
- The phone's keyboard comes up by itself when you click into a text field on the PC.
- Terminals open in PowerShell (PowerShell 7 when it's installed). They keep running while your phone is away,
  and come back with Claude Code resumed after a restart.
- Uninstall from Settings > Apps.

© 2026 Maut Solutions
