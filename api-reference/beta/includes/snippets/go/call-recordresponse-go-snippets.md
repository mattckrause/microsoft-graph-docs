---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := msgraphsdk.New()
bargeInAllowed := true
requestBody.SetBargeInAllowed(&bargeInAllowed)
clientContext := "d45324c1-fcb5-430a-902c-f20af696537c"
requestBody.SetClientContext(&clientContext)
requestBody.SetPrompts( []Prompt {
	msgraphsdk.NewPrompt(),
	SetAdditionalData(map[string]interface{}{
		"@odata.type": "#microsoft.graph.mediaPrompt",
	}
}
maxRecordDurationInSeconds := int32(10)
requestBody.SetMaxRecordDurationInSeconds(&maxRecordDurationInSeconds)
initialSilenceTimeoutInSeconds := int32(5)
requestBody.SetInitialSilenceTimeoutInSeconds(&initialSilenceTimeoutInSeconds)
maxSilenceTimeoutInSeconds := int32(2)
requestBody.SetMaxSilenceTimeoutInSeconds(&maxSilenceTimeoutInSeconds)
playBeep := true
requestBody.SetPlayBeep(&playBeep)
requestBody.SetStopTones( []String {
	"#",
	"1",
	"*",
}
callId := "call-id"
result, err := graphClient.Communications().CallsById(&callId).RecordResponse(call-id).Post(requestBody)


```