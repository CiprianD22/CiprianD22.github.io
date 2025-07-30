## Latest tips / quick solutions:

* Send HTTP Rest API request using <ins>Windows Powershell Version 7</ins> with Bearer/Token Authentication
 
```powershell
<# The **Invoke-RestMethod** requires an instance of .NET SecureString in which the Bearer Token is to be stored: #>
$sString = [SecureString]::new()

<# Populate the SecureString with our Token string #>
"MyTokEnStrinGHexHhHhhHhHh".ToCharArray() | %{ $sString.AppendChar($_) }

<# Invoke the API call using HTTP ('irm' is the abbreviation for **Invoke-RestMethod** in Powershell #>
$response = irm "https://api.host.com/client/v4/user/tokens/verify" -Authentication Bearer -Token $sString
```

