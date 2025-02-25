---
title: "agreementAcceptance resource type"
description: "Represents the current status of a user within scope of a company's customizable terms of use powered by Azure Active Directory (Azure AD)."
ms.localizationpriority: medium
doc_type: resourcePageType
ms.prod: "governance"
author: raprakasMSFT
---

# agreementAcceptance resource type

Namespace: microsoft.graph

Represents the current status of a user's response to a company's customizable terms of use agreement powered by Azure Active Directory (Azure AD).

## Properties
| Property     | Type        | Description |
|:-------------|:------------|:------------|
|agreementFileId|String|The identifier of the agreement file accepted by the user.|
|agreementId|String|The identifier of the agreement.|
|deviceDisplayName|String|The display name of the device used for accepting the agreement.|
|deviceId|String|The unique identifier of the device used for accepting the agreement.|
|deviceOSType|String|The operating system used to accept the agreement.|
|deviceOSVersion|String|The operating system version of the device used to accept the agreement.	|
|expirationDateTime|DateTimeOffset|The expiration date time of the acceptance. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 is `2014-01-01T00:00:00Z`.|
|id|String| The identifier of the agreement acceptance. Read-only.|
|recordedDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 is `2014-01-01T00:00:00Z`.|
|state|string| The state of the agreement acceptance. Possible values are: `accepted`, `declined`. Supports `$filter` (`eq`).|
|userDisplayName|String|Display name of the user when the acceptance was recorded.|
|userEmail|String|Email of the user when the acceptance was recorded.|
|userId|String|The identifier of the user who accepted the agreement.|
|userPrincipalName|String|UPN of the user when the acceptance was recorded.|

## Relationships
None.


## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreementAcceptance"
}-->

```json
{
      "id": "String (identifier)",
      "agreementId": "String",
      "userId": "String",
      "deviceId": "String",
      "deviceDisplayName": "String",
      "deviceOSType": "String",
      "deviceOSVersion": "String",
      "agreementFileId": "String",
      "userDisplayName": "String",
      "userPrincipalName": "String",
      "userEmail": "String",
      "recordedDateTime": "String (timestamp)",
      "expirationDateTime": "String",
      "state": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "agreementAcceptance resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


