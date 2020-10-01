# Windows-Terminal-Config

## Default config file location:
```
C:\Users\%USERNAME%\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState
```

## Using config file via Windows Symlinks

1. Make sure you have permissions to create symbolic link from gpedit.msc if you don't have permission you have do step 2 as Administrator.
```
Computer Configuration\Windows Settings\Security Settings\Local Policies\User Rights Assignment : Create symbolic links
```
2. Create 'soft' symlink via mklink in cmd.exe
```
mklink Link Target & REM soft symlink of Target at Link
mklink /D Link Target & REM soft link pointing to a directory
```
3. Create a symlink of the settings.json at the Default config file location
```
mklink "C:\Users\%USERNAME%\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json" "C:\Users\%USERNAME%\Git Repositories\Windows-Terminal-Config\settings.json"
```

