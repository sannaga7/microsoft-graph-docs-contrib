---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewCustomCalloutExtension()
additionalData := map[string]interface{}{
value := graphmodels.New()
displayName := "test_action_0127_email"
value.SetDisplayName(&displayName) 
description := "this is for graph testing only"
value.SetDescription(&description) 
endpointConfiguration := graphmodels.New()
subscriptionId := "38ab2ccc-3747-4567-b36b-9478f5602f0d"
endpointConfiguration.SetSubscriptionId(&subscriptionId) 
resourceGroupName := "test"
endpointConfiguration.SetResourceGroupName(&resourceGroupName) 
logicAppWorkflowName := "elm-extension-email"
endpointConfiguration.SetLogicAppWorkflowName(&logicAppWorkflowName) 
	value.SetEndpointConfiguration(endpointConfiguration)
authenticationConfiguration := graphmodels.New()
	value.SetAuthenticationConfiguration(authenticationConfiguration)
	requestBody.SetValue(value)
}
requestBody.SetAdditionalData(additionalData)

customWorkflowExtensions, err := graphClient.IdentityGovernance().EntitlementManagement().Catalogs().ByAccessPackageCatalogId("accessPackageCatalog-id").CustomWorkflowExtensions().Post(context.Background(), requestBody, nil)


```