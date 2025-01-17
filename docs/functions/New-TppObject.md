# New-TppObject

## SYNOPSIS
Create a new object

## SYNTAX

```
New-TppObject [-Path] <String> [-Class] <String> [[-Attribute] <Hashtable>] [-PushCertificate] [-PassThru]
 [[-VenafiSession] <PSObject>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Generic use function to create a new object if a specific function hasn't been created yet for the class.

## EXAMPLES

### EXAMPLE 1
```
New-TppObject -Path '\VED\Policy\Test Device' -Class 'Device' -Attribute @{'Description'='new device testing'}
Create a new device
```

### EXAMPLE 2
```
New-TppObject -Path '\VED\Policy\Test Device' -Class 'Device' -Attribute @{'Description'='new device testing'} -PassThru
Create a new device and return the resultant object
```

### EXAMPLE 3
```
New-TppObject -Path '\VED\Policy\Test Device\App' -Class 'Basic' -Attribute @{'Driver Name'='appbasic';'Certificate'='\Ved\Policy\mycert.com'}
Create a new Basic application and associate it to a device and certificate
```

## PARAMETERS

### -Path
Full path, including name, for the object to be created.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Class
Class name of the new object.
See https://docs.venafi.com/Docs/current/TopNav/Content/SDK/WebSDK/SchemaReference/r-SDK-CNattributesWhere.php for more info.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Attribute
Hashtable with initial values for the new object.
These will be specific to the object class being created.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PushCertificate
If creating an application object, you can optionally push the certificate once the creation is complete.
Only available if a 'Certificate' key containing the certificate path is provided for Attribute.
Please note, this feature was added in v18.3.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ProvisionCertificate

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Return a TppObject representing the newly created object.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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
Position: 4
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

### none
## OUTPUTS

### TppObject, if PassThru provided
## NOTES

## RELATED LINKS

[http://VenafiPS.readthedocs.io/en/latest/functions/New-TppObject/](http://VenafiPS.readthedocs.io/en/latest/functions/New-TppObject/)

[https://github.com/Venafi/VenafiPS/blob/main/VenafiPS/Public/New-TppObject.ps1](https://github.com/Venafi/VenafiPS/blob/main/VenafiPS/Public/New-TppObject.ps1)

[https://github.com/Venafi/VenafiPS/blob/main/VenafiPS/Public/Add-TppCertificateAssociation.ps1](https://github.com/Venafi/VenafiPS/blob/main/VenafiPS/Public/Add-TppCertificateAssociation.ps1)

[https://docs.venafi.com/Docs/current/TopNav/Content/SDK/WebSDK/r-SDK-POST-Config-create.php](https://docs.venafi.com/Docs/current/TopNav/Content/SDK/WebSDK/r-SDK-POST-Config-create.php)

[https://docs.venafi.com/Docs/current/TopNav/Content/SDK/WebSDK/SchemaReference/r-SDK-CNattributesWhere.php](https://docs.venafi.com/Docs/current/TopNav/Content/SDK/WebSDK/SchemaReference/r-SDK-CNattributesWhere.php)

