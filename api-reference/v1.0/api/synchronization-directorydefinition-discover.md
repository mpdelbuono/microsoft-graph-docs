---
title: "directoryDefinition: discover"
description: "Discover the latest schema definition for provisioning to an application. "
ms.localizationpriority: medium
author: "ArvindHarinder1"
ms.prod: "applications"
doc_type: "apiPageType"
---

# directoryDefinition: discover

Namespace: microsoft.graph

Discover the latest schema definition for provisioning to an application. 

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "synchronization_directorydefinition_discover" } -->
[!INCLUDE [permissions-table](../includes/permissions/synchronization-directorydefinition-discover-permissions.md)]

[!INCLUDE [rbac-synchronization-apis](../includes/rbac-for-apis/rbac-synchronization-apis.md)]

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
POST /servicePrincipals/{id}/synchronization/jobs/{jobId}/schema/directories/{directoryId}/discover
```

## Request headers

| Header        | Value                      |
|:--------------|:---------------------------|
| Authorization | Bearer {token} (required)  |

## Request body

Do not supply a request body for this method. 

## Response

If successful, this method returns a `200 OK` response with a [directoryDefinition](../resources/synchronization-directorydefinition.md) object.

## Example

### Request
The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "discover_directorydefinition"
}-->
```http
POST https://graph.microsoft.com/v1.0/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema/directories/{directoryId}/discover
```


### Response

The following is an example of a response.

>**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryDefinition"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "discoverabilities": "AttributeNames, AttributeDataTypes",
  "discoveryDateTime": "2019-03-20T15:47:50.4707552Z",
  "id": "directoryDefinitionId",
  "objects": [{
        "name": "User",
        "attributes": [{
                "name": "Id",
                "type": "String"
            }, {
                "name": "FirstName",
                "type": "String"
            },
            {
                "name": "CustomExendedAttribute",
                "type": "String"
            }  
        ]
    }],
  "version": "bf8c03ac-d45e-47fe-b3a1-711a9418b2b1"
}
 ```


