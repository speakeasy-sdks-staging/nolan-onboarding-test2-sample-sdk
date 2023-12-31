# Drinks
(*Drinks*)

## Overview

The drinks endpoints.

### Available Operations

* [GetDrink](#getdrink) - Get a drink.
* [ListDrinks](#listdrinks) - Get a list of drinks.

## GetDrink

Get a drink by name, if authenticated this will include stock levels and product codes otherwise it will only include public information.

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
    res, err := s.Drinks.GetDrink(ctx, operations.GetDrinkRequest{
        Name: "North District",
    })
    if err != nil {
        log.Fatal(err)
    }

    if res.Drink != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `ctx`                                                                    | [context.Context](https://pkg.go.dev/context#Context)                    | :heavy_check_mark:                                                       | The context to use for the request.                                      |
| `request`                                                                | [operations.GetDrinkRequest](../../models/operations/getdrinkrequest.md) | :heavy_check_mark:                                                       | The request object to use for the request.                               |


### Response

**[*operations.GetDrinkResponse](../../models/operations/getdrinkresponse.md), error**


## ListDrinks

Get a list of drinks, if authenticated this will include stock levels and product codes otherwise it will only include public information.

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
    res, err := s.Drinks.ListDrinks(ctx, operations.ListDrinksRequest{})
    if err != nil {
        log.Fatal(err)
    }

    if res.Drinks != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                    | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `ctx`                                                                        | [context.Context](https://pkg.go.dev/context#Context)                        | :heavy_check_mark:                                                           | The context to use for the request.                                          |
| `request`                                                                    | [operations.ListDrinksRequest](../../models/operations/listdrinksrequest.md) | :heavy_check_mark:                                                           | The request object to use for the request.                                   |


### Response

**[*operations.ListDrinksResponse](../../models/operations/listdrinksresponse.md), error**

