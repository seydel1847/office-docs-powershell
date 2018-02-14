---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection
schema: 2.0.0
---

# Remove-RoleGroup

## SYNOPSIS
!!! Exchange Server 2010

Use the Remove-RoleGroup cmdlet to remove a management role group.

!!! Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

This cmdlet is available in on-premises Exchange and in the cloud-based service. Some parameters and settings may be exclusive to one environment or the other.

Use the Remove-RoleGroup cmdlet to remove a management role group.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Remove-RoleGroup [-Identity] <RoleGroupIdParameter> [-BypassSecurityGroupManagerCheck] [-Confirm]
 [-DomainController <Fqdn>] [-Force] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

When you remove a role group, all the management role assignments that are assigned management roles to the role group are also removed. The management roles aren't removed. Members of a removed role group can no longer manage a feature if the role group was the only means by which they were granted access to the feature.

You can't remove built-in role groups.

If the ManagedBy property has been populated with role group managers, the user removing the role group must be a role group manager. Alternately, if the user is a member of the Organization Management role group or is directly or indirectly assigned the Role Management role, the BypassSecurityGroupManagerCheck switch can be used to override the security group management check.

For more information about role groups, see Understanding Management Role Groups.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Role groups" entry in the Role Management Permissions topic.

!!! Exchange Server 2013

When you remove a role group, all the management role assignments assigned management roles to the role group are also removed. The management roles aren't removed. Members of a removed role group can no longer manage a feature if the role group was the only means by which they were granted access to the feature.

You can't remove built-in role groups.

If the ManagedBy property has been populated with role group managers, the user removing the role group must be a role group manager. Alternately, if the user is a member of the Organization Management role group or is directly or indirectly assigned the Role Management role, the BypassSecurityGroupManagerCheck switch can be used to override the security group management check.

For more information about role groups, see Understanding management role groups.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Role groups" entry in the Role management permissions topic.

!!! Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

When you remove a role group, all the management role assignments assigned management roles to the role group are also removed. The management roles aren't removed. Members of a removed role group can no longer manage a feature if the role group was the only means by which they were granted access to the feature.

You can't remove built-in role groups.

If the ManagedBy property has been populated with role group managers, the user removing the role group must be a role group manager. Alternately, if the user is a member of the Organization Management role group or is directly or indirectly assigned the Role Management role, the BypassSecurityGroupManagerCheck switch can be used to override the security group management check.

For more information about role groups, see Understanding management role groups.

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Remove-RoleGroup "Training Administrators"
```

This example removes the Training Administrators role group.

### Example 1 -------------------------- (Exchange Server 2013)
```
Remove-RoleGroup "Training Administrators"
```

This example removes the Training Administrators role group.

### Example 1 -------------------------- (Exchange Server 2016)
```
Remove-RoleGroup "Training Administrators"
```

This example removes the Training Administrators role group.

### Example 1 -------------------------- (Exchange Online)
```
Remove-RoleGroup "Training Administrators"
```

This example removes the Training Administrators role group.

### Example 1 -------------------------- (Office 365 Security & Compliance Center)
```
Remove-RoleGroup "Training Administrators"
```

This example removes the Training Administrators role group.

### Example 1 -------------------------- (Exchange Online Protection)
```
Remove-RoleGroup "Training Administrators"
```

This example removes the Training Administrators role group.

### Example 2 -------------------------- (Exchange Server 2010)
```
Remove-RoleGroup "Vancouver Recipient Administrators" -BypassSecurityGroupManagerCheck
```

This example removes the Vancouver Recipient Administrators role group. Because the user running the command wasn't added to the ManagedBy property of the role group, the BypassSecurityGroupManagerCheck switch must be used. The user is assigned the Role Management role, which enables the user to bypass the security group manager check.

### Example 2 -------------------------- (Exchange Server 2013)
```
Remove-RoleGroup "Vancouver Recipient Administrators" -BypassSecurityGroupManagerCheck
```

This example removes the Vancouver Recipient Administrators role group. Because the user running the command wasn't added to the ManagedBy property of the role group, the BypassSecurityGroupManagerCheck switch must be used. The user is assigned the Role Management role, which enables the user to bypass the security group manager check.

### Example 2 -------------------------- (Exchange Server 2016)
```
Remove-RoleGroup "Vancouver Recipient Administrators" -BypassSecurityGroupManagerCheck
```

This example removes the Vancouver Recipient Administrators role group. Because the user running the command wasn't added to the ManagedBy property of the role group, the BypassSecurityGroupManagerCheck switch must be used. The user is assigned the Role Management role, which enables the user to bypass the security group manager check.

### Example 2 -------------------------- (Exchange Online)
```
Remove-RoleGroup "Vancouver Recipient Administrators" -BypassSecurityGroupManagerCheck
```

This example removes the Vancouver Recipient Administrators role group. Because the user running the command wasn't added to the ManagedBy property of the role group, the BypassSecurityGroupManagerCheck switch must be used. The user is assigned the Role Management role, which enables the user to bypass the security group manager check.

### Example 2 -------------------------- (Office 365 Security & Compliance Center)
```
Remove-RoleGroup "Vancouver Recipient Administrators" -BypassSecurityGroupManagerCheck
```

This example removes the Vancouver Recipient Administrators role group. Because the user running the command wasn't added to the ManagedBy property of the role group, the BypassSecurityGroupManagerCheck switch must be used. The user is assigned the Role Management role, which enables the user to bypass the security group manager check.

### Example 2 -------------------------- (Exchange Online Protection)
```
Remove-RoleGroup "Vancouver Recipient Administrators" -BypassSecurityGroupManagerCheck
```

This example removes the Vancouver Recipient Administrators role group. Because the user running the command wasn't added to the ManagedBy property of the role group, the BypassSecurityGroupManagerCheck switch must be used. The user is assigned the Role Management role, which enables the user to bypass the security group manager check.

## PARAMETERS

### -Identity
The Identity parameter specifies the role group to remove. If the role group name contains spaces, enclose the name in quotation marks (").

```yaml
Type: RoleGroupIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

Required: True
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -BypassSecurityGroupManagerCheck
The BypassSecurityGroupManagerCheck switch enables a user who hasn't been added to the ManagedBy property to remove a role group. The user must be a member of the Organization Management role group or be assigned, either directly or indirectly, the Role Management role.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
!!! Exchange Server 2010, Exchange Server 2013

The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-* and Set-* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.



!!! Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
!!! Exchange Server 2010

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

This parameter is available only in on-premises Exchange.

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.



```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
!!! Exchange Server 2010

This parameter is available for multi-tenant deployments. It isn't available for on-premises deployments. For more information about multi-tenant deployments, see Multi-Tenant Support.

The Force switch specifies whether to suppress warning or confirmation messages. This switch can be used when the task is run programmatically and prompting for administrative input is inappropriate. If the Force switch isn't provided in the command, you're prompted for administrative input. You don't have to specify a value with this parameter.



!!! Exchange Server 2013

The Force switch specifies whether to suppress warning or confirmation messages. This switch can be used when the task is run programmatically and prompting for administrative input is inappropriate. If the Force switch isn't provided in the command, you're prompted for administrative input. You don't have to specify a value with this parameter.



!!! Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

The Force switch specifies whether to suppress warning or confirmation messages. You can use this switch to run tasks programmatically where prompting for administrative input is inappropriate. You don't need to specify a value with this switch.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
!!! Exchange Server 2010, Exchange Server 2013

The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.



!!! Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

This parameter doesn't work in the Office 365 Security & Compliance Center.

The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online, Office 365 Security & Compliance Center, Exchange Online Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/6fe6975b-bc0f-4920-b0b0-6da245429f64.aspx)
