# Config
(*Config*)

### Available Operations

* [SubscribeToWebhooks](#subscribetowebhooks) - Subscribe to webhooks.

## SubscribeToWebhooks

Subscribe to webhooks.

### Example Usage

```go
package main

import(
	"context"
	"log"
	nolanonboardingtest2samplesdk "github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk"
	"github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk/pkg/models/shared"
	"github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk/pkg/models/operations"
)

func main() {
    s := nolanonboardingtest2samplesdk.New(
        nolanonboardingtest2samplesdk.WithSecurity(""),
    )

    ctx := context.Background()
    res, err := s.Config.SubscribeToWebhooks(ctx, []operations.SubscribeToWebhooksRequestBody{
        operations.SubscribeToWebhooksRequestBody{},
    })
    if err != nil {
        log.Fatal(err)
    }

    if res.StatusCode == http.StatusOK {
        // handle response
    }
}
```

### Parameters

| Parameter                                                        | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `ctx`                                                            | [context.Context](https://pkg.go.dev/context#Context)            | :heavy_check_mark:                                               | The context to use for the request.                              |
| `request`                                                        | [[]operations.SubscribeToWebhooksRequestBody](../../models//.md) | :heavy_check_mark:                                               | The request object to use for the request.                       |


### Response

**[*operations.SubscribeToWebhooksResponse](../../models/operations/subscribetowebhooksresponse.md), error**

