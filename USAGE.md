<!-- Start SDK Example Usage -->


```go
package main

import (
	"context"
	nolanonboardingtest2samplesdk "github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk"
	"github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk/pkg/models/operations"
	"github.com/speakeasy-sdks-staging/nolan-onboarding-test2-sample-sdk/pkg/models/shared"
	"log"
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
<!-- End SDK Example Usage -->