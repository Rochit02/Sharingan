# Sharingan 👁️

Sharingan is a high-performance, ultra-stealthy Remote Control and Screen Sharing application designed specifically for seamless use over a local network. 

Whether you need to monitor a secondary machine, provide remote assistance, or control a desktop discreetly from a laptop on the same network, Sharingan provides Low-latency access directly through a standard web browser without leaving a trace on the host machine's taskbar.

## 🚀 Key Features

- **Ultimate Stealth:** Sharingan compiles into a single, standalone executable (`Sharingan.exe`). When launched, it runs entirely in the background without a console window. Its only footprint is a discreet system tray icon hidden in the Windows taskbar.
- **Undetectable Operation:** Because Sharingan is a custom, self-compiled Python script running silently in the background, it does not trigger standard flags associated with commercial remote desktop software (like TeamViewer or AnyDesk) by automated monitoring systems. It is also undetectable by platforms like Hacker Rank while writing your exams for placements.
- **Browser-Based Viewer:** The client does not need to install any software. Simply enter the host's local IP address into any modern web browser (Chrome, Firefox, Safari) from a laptop or mobile device to instantly view and control the screen.
- **Low-Latency Streaming:** Engineered for local networks, the video feed uses optimized MJPEG streaming locked at 60 FPS at 1080p resolution. This guarantees crystal-clear text readability with absolutely Low network buffer bloat or input lag.
- **Full Remote Control:**
  - **Mouse:** Left, right, and middle clicks map perfectly to the host.
  - **Scroll:** Seamless scrolling support.
  - **Keyboard:** Keystrokes typed while the viewer is active are instantly forwarded to the host machine.
- **Secure Authentication:** Dynamically generates a random 8-digit passcode every time it runs. Clients must enter this code on a sleek login page before gaining access to the remote desktop.
- **Single-Instance Lock:** Built-in safeguards ensure the application binds to a secure background port, preventing accidental duplicate launches.

## 🛠️ Installation & Compilation

1. Clone or download the repository to your host machine.
2. Install the required dependencies:
   ```powershell
   pip install -r requirements.txt
   pip install pystray Pillow pyinstaller
   ```
3. Compile the application into a stealthy, standalone executable:
   ```powershell
   pyinstaller --name "Sharingan" --onefile --noconsole --add-data "templates;templates" host.py
   ```
4. The resulting `Sharingan.exe` will be located in the `dist/` folder.

## 🎮 Usage

1. Run `Sharingan.exe` on the host PC. 
2. A popup will immediately appear displaying the local network URL (e.g., `http://192.168.1.5:5000`) and the **8-digit passcode** for the current session. 
3. The app will then minimize to the Windows system tray (hidden icons). 
4. On your client laptop (connected to the same Wi-Fi or LAN), open a web browser and navigate to the provided URL.
5. Enter the 8-digit passcode on the login screen to authenticate.
6. You now have full view and control of the host PC! You can also double-click the video feed to enter Full-Screen mode, or use the "Buy Me A Coffee" button directly within the client viewer.

### System Tray Controls
Right-click the red Sharingan icon in the system tray to access the menu:
- **Show URL:** Displays the connection URL again and provides a quick donation link.
- **Exit:** Securely terminates all background capture and web server threads, closing the application completely.

## ☕ Support
If you find this tool useful, consider supporting the development!
**[Donate via BuyMeACoffee](https://buymeacoffee.com/rochit)**
