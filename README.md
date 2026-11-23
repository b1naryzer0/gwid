************************************
GetWindowsInstallDate (gwid)
************************************
gwid determines the original installation date of Windows.

Standard tools such as systeminfo or WMI often only return the date of the latest build version.
gwid attempts to determine the actual, original installation date using registry keys and folder timestamps
to determine this and returns the oldest value from the data obtained as the result.

PS C:\> gwid
Original installation date: 23.05.2019 18:07:16


PS C:\> gwid -all
********************************
* GetWindowsInstallDate (gwid) *
*    (c) 80sKid 11/2026        *
********************************

All detected sources (chronological):
-----------------------------------------------------------------
09.12.2024 01:03:04     |  Current OS (Build 26300)
02.04.2023 10:37:37     |  Registry history (Source OS (Updated on 12/8/2023 22:06:27), Build 19045)
08.12.2023 22:42:32     |  Registry history (Source OS (Updated on 12/8/2024 23:58:29), Build 22631)
01.04.2024 08:21:16     |  Folder: C:\Users\Default
23.05.2019 18:07:16     |  Folder: C:\Recovery
01.04.2024 08:21:16     |  File:   C:\Windows\System32\config\SYSTEM

Original installation date: 23.05.2019 18:07:16

PS C:\> gwid /?
********************************
* GetWindowsInstallDate (gwid) *
*    (c) 80sKid 11/2026        *
********************************
Determines the original installation date of Windows.

Usage: gwid.exe [-all] [/?]

Parameters:
  -all        Lists all detected system and registry sources chronologically.
  /?          Displays this help and usage information.


