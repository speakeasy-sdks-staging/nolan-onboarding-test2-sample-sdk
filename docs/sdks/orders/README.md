# Orders
(*Orders*)

## Overview

The orders endpoints.

### Available Operations

* [CreateOrder](#createorder) - Create an order.

## CreateOrder

Create an order for a drink.

### Example Usage

```go
package main

import(
	"context"
	"log"
	nolanonboardingtest2samplesdk "github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk"
	"github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk/pkg/models/shared"
	"github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk/pkg/models/operations"
	"github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk/pkg/models/callbacks"
)

func main() {
    s := nolanonboardingtest2samplesdk.New(
        nolanonboardingtest2samplesdk.WithSecurity(""),
    )

    ctx := context.Background()
    res, err := s.Orders.CreateOrder(ctx, operations.CreateOrderRequest{
        RequestBody: []shared.OrderInput{
            shared.OrderInput{
                ProductCode: "APM-1F2D3",
                Quantity: 26535,
                Type: shared.OrderTypeDrink,
            },
        },
    })
    if err != nil {
        log.Fatal(err)
    }

    if res.Order != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `ctx`                                                                          | [context.Context](https://pkg.go.dev/context#Context)                          | :heavy_check_mark:                                                             | The context to use for the request.                                            |
| `request`                                                                      | [operations.CreateOrderRequest](../../models/operations/createorderrequest.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |


### Response

**[*operations.CreateOrderResponse](../../models/operations/createorderresponse.md), error**

