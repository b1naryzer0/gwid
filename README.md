** GetWindowsInstallDate (gwid) **

gwid determines the original installation date of Windows.

Standard tools such as systeminfo or WMI often only return the date of the latest build version.
gwid attempts to determine the actual, original installation date using registry keys and folder timestamps
to determine this and returns the oldest value from the data obtained as the result.

PS C:\> gwid
* tries to determine the original installation date and outputs it

PS C:\> gwid -all
* lists all detected sources (chronological) and outputs the installdate

PS C:\> gwid /?
* Usage: gwid.exe [-all] [/?]
