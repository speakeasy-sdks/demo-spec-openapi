# github.com/speakeasy-sdks/demo-spec-openapi

<!-- Start SDK Installation -->
## SDK Installation

```bash
go get github.com/speakeasy-sdks/demo-spec-openapi
```
<!-- End SDK Installation -->

## SDK Example Usage
<!-- Start SDK Example Usage -->
```go
package main

import(
	"context"
	"log"
	demospecopenapi "github.com/speakeasy-sdks/demo-spec-openapi"
)

func main() {
    s := demospecopenapi.New()

    ctx := context.Background()
    res, err := s.Pets.CreatePets(ctx)
    if err != nil {
        log.Fatal(err)
    }

    if res.StatusCode == http.StatusOK {
        // handle response
    }
}
```
<!-- End SDK Example Usage -->

<!-- Start SDK Available Operations -->
## Available Resources and Operations


### [Pets](docs/sdks/pets/README.md)

* [CreatePets](docs/sdks/pets/README.md#createpets) - Create a pet
* [ListPets](docs/sdks/pets/README.md#listpets) - List all pets
* [ShowPetByID](docs/sdks/pets/README.md#showpetbyid) - Info for a specific pet
<!-- End SDK Available Operations -->



<!-- Start Dev Containers -->

<!-- End Dev Containers -->



<!-- Start Pagination -->
# Pagination

Some of the endpoints in this SDK support pagination. To use pagination, you make your SDK calls as usual, but the
returned response object will have a `Next` method that can be called to pull down the next group of results. If the
return value of `Next` is `nil`, then there are no more pages to be fetched.

Here's an example of one such pagination call:
<!-- End Pagination -->



<!-- Start Go Types -->

<!-- End Go Types -->

<!-- Placeholder for Future Speakeasy SDK Sections -->



### Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

### Contributions

While we value open-source contributions to this SDK, this library is generated programmatically.
Feel free to open a PR or a Github issue as a proof of concept and we'll do our best to include it in a future release!

### SDK Created by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
