# Windows Registry Hacks

All of the following registry edits are tested on Windows 11 unless explictly stated

## Disable Web Search in Start Menu and Explorer
```
if( -not (Test-Path -Path HKLM:\SOFTWARE\Policies\Microsoft\Windows\Explorer)){
    New-Item HKLM:\SOFTWARE\Policies\Microsoft\Windows\Explorer
}
Set-ItemProperty -Path HKLM:\SOFTWARE\Policies\Microsoft\Windows\Explorer -Name "DisableSearchBoxSuggestions" -Value 1 -Type DWORD
```

## Bring back old context menu on Windows 11
```
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
```

