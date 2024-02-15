# Pets
(*Pets*)

### Available Operations

* [CreatePets](#createpets) - Create a pet
* [ListPets](#listpets) - List all pets
* [ShowPetByID](#showpetbyid) - Info for a specific pet

## CreatePets

Create a pet

### Example Usage

```go
package main

import(
	demospecopenapi "github.com/speakeasy-sdks/demo-spec-openapi"
	"context"
	"github.com/speakeasy-sdks/demo-spec-openapi/pkg/models/shared"
	"log"
	"net/http"
)

func main() {
    s := demospecopenapi.New()

    ctx := context.Background()
    res, err := s.Pets.CreatePets(ctx, shared.Pet{
        ID: 596804,
        Name: "<value>",
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

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `request`                                             | [shared.Pet](../../pkg/models/shared/pet.md)          | :heavy_check_mark:                                    | The request object to use for the request.            |


### Response

**[*operations.CreatePetsResponse](../../pkg/models/operations/createpetsresponse.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## ListPets

List all pets

### Example Usage

```go
package main

import(
	demospecopenapi "github.com/speakeasy-sdks/demo-spec-openapi"
	"context"
	"github.com/speakeasy-sdks/demo-spec-openapi/pkg/models/operations"
	"log"
)

func main() {
    s := demospecopenapi.New()

    ctx := context.Background()
    res, err := s.Pets.ListPets(ctx, operations.ListPetsRequest{})
    if err != nil {
        log.Fatal(err)
    }

    if res.Pets != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                    | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `ctx`                                                                        | [context.Context](https://pkg.go.dev/context#Context)                        | :heavy_check_mark:                                                           | The context to use for the request.                                          |
| `request`                                                                    | [operations.ListPetsRequest](../../pkg/models/operations/listpetsrequest.md) | :heavy_check_mark:                                                           | The request object to use for the request.                                   |


### Response

**[*operations.ListPetsResponse](../../pkg/models/operations/listpetsresponse.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## ShowPetByID

Info for a specific pet

### Example Usage

```go
package main

import(
	demospecopenapi "github.com/speakeasy-sdks/demo-spec-openapi"
	"context"
	"github.com/speakeasy-sdks/demo-spec-openapi/pkg/models/operations"
	"log"
)

func main() {
    s := demospecopenapi.New()

    ctx := context.Background()
    res, err := s.Pets.ShowPetByID(ctx, operations.ShowPetByIDRequest{
        PetID: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }

    if res.Pet != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                          | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `ctx`                                                                              | [context.Context](https://pkg.go.dev/context#Context)                              | :heavy_check_mark:                                                                 | The context to use for the request.                                                |
| `request`                                                                          | [operations.ShowPetByIDRequest](../../pkg/models/operations/showpetbyidrequest.md) | :heavy_check_mark:                                                                 | The request object to use for the request.                                         |


### Response

**[*operations.ShowPetByIDResponse](../../pkg/models/operations/showpetbyidresponse.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |
