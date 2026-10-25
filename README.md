# AdOps Work Tracker

AdOps Work Tracker is the desktop app for logging a day's tasks. Paste this into PowerShell on Windows. It downloads the setup program, installs it for the current user, and opens the app:

```powershell
$exe = Join-Path $env:TEMP "AdOpsWorkTracker-setup.exe"; Invoke-WebRequest -Uri "https://github.com/aiworksaanket/adops-tracker-install/releases/latest/download/AdOpsWorkTracker-setup.exe" -OutFile $exe -UseBasicParsing; Start-Process -FilePath $exe -ArgumentList "/S" -Wait; Start-Process "$env:LOCALAPPDATA\AdOps Work Tracker\adops-tracker.exe"
```

The installer is unsigned. If SmartScreen says Windows protected your PC, choose More info, then Run anyway. The service account key is not in this download.
