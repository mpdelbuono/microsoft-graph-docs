---
title: "synchronization: acquireAccessToken"
description: "Acquire an OAuth Access token to authorize the Azure AD provisioning service to provision users into an application"
author: "ArvindHarinder1"
ms.localizationpriority: medium
ms.prod: "applications"
doc_type: apiPageType
---

# synchronization: acquireAccessToken
Namespace: microsoft.graph

Acquire an OAuth access token to authorize the Azure AD provisioning service to provision users into an application.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "synchronization_synchronization_acquireaccesstoken" } -->
[!INCLUDE [permissions-table](../includes/permissions/synchronization-synchronization-acquireaccesstoken-permissions.md)]

[!INCLUDE [rbac-synchronization-apis](../includes/rbac-for-apis/rbac-synchronization-apis.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /applications/{applicationsId}/synchronization/acquireAccessToken
POST /servicePrincipals/{servicePrincipalsId}/synchronization/acquireAccessToken
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Parameter|Type|Description|
|:---|:---|:---|
|credentials|[synchronizationSecretKeyStringValuePair](../resources/synchronization-synchronizationsecretkeystringvaluepair.md) collection|Represents a single secret value.|



## Response

If successful, this action returns a `204 No Content` response code.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "synchronization_acquireaccesstoken"
}
-->
``` http
POST https://graph.microsoft.com/v1.0/applications/{applicationsId}/synchronization/acquireAccessToken
Content-Type: application/json

{
  "credentials": [
    {
      "@odata.type": "microsoft.graph.synchronizationSecretKeyStringValuePair"
    }
  ]
}
```


### Response
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```


