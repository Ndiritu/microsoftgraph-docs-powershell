---
external help file: Microsoft.Graph.Identity.SignIns-help.xml
Module Name: Microsoft.Graph.Identity.SignIns
online version: https://learn.microsoft.com/powershell/module/microsoft.graph.identity.signins/new-mgpolicycrosstenantaccesspolicypartner
schema: 2.0.0
---

# New-MgPolicyCrossTenantAccessPolicyPartner

## SYNOPSIS
Create a new partner configuration in a cross-tenant access policy.

> [!NOTE]
> To view the beta release of this cmdlet, view [New-MgBetaPolicyCrossTenantAccessPolicyPartner](/powershell/module/Microsoft.Graph.Beta.Identity.SignIns/New-MgBetaPolicyCrossTenantAccessPolicyPartner?view=graph-powershell-beta)

## SYNTAX

### CreateExpanded (Default)
```
New-MgPolicyCrossTenantAccessPolicyPartner [-ResponseHeadersVariable <String>]
 [-AdditionalProperties <Hashtable>]
 [-AutomaticUserConsentSettings <IMicrosoftGraphInboundOutboundPolicyConfiguration>]
 [-B2BCollaborationInbound <IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>]
 [-B2BCollaborationOutbound <IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>]
 [-B2BDirectConnectInbound <IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>]
 [-B2BDirectConnectOutbound <IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>]
 [-IdentitySynchronization <IMicrosoftGraphCrossTenantIdentitySyncPolicyPartner>]
 [-InboundTrust <IMicrosoftGraphCrossTenantAccessPolicyInboundTrust>] [-IsServiceProvider] [-TenantId <String>]
 [-Headers <IDictionary>] [-ProgressAction <ActionPreference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Create
```
New-MgPolicyCrossTenantAccessPolicyPartner
 -BodyParameter <IMicrosoftGraphCrossTenantAccessPolicyConfigurationPartner>
 [-ResponseHeadersVariable <String>] [-Headers <IDictionary>] [-ProgressAction <ActionPreference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Create a new partner configuration in a cross-tenant access policy.

## EXAMPLES
### Example 1: Code snippet

```powershell
Import-Module Microsoft.Graph.Identity.SignIns

$params = @{
	tenantId = "3d0f5dec-5d3d-455c-8016-e2af1ae4d31a"
	b2bDirectConnectOutbound = @{
		usersAndGroups = @{
			accessType = "blocked"
			targets = @(
				@{
					target = "6f546279-4da5-4b53-a095-09ea0cef9971"
					targetType = "group"
				}
			)
		}
	}
	b2bDirectConnectInbound = @{
		applications = @{
			accessType = "allowed"
			targets = @(
				@{
					target = "Office365"
					targetType = "application"
				}
			)
		}
	}
}

New-MgPolicyCrossTenantAccessPolicyPartner -BodyParameter $params
```
This example shows how to use the New-MgPolicyCrossTenantAccessPolicyPartner Cmdlet.

To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).


## PARAMETERS

### -AdditionalProperties
Additional Parameters

```yaml
Type: Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticUserConsentSettings
inboundOutboundPolicyConfiguration
To construct, see NOTES section for AUTOMATICUSERCONSENTSETTINGS properties and create a hash table.

```yaml
Type: IMicrosoftGraphInboundOutboundPolicyConfiguration
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -B2BCollaborationInbound
crossTenantAccessPolicyB2BSetting
To construct, see NOTES section for B2BCOLLABORATIONINBOUND properties and create a hash table.

```yaml
Type: IMicrosoftGraphCrossTenantAccessPolicyB2BSetting
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -B2BCollaborationOutbound
crossTenantAccessPolicyB2BSetting
To construct, see NOTES section for B2BCOLLABORATIONOUTBOUND properties and create a hash table.

```yaml
Type: IMicrosoftGraphCrossTenantAccessPolicyB2BSetting
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -B2BDirectConnectInbound
crossTenantAccessPolicyB2BSetting
To construct, see NOTES section for B2BDIRECTCONNECTINBOUND properties and create a hash table.

```yaml
Type: IMicrosoftGraphCrossTenantAccessPolicyB2BSetting
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -B2BDirectConnectOutbound
crossTenantAccessPolicyB2BSetting
To construct, see NOTES section for B2BDIRECTCONNECTOUTBOUND properties and create a hash table.

```yaml
Type: IMicrosoftGraphCrossTenantAccessPolicyB2BSetting
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BodyParameter
crossTenantAccessPolicyConfigurationPartner
To construct, see NOTES section for BODYPARAMETER properties and create a hash table.

```yaml
Type: IMicrosoftGraphCrossTenantAccessPolicyConfigurationPartner
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Headers
Optional headers that will be added to the request.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IdentitySynchronization
crossTenantIdentitySyncPolicyPartner
To construct, see NOTES section for IDENTITYSYNCHRONIZATION properties and create a hash table.

```yaml
Type: IMicrosoftGraphCrossTenantIdentitySyncPolicyPartner
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InboundTrust
crossTenantAccessPolicyInboundTrust
To construct, see NOTES section for INBOUNDTRUST properties and create a hash table.

```yaml
Type: IMicrosoftGraphCrossTenantAccessPolicyInboundTrust
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsServiceProvider
Identifies whether the partner-specific configuration is a Cloud Service Provider for your organization.

```yaml
Type: SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgressAction
{{ Fill ProgressAction Description }}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: proga

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResponseHeadersVariable
Optional Response Headers Variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RHV

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
The tenant identifier for the partner Microsoft Entra organization.
Read-only.
Key.

```yaml
Type: String
Parameter Sets: CreateExpanded
Aliases:

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Graph.PowerShell.Models.IMicrosoftGraphCrossTenantAccessPolicyConfigurationPartner
### System.Collections.IDictionary
## OUTPUTS

### Microsoft.Graph.PowerShell.Models.IMicrosoftGraphCrossTenantAccessPolicyConfigurationPartner
## NOTES
COMPLEX PARAMETER PROPERTIES

To create the parameters described below, construct a hash table containing the appropriate properties.
For information on hash tables, run Get-Help about_Hash_Tables.

AUTOMATICUSERCONSENTSETTINGS `<IMicrosoftGraphInboundOutboundPolicyConfiguration>`: inboundOutboundPolicyConfiguration
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[InboundAllowed <Boolean?>]`: Defines whether external users coming inbound are allowed.
  - `[OutboundAllowed <Boolean?>]`: Defines whether internal users are allowed to go outbound.

B2BCOLLABORATIONINBOUND `<IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>`: crossTenantAccessPolicyB2BSetting
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[Applications <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[AccessType <String>]`: crossTenantAccessPolicyTargetConfigurationAccessType
    - `[Targets <IMicrosoftGraphCrossTenantAccessPolicyTarget- `[]`>]`: Specifies whether to target users, groups, or applications with this rule.
      - `[Target <String>]`: The unique identifier of the user, group, or application; one of the following keywords: AllUsers and AllApplications; or for targets that are applications, you may use reserved values.
      - `[TargetType <String>]`: crossTenantAccessPolicyTargetType
  - `[UsersAndGroups <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration

B2BCOLLABORATIONOUTBOUND `<IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>`: crossTenantAccessPolicyB2BSetting
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[Applications <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[AccessType <String>]`: crossTenantAccessPolicyTargetConfigurationAccessType
    - `[Targets <IMicrosoftGraphCrossTenantAccessPolicyTarget- `[]`>]`: Specifies whether to target users, groups, or applications with this rule.
      - `[Target <String>]`: The unique identifier of the user, group, or application; one of the following keywords: AllUsers and AllApplications; or for targets that are applications, you may use reserved values.
      - `[TargetType <String>]`: crossTenantAccessPolicyTargetType
  - `[UsersAndGroups <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration

B2BDIRECTCONNECTINBOUND `<IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>`: crossTenantAccessPolicyB2BSetting
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[Applications <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[AccessType <String>]`: crossTenantAccessPolicyTargetConfigurationAccessType
    - `[Targets <IMicrosoftGraphCrossTenantAccessPolicyTarget- `[]`>]`: Specifies whether to target users, groups, or applications with this rule.
      - `[Target <String>]`: The unique identifier of the user, group, or application; one of the following keywords: AllUsers and AllApplications; or for targets that are applications, you may use reserved values.
      - `[TargetType <String>]`: crossTenantAccessPolicyTargetType
  - `[UsersAndGroups <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration

B2BDIRECTCONNECTOUTBOUND `<IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>`: crossTenantAccessPolicyB2BSetting
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[Applications <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[AccessType <String>]`: crossTenantAccessPolicyTargetConfigurationAccessType
    - `[Targets <IMicrosoftGraphCrossTenantAccessPolicyTarget- `[]`>]`: Specifies whether to target users, groups, or applications with this rule.
      - `[Target <String>]`: The unique identifier of the user, group, or application; one of the following keywords: AllUsers and AllApplications; or for targets that are applications, you may use reserved values.
      - `[TargetType <String>]`: crossTenantAccessPolicyTargetType
  - `[UsersAndGroups <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration

BODYPARAMETER `<IMicrosoftGraphCrossTenantAccessPolicyConfigurationPartner>`: crossTenantAccessPolicyConfigurationPartner
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[AutomaticUserConsentSettings <IMicrosoftGraphInboundOutboundPolicyConfiguration>]`: inboundOutboundPolicyConfiguration
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[InboundAllowed <Boolean?>]`: Defines whether external users coming inbound are allowed.
    - `[OutboundAllowed <Boolean?>]`: Defines whether internal users are allowed to go outbound.
  - `[B2BCollaborationInbound <IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>]`: crossTenantAccessPolicyB2BSetting
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[Applications <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration
      - `[(Any) <Object>]`: This indicates any property can be added to this object.
      - `[AccessType <String>]`: crossTenantAccessPolicyTargetConfigurationAccessType
      - `[Targets <IMicrosoftGraphCrossTenantAccessPolicyTarget- `[]`>]`: Specifies whether to target users, groups, or applications with this rule.
        - `[Target <String>]`: The unique identifier of the user, group, or application; one of the following keywords: AllUsers and AllApplications; or for targets that are applications, you may use reserved values.
        - `[TargetType <String>]`: crossTenantAccessPolicyTargetType
    - `[UsersAndGroups <IMicrosoftGraphCrossTenantAccessPolicyTargetConfiguration>]`: crossTenantAccessPolicyTargetConfiguration
  - `[B2BCollaborationOutbound <IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>]`: crossTenantAccessPolicyB2BSetting
  - `[B2BDirectConnectInbound <IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>]`: crossTenantAccessPolicyB2BSetting
  - `[B2BDirectConnectOutbound <IMicrosoftGraphCrossTenantAccessPolicyB2BSetting>]`: crossTenantAccessPolicyB2BSetting
  - `[IdentitySynchronization <IMicrosoftGraphCrossTenantIdentitySyncPolicyPartner>]`: crossTenantIdentitySyncPolicyPartner
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[DisplayName <String>]`: Display name for the cross-tenant user synchronization policy.
Use the name of the partner Microsoft Entra tenant to easily identify the policy.
Optional.
    - `[TenantId <String>]`: Tenant identifier for the partner Microsoft Entra organization.
Read-only.
    - `[UserSyncInbound <IMicrosoftGraphCrossTenantUserSyncInbound>]`: crossTenantUserSyncInbound
      - `[(Any) <Object>]`: This indicates any property can be added to this object.
      - `[IsSyncAllowed <Boolean?>]`: Defines whether user objects should be synchronized from the partner tenant.
false causes any current user synchronization from the source tenant to the target tenant to stop.
This property has no impact on existing users who have already been synchronized.
  - `[InboundTrust <IMicrosoftGraphCrossTenantAccessPolicyInboundTrust>]`: crossTenantAccessPolicyInboundTrust
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[IsCompliantDeviceAccepted <Boolean?>]`: Specifies whether compliant devices from external Microsoft Entra organizations are trusted.
    - `[IsHybridAzureAdJoinedDeviceAccepted <Boolean?>]`: Specifies whether Microsoft Entra hybrid joined devices from external Microsoft Entra organizations are trusted.
    - `[IsMfaAccepted <Boolean?>]`: Specifies whether MFA from external Microsoft Entra organizations is trusted.
  - `[IsServiceProvider <Boolean?>]`: Identifies whether the partner-specific configuration is a Cloud Service Provider for your organization.
  - `[TenantId <String>]`: The tenant identifier for the partner Microsoft Entra organization.
Read-only.
Key.

IDENTITYSYNCHRONIZATION `<IMicrosoftGraphCrossTenantIdentitySyncPolicyPartner>`: crossTenantIdentitySyncPolicyPartner
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[DisplayName <String>]`: Display name for the cross-tenant user synchronization policy.
Use the name of the partner Microsoft Entra tenant to easily identify the policy.
Optional.
  - `[TenantId <String>]`: Tenant identifier for the partner Microsoft Entra organization.
Read-only.
  - `[UserSyncInbound <IMicrosoftGraphCrossTenantUserSyncInbound>]`: crossTenantUserSyncInbound
    - `[(Any) <Object>]`: This indicates any property can be added to this object.
    - `[IsSyncAllowed <Boolean?>]`: Defines whether user objects should be synchronized from the partner tenant.
false causes any current user synchronization from the source tenant to the target tenant to stop.
This property has no impact on existing users who have already been synchronized.

INBOUNDTRUST `<IMicrosoftGraphCrossTenantAccessPolicyInboundTrust>`: crossTenantAccessPolicyInboundTrust
  - `[(Any) <Object>]`: This indicates any property can be added to this object.
  - `[IsCompliantDeviceAccepted <Boolean?>]`: Specifies whether compliant devices from external Microsoft Entra organizations are trusted.
  - `[IsHybridAzureAdJoinedDeviceAccepted <Boolean?>]`: Specifies whether Microsoft Entra hybrid joined devices from external Microsoft Entra organizations are trusted.
  - `[IsMfaAccepted <Boolean?>]`: Specifies whether MFA from external Microsoft Entra organizations is trusted.

## RELATED LINKS

[https://learn.microsoft.com/powershell/module/microsoft.graph.identity.signins/new-mgpolicycrosstenantaccesspolicypartner](https://learn.microsoft.com/powershell/module/microsoft.graph.identity.signins/new-mgpolicycrosstenantaccesspolicypartner)

[https://learn.microsoft.com/graph/api/crosstenantaccesspolicy-post-partners?view=graph-rest-1.0](https://learn.microsoft.com/graph/api/crosstenantaccesspolicy-post-partners?view=graph-rest-1.0)




