# 🖱️ find_your_center.ps1

**Purpose:**
Get the live X and Y coordinates of your mouse cursor using PowerShell. Perfect for UI scripting, automation, or just centering your soul.

---

## 💡 Description
This minimal PowerShell script continuously displays the current mouse cursor coordinates on your screen every second. It’s a great tool when you're scripting clicks, aligning windows, or channeling your inner monk for pixel-perfect placement.

---

## 📜 Script
```powershell
Add-Type -AssemblyName System.Windows.Forms

while ($true) {
    $position = [System.Windows.Forms.Cursor]::Position

    Write-Host -NoNewline ("`rX: {0} | Y: {1}" -f $position.X, $position.Y)

    # Sleep for a short interval (e.g., 1 second)
    Start-Sleep -Seconds 1
}
```

---

## 🛠️ How to Use
1. Open PowerShell.
2. Save this script as `find_your_center.ps1`.
3. Run the script:
   ```powershell
   .\find_your_center.ps1
   ```
4. Watch your coordinates update live in the console.

---

## 💬 Notes
- You can change the `Start-Sleep` interval for faster or slower updates.
- Great for UI testing, pixel hunting in old games, or figuring out where the hell the OK button went.

---

## ⚠️ Disclaimer
This won't help you find emotional balance. Just the mouse.

---

## ✨ Made for chaotic devs by chaotic devs
If you’re on a journey of building weird scripts for oddly specific problems — welcome home.

