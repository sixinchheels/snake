Step 1 — Install the Tools
Windows:
  ->NASM — download the Windows installer from https://www.nasm.us/ and add it to your PATH.
  ->DOSBox — download from https://www.dosbox.com/download.php?main=1 and install it.
  
  Verify NASM in PowerShell:

  ->powershell
  ->nasm -v
  
Linux
  ->bash
  ->sudo apt update
  ->sudo apt install nasm dosbox

Step 2 — Assemble the File in VS Code
Rename your file to something DOS-friendly, e.g. snake.asm (avoid spaces and .txt extension — NASM doesn't care, but DOSBox does when you type the filename).

  ->Open the folder in VS Code (File → Open Folder).
  ->Open the integrated terminal: Ctrl+`.

Run the exact command from your source header:
  ->bash
  ->nasm -f bin snake.asm -o snake.com

Step 3 — Run It in DOSBox
Windows (and Linux, same procedure)
Open DOSBox from the Start menu (or run dosbox in the Linux terminal), then inside the DOSBox prompt type:

  ->dos
  ->mount c C:\path\to\your\folder
  ->c:
  ->snake.com

Option B — Automatic launch (recommended for VS Code workflow):

Create a file called run.conf next to snake.com:
  ->ini
  ->[autoexec]
  ->mount c .
  ->c:
  ->snake.com
  ->exit
  
Then launch:
Windows: dosbox -conf run.conf (or "C:\Program Files\DOSBox-0.74-3\DOSBox.exe" -conf run.conf)
Linux: dosbox -conf run.conf

DOSBox will mount the current directory as C:, run the game, and close when you quit.
