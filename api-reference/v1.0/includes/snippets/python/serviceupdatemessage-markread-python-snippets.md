---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = MarkReadPostRequestBody(
	message_ids = [
		"MC172851",
		"MC167983",
	]
)

result = await graph_client.admin.service_announcement.messages.mark_read.post(body = request_body)


```