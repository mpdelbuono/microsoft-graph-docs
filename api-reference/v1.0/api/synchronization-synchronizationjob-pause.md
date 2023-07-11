---
title: "synchronizationJob: pause"
description: "Temporarily stop synchronization. All the progress, including job state, is persisted, and the job will continue from where it left off when a Start call is made."
ms.localizationpriority: medium
doc_type: apiPageType
author: "ArvindHarinder1"
ms.prod: "applications"
---

# synchronizationJob: pause

Namespace: microsoft.graph

Temporarily stop a running synchronization job. All the progress, including job state, is persisted, and the job will continue from where it left off when a [start](../api/synchronization-synchronizationjob-start.md) call is made.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "synchronization_synchronizationjob_pause" } -->
[!INCLUDE [permissions-table](../includes/permissions/synchronization-synchronizationjob-pause-permissions.md)]

[!INCLUDE [rbac-synchronization-apis](../includes/rbac-for-apis/rbac-synchronization-apis.md)]

## HTTP Request
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{jobId}/pause
```

## Request headers

| Name           | Type    | Description|
|:---------------|:--------|:-----------|
| Authorization  | string  | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, returns a `204 No Content` response. It does not return anything in the response body.

## Example

### Request
The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "synchronizationjob_pause"
}-->
```http
POST https://graph.microsoft.com/v1.0/servicePrincipals/{id}/synchronization/jobs/{jobId}/pause
```


### Response
The following is an example of a response.
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 204 No Content
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "synchronizationJob: pause",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->


