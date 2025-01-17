# New-TppCodeSignProject

## SYNOPSIS
Create a new code sign project

## SYNTAX

```
New-TppCodeSignProject [-Path] <String> [[-VenafiSession] <PSObject>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Create a new code sign project which will be empty.

## EXAMPLES

### EXAMPLE 1
```
New-TppCodeSignProject -Path '\ved\code signing\projects\my_project'
Create a new code sign project
```

## PARAMETERS

### -Path
Path of the project to create

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Path
## OUTPUTS

### PSCustomObject with the following properties:
###     Application
###     Auditor
###     CertificateEnvironments
###     Collection
###     CreatedOn
###     Guid
###     Id
###     KeyUseApprovers
###     KeyUsers
###     Owners
###     Status
###     Name
###     Path
###     TypeName
## NOTES

## RELATED LINKS

[http://VenafiPS.readthedocs.io/en/latest/functions/New-TppCodeSignProject/](http://VenafiPS.readthedocs.io/en/latest/functions/New-TppCodeSignProject/)

[https://github.com/Venafi/VenafiPS/blob/main/VenafiPS/Public/New-TppCodeSignProject.ps1](https://github.com/Venafi/VenafiPS/blob/main/VenafiPS/Public/New-TppCodeSignProject.ps1)

[https://docs.venafi.com/Docs/current/TopNav/Content/SDK/CodeSignSDK/r-SDKc-POST-Codesign-CreateProject.php](https://docs.venafi.com/Docs/current/TopNav/Content/SDK/CodeSignSDK/r-SDKc-POST-Codesign-CreateProject.php)

