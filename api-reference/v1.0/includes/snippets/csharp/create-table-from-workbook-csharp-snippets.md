---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.Drives.Item.Items.Item.Workbook.Tables.Add.AddPostRequestBody
{
	Address = "A1:D8",
	HasHeaders = false,
};
var result = await graphClient.Drives["{drive-id}"].Items["{driveItem-id}"].Workbook.Tables.Add.PostAsync(requestBody);


```