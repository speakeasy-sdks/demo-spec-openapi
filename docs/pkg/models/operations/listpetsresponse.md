# ListPetsResponse


## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `ContentType`                                           | *string*                                                | :heavy_check_mark:                                      | HTTP response content type for this operation           |
| `Error`                                                 | [*shared.Error](../../../pkg/models/shared/error.md)    | :heavy_minus_sign:                                      | unexpected error                                        |
| `Headers`                                               | map[string][]*string*                                   | :heavy_check_mark:                                      | N/A                                                     |
| `Pets`                                                  | [][shared.Pet](../../../pkg/models/shared/pet.md)       | :heavy_minus_sign:                                      | A paged array of pets                                   |
| `StatusCode`                                            | *int*                                                   | :heavy_check_mark:                                      | HTTP response status code for this operation            |
| `RawResponse`                                           | [*http.Response](https://pkg.go.dev/net/http#Response)  | :heavy_check_mark:                                      | Raw HTTP response; suitable for custom response parsing |