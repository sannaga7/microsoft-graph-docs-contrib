---
title: "Remove multiTenantOrganizationMember"
description: "Remove a tenant from a multitenant organization."
author: "rolyon"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# Remove multiTenantOrganizationMember
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Remove a tenant from a multitenant organization. A tenant can be removed in the following scenarios:

* An active member tenant can remove itself.
* An active owner tenant can remove any other tenant.
* An active owner tenant can remove itself as long as there is another active owner tenant remaining.
* An active owner tenant can remove itself as long as there is no other active tenant remaining, thereby deleting the entire multi-tenant organization.

To allow for asynchronous processing, you must wait for **up to 2 hours** before removal of a tenant is completed.

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|MultiTenantOrganization.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|MultiTenantOrganization.ReadWrite.All|

[!INCLUDE [rbac-multitenantorganization-apis-write](../includes/rbac-for-apis/rbac-multitenantorganization-apis-write.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /tenantRelationships/multiTenantOrganization/tenants/{tenantId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

The following example removes a tenant from a multi-tenant organization.

### Request

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_multitenantorganizationmember"
}
-->
``` http
DELETE https://graph.microsoft.com/beta/tenantRelationships/multiTenantOrganization/tenants/5036a0a0-a7a4-4933-9086-5dd54535dd6e
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-multitenantorganizationmember-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/delete-multitenantorganizationmember-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/delete-multitenantorganizationmember-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-multitenantorganizationmember-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-multitenantorganizationmember-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/delete-multitenantorganizationmember-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/delete-multitenantorganizationmember-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/delete-multitenantorganizationmember-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response

<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

