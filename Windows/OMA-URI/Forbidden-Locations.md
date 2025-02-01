Good practice to test an ADMX locally via Local Group Policy editor to ensure it doesn't write the settings to a FORBIDDEN LOCATION.  If you dare do so, your system will begin throwing error 865 in the DeviceManagement-Enterprise-Diagnostics-Provider / Admin logs showing access denied.

Forbidden locations in HKLM/HKCU: 
 System,

 Software\Microsoft,
 
 Software\Policies\Microsoft keys
 
Except for the following locations:
Software\Policies\Microsoft\Office\
Software\Microsoft\Office\
Software\Microsoft\Windows\CurrentVersion\Explorer\
Software\Microsoft\Internet Explorer\
software\policies\microsoft\shared tools\proofing tools\
software\policies\microsoft\imejp\
software\policies\microsoft\ime\shared\
software\policies\microsoft\shared tools\graphics filters\
software\policies\microsoft\windows\currentversion\explorer\
software\policies\microsoft\softwareprotectionplatform\
software\policies\microsoft\officesoftwareprotectionplatform\
software\policies\microsoft\windows\windows search\preferences\
software\policies\microsoft\exchange\
software\microsoft\shared tools\proofing tools\
software\microsoft\shared tools\graphics filters\
software\microsoft\windows\windows search\preferences\
software\microsoft\exchange\
software\policies\microsoft\vba\security\
software\microsoft\onedrive
software\Microsoft\Edge
Software\Microsoft\EdgeUpdate\

In this case, if you're attempting to do an OMA-URI CSP setting for PowerShellCore, you are out of luck as they write to {HKCU/HKLM}\Software\Policies\Microsoft\PowerShellCore

See more @ https://learn.microsoft.com/en-us/windows/client-management/win32-and-centennial-app-policy-configuration#overview