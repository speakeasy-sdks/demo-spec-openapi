<!-- Start SDK Example Usage [usage] -->
```go
package main

import (
	"context"
	demospecopenapi "github.com/speakeasy-sdks/demo-spec-openapi"
	"github.com/speakeasy-sdks/demo-spec-openapi/pkg/models/shared"
	"log"
)

func main() {
	s := demospecopenapi.New()

	ctx := context.Background()
	res, err := s.Pets.CreatePets(ctx, shared.Pet{
		ID:   596804,
		Name: "<value>",
	})
	if err != nil {
		log.Fatal(err)
	}
	if res != nil {
		// handle response
	}
}

```
<!-- End SDK Example Usage [usage] -->