---
title: "Get hostPair"
description: "Read the properties and relationships of a hostPair object."
author: "jakedavies-microsoft"
ms.localizationpriority: medium
ms.prod: "security"
doc_type: apiPageType
---

# Get hostPair
Namespace: microsoft.graph.security

[!INCLUDE [threatintelligence-api-disclaimer](../../includes/threatintelligence-api-disclaimer.md)]

Read the properties and relationships of a [hostPair](../resources/security-hostpair.md) object.

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|ThreatIntelligence.Read.All.|
|Delegated (personal Microsoft account)|Not supported.|
|Application|ThreatIntelligence.Read.All.|

## HTTP request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /security/threatIntelligence/hostPairs/{hostPairId}
```

## Optional query parameters
This method supports the `$select` OData query parameter to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

The following properties can be used for `$select` calls.

|Property|Example|Notes|
|:---|:---|:---|
|All [hostPair](../resources/security-hostpair.md) properties|`$select=id,firstSeenDateTime`|Use the name as it appears in the [hostPair](../resources/security-hostpair.md) resource.|
|parentHost|`$select=parentHost`|Does not support selecting on nested properties (for example `parentHost/id`).|
|childHost|`$select=childHost`|Does not support selecting on nested properties (for example `childHost/id`).|

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a [microsoft.graph.security.hostPair](../resources/security-hostpair.md) object in the response body.

## Examples

### Request
The following is an example of a request.
# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_hostpair",
  "sampleKeys": ["ZmluYWxSZWRpcmVjdCQkY29udG9zby5jb20kJGNvbnRvc28uY29tJCRjb250b3NvLmNvbQ=="]
}
-->
``` http
GET https://graph.microsoft.com/v1.0/security/threatIntelligence/hostPairs/ZmluYWxSZWRpcmVjdCQkY29udG9zby5jb20kJGNvbnRvc28uY29tJCRjb250b3NvLmNvbQ==
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-hostpair-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/get-hostpair-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/get-hostpair-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-hostpair-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-hostpair-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/get-hostpair-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/get-hostpair-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/get-hostpair-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

---

### Response
The following is an example of the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security.hostPair"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "microsoft.graph.security.hostPair",
  "id": "ZmluYWxSZWRpcmVjdCQkY29udG9zby5jb20kJGNvbnRvc28uY29tJCRjb250b3NvLmNvbQ==",
  "firstSeenDateTime": "2022-05-11T01:27:14.187Z",
  "lastSeenDateTime": "2023-06-23T06:33:31.493Z",
  "linkKind": "finalRedirect",
  "parentHost": {
      "id": "contoso.com"
  },
  "childHost": {
      "id": "contoso.com"
  }
}
```

