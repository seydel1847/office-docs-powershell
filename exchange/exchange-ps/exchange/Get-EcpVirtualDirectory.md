---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016
schema: 2.0.0
---

# Get-EcpVirtualDirectory

## SYNOPSIS
!!! Exchange Server 2010

Use the Get-EcpVirtualDirectory cmdlet to retrieve all Exchange Control Panel virtual directories on a computer running Microsoft Exchange Server 2010 that has the Client Access server role installed.

!!! Exchange Server 2013

This cmdlet is available only in on-premises Exchange.

Use the Get-EcpVirtualDirectory cmdlet to retrieve all configuration data for Exchange Control Panel (ECP) virtual directories. The ECP virtual directory manages the Exchange Administration Center.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

The ECP is the web-based user interface developed for Microsoft Exchange Server 2010. The Exchange Server 2013Exchange Administration Center cmdlets for virtual directory still use ECP in the name, and the ECP cmdlets can be used to manage Exchange 2010 and Exchange 2013 ECP virtual directories.

!!! Exchange Server 2016

This cmdlet is available only in on-premises Exchange.

Use the Get-EcpVirtualDirectory cmdlet to view Exchange Control Panel (ECP) virtual directories that are used in Internet Information Services (IIS) on Microsoft Exchange servers. The Exchange admin center (EAC) uses the ECP virtual directories.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

The ECP web management interface was introduced in MicrosoftExchange Server 2010. In Exchange Server 2013 and Exchange Server 2016, the EAC virtual directories and the corresponding management cmdlets still use ECP in the name. You can use these cmdlets to manage ECP virtual directories on Exchange 2010, Exchange 2013, and Exchange 2016 servers.

## SYNTAX

### Set2
```
Get-EcpVirtualDirectory -Server <ServerIdParameter> [-ADPropertiesOnly] [-DomainController <Fqdn>]
 [-ShowMailboxVirtualDirectories] [<CommonParameters>]
```

### Set1
```
Get-EcpVirtualDirectory [[-Identity] <VirtualDirectoryIdParameter>] [-ADPropertiesOnly]
 [-DomainController <Fqdn>] [-ShowMailboxVirtualDirectories] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Exchange Control Panel (ECP) virtual directory settings" entry in the Client Access Permissions topic.

!!! Exchange Server 2013

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Exchange Administration Center connectivity" entry in the Exchange and Shell infrastructure permissions topic.

!!! Exchange Server 2016

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Get-EcpVirtualDirectory -Server Server01
```

This example displays the configuration data for the Exchange Control Panel virtual directory on Server01.

### Example 1 -------------------------- (Exchange Server 2013)
```
Get-EcpVirtualDirectory -Server Server01
```

This example displays the configuration data for the Exchange Control Panel virtual directory on Server01.

### Example 1 -------------------------- (Exchange Server 2016)
```
Get-EcpVirtualDirectory -Server Server01
```

This example returns a summary list of all Exchange Control Panel virtual directories on the server named Server01.

### Example 2 -------------------------- (Exchange Server 2016)
```
Get-EcpVirtualDirectory -Identity "Server01\ecp*" | Format-List
```

This example returns detailed information for the Exchange Control Panel virtual directory named "ecp (Default Web Site)" on the server named Server01.

### Example 3 -------------------------- (Exchange Server 2016)
```
Get-EcpVirtualDirectory
```

This example returns a summary list of all Exchange Control Panel virtual directories in the client access services on all Mailbox servers in the organization.

## PARAMETERS

### -Server
!!! Exchange Server 2010

The Server parameter specifies the name or GUID of the server that hosts the Exchange Control Panel virtual directories that you want to display. If you don't specify a value for the Server parameter, all Exchange Control Panel virtual directories are returned.



!!! Exchange Server 2013

The Server parameter specifies the name or GUID of the server that hosts the ECP virtual directories that you want to display. If you don't specify a value for the Server parameter, all ECP virtual directories are returned.



!!! Exchange Server 2016

The Server parameter specifies the Exchange server that hosts the virtual directory. You can use any value that uniquely identifies the server. For example:

- Name

- FQDN

- Distinguished name (DN)

- ExchangeLegacyDN

You can't use the Server and Identity parameters in the same command.



```yaml
Type: ServerIdParameter
Parameter Sets: Set2
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -ADPropertiesOnly
The ADPropertiesOnly switch specifies whether to return only the properties about the virtual directory stored in Active Directory. The properties stored in the Internet Information Services (IIS) metabase aren't returned.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
!!! Exchange Server 2010

The Identity parameter specifies the name or GUID of an Exchange Control Panel virtual directory. The Identity parameter is represented as: ServerName\\ECP (WebsiteName). If you don't specify a server name, the command returns the Exchange Control Panel virtual directory on the local server.



!!! Exchange Server 2013

The Identity parameter specifies the name or GUID of an ECP virtual directory. The Identity parameter is represented as: ServerName\\ECP (WebsiteName). If you don't specify a server name, the command returns the ECP virtual directory on the local server.



!!! Exchange Server 2016

The Identity parameter specifies the virtual directory that you want to view.

You can use any value that uniquely identifies the virtual directory. For example:

- Name or \<Server\>\\Name

- Distinguished name (DN)

- GUID

The Name value uses the syntax "\<VirtualDirectoryName\> (\<WebsiteName\>)" from the properties of the virtual directory. You can specify the wildcard character (\*) instead of the default website by using the syntax \<VirtualDirectoryName\>\*.

You can't use the Identity and Server parameters in the same command.



```yaml
Type: VirtualDirectoryIdParameter
Parameter Sets: Set1
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -ShowMailboxVirtualDirectories
!!! Exchange Server 2013

The ShowMailboxVirtualDirectories switch specifies whether to return the ECP virtual directories that are located on servers running the Mailbox server role. This switch should only be used with the direction of Microsoft support.



!!! Exchange Server 2016

The ShowMailboxVirtualDirectories switch shows information about backend virtual directories on Mailbox servers. You don't need to specify a value with this switch.

By default, this cmdlet shows information about virtual directories in the Client Access services on Mailbox servers. Client connections are proxied from the Client Access services on Mailbox servers to the backend services on Mailbox servers. Clients don't connect directly to the backend services.

We recommend that you use this parameter only under the direction of Microsoft Customer Service and Support.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016

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

[Online Version](https://technet.microsoft.com/library/afa04216-965d-4a6c-949c-170f916e8f4c.aspx)
