# Pets
(*.Pets*)

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

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |


### Response

**[*operations.CreatePetsResponse](../../models/operations/createpetsresponse.md), error**


## ListPets

List all pets

### Example Usage

```go
package main

import(
	"context"
	"log"
	demospecopenapi "github.com/speakeasy-sdks/demo-spec-openapi"
	"github.com/speakeasy-sdks/demo-spec-openapi/pkg/models/operations"
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

| Parameter                                                                | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `ctx`                                                                    | [context.Context](https://pkg.go.dev/context#Context)                    | :heavy_check_mark:                                                       | The context to use for the request.                                      |
| `request`                                                                | [operations.ListPetsRequest](../../models/operations/listpetsrequest.md) | :heavy_check_mark:                                                       | The request object to use for the request.                               |


### Response

**[*operations.ListPetsResponse](../../models/operations/listpetsresponse.md), error**


## ShowPetByID

Info for a specific pet

### Example Usage

```go
package main

import(
	"context"
	"log"
	demospecopenapi "github.com/speakeasy-sdks/demo-spec-openapi"
	"github.com/speakeasy-sdks/demo-spec-openapi/pkg/models/operations"
)

func main() {
    s := demospecopenapi.New()

    ctx := context.Background()
    res, err := s.Pets.ShowPetByID(ctx, operations.ShowPetByIDRequest{
        PetID: "string",
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

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `ctx`                                                                          | [context.Context](https://pkg.go.dev/context#Context)                          | :heavy_check_mark:                                                             | The context to use for the request.                                            |
| `request`                                                                      | [operations.ShowPetByIDRequest](../../models/operations/showpetbyidrequest.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |


### Response

**[*operations.ShowPetByIDResponse](../../models/operations/showpetbyidresponse.md), error**

