# Get-TppCodeSignEnvironment

## SYNOPSIS
Get a code sign environment

## SYNTAX

```
Get-TppCodeSignEnvironment [-Path] <String> [[-VenafiSession] <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
Get code sign environment details

## EXAMPLES

### EXAMPLE 1
```
Get-TppCodeSignEnvironment -Path '\ved\code signing\projects\my_project\my_env'
Get a code sign environment
```

### EXAMPLE 2
```
$envObj | Get-TppCodeSignEnvironment
Get a environment after searching using Find-TppCodeSignEnvironment
```

## PARAMETERS

### -Path
Path of the environment to get

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -VenafiSession
Authentication for the function.
The value defaults to the script session object $VenafiSession created by New-VenafiSession.
A TPP token or VaaS key can also provided.
If providing a TPP token, an environment variable named TppServer must also be set.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: $script:VenafiSession
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Path
## OUTPUTS

### PSCustomObject with the following properties:
###     AllowUserKeyImport
###     Disabled
###     Guid
###     Id
###     CertificateStatus
###     CertificateStatusText
###     CertificateTemplate
###     SynchronizeChain
###     Path
###     Name
###     TypeName
###     OrganizationalUnit
###     IPAddressRestriction
###     KeyUseFlowPath
###     TemplatePath
###     CertificateAuthorityPath
###     CertificatePath
###     CertificateSubject
###     City
###     KeyAlgorithm
###     KeyStorageLocation
###     Organization
###     OrganizationUnit
###     SANEmail
###     State
###     Country
## NOTES

## RELATED LINKS

[http://VenafiPS.readthedocs.io/en/latest/functions/Get-TppCodeSignEnvironment/](http://VenafiPS.readthedocs.io/en/latest/functions/Get-TppCodeSignEnvironment/)

[https://github.com/Venafi/VenafiPS/blob/main/VenafiPS/Public/Get-TppCodeSignEnvironment.ps1](https://github.com/Venafi/VenafiPS/blob/main/VenafiPS/Public/Get-TppCodeSignEnvironment.ps1)

[https://docs.venafi.com/Docs/current/TopNav/Content/SDK/CodeSignSDK/r-SDKc-POST-Codesign-GetEnvironment.php](https://docs.venafi.com/Docs/current/TopNav/Content/SDK/CodeSignSDK/r-SDKc-POST-Codesign-GetEnvironment.php)

