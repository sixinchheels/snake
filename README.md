============================================================
SNAKE GAME - HOW TO PLAY ON ANY DEVICE
============================================================

WHAT YOU NEED
-------------
1. A DOS emulator (DOSBox is the standard choice)
2. The snake.com file (assembled from snake.asm with NASM)

The .com file is tiny (~1 KB) and portable to every platform.


============================================================
WINDOWS
============================================================

Option A: DOSBox (Recommended)
  1. Download DOSBox from https://www.dosbox.com/download.php?main=1
  2. Run the installer
  3. Put snake.com in a folder, e.g. C:\snake\
  4. Open DOSBox
  5. At the Z:\> prompt, type:
       mount c C:\snake
       c:
       snake.com

Option B: Drag-and-Drop
  Drag snake.com directly onto the DOSBox icon.

Option C: DOSBox-X
  Download from https://dosbox-x.com/ for more features.


============================================================
MACOS
============================================================

Option A: DOSBox via Homebrew
  brew install dosbox
  cd ~/Desktop/snake
  dosbox snake.com

Option B: DOSBox-X via Homebrew
  brew install dosbox-x
  dosbox-x snake.com

Option C: Flatpak
  flatpak install flathub com.dosbox_x.DOSBox-X
  flatpak run com.dosbox_x.DOSBox-X snake.com


============================================================
LINUX (Any Distro)
============================================================

Debian / Ubuntu / Mint:
  sudo apt install dosbox
  dosbox snake.com

Fedora:
  sudo dnf install dosbox
  dosbox snake.com

Arch / CachyOS / Manjaro:
  sudo pacman -S dosbox
  dosbox snake.com

Flatpak (works everywhere):
  flatpak install flathub com.dosbox.DOSBox
  flatpak run com.dosbox.DOSBox snake.com


============================================================
IPHONE / IPAD
============================================================

iOS doesn't allow DOS emulators in the App Store.

Option A: Browser-based emulator (easiest)
  - Go to https://js-dos.com/
  - Upload snake.com
  - Play in Safari

Option B: iDOS 2 (sideload only)
  - Requires AltStore or similar sideloading tools

Option C: Remote to a PC
  - Run DOSBox on your computer
  - Use VNC or Chrome Remote Desktop


============================================================
BROWSER (Any Device)
============================================================

No install needed. Use js-dos:

  1. Go to https://js-dos.com/
  2. Drag and drop snake.com onto the page
  3. Play directly in the browser

Works on any device with a modern browser
(desktop, laptop, tablet, phone, even some smart TVs).
