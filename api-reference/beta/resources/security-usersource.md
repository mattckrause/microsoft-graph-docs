---
title: "userSource resource type"
description: "The container for a user's mailbox and OneDrive for Business site."
author: "SeunginLyu"
ms.localizationpriority: medium
ms.prod: "ediscovery"
doc_type: resourcePageType
---

# userSource resource type

Namespace: microsoft.graph.security

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The container for a user's mailbox and OneDrive for Business site.

Inherits from [dataSource](../resources/security-datasource.md).

## Methods
None. 
## Properties
|Property|Type|Description|
|:---|:---|:---|
|createdBy|[identitySet](../resources/identityset.md)|The user who created the **userSource**.|
|createdDateTime|DateTimeOffset|The date and time the **userSource** was created|
|displayName|String|The display name associated with the mailbox and site.|
|email|String|Email address of the user's mailbox.|
|id|String|The ID of the **userSource**. This is not the ID of the actual group|
|includedSources|String|Specifies which sources are included in this group. Possible values are: `mailbox`, `site`.|
|siteWebUrl|String|The URL of the user's OneDrive for Business site. Read-only.|
|holdStatus|String|The hold status of the **userSource**.The possible values are: `notApplied`, `applied`, `applying`, `removing`, `partial`|
### sourceType values

Types of source related to the user. Includes mailbox and site by default.

|Member|Description|
|:----|-----------|
|mailbox|Represents a mailbox.|
|site|Represents a OneDrive for Business site.|

### userSourceHoldStatus values

|Name|Description|
|:----|-----------|
|notApplied|The userSource is not on Hold (all sources in it are not on hold).|
|applied|The userSource is on Hold (all sources are on hold).|
|applying|The userSource is in applying hold state (applyHold operation triggered).|
|removing|The userSource is in removing the hold state(removeHold operation triggered).|
|partial|The userSource is in mixed state where some sources are on hold and some not on hold or error state.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.security.userSource",
  "baseType": "microsoft.graph.security.dataSource",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.security.userSource",
  "id": "String (identifier)",
  "displayName": "String",
  "holdStatus": "String",
  "createdDateTime": "String (timestamp)",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "email": "String",
  "includedSources": "String",
  "siteWebUrl": "String"
}
```