# go-holidayapi
Official Go library for [Holiday API](https://holidayapi.pl)

## Usage

```go
package main

import (
    "fmt"
    "github.com/holidayapi-pl/go-holidayapi"
)

func main() {
    hapi := holidayapi.NewV1("_MY_API_KEY_")

    holidays, err := hapi.Holidays(map[string]interface{}{
        // Required
        "country": "PL",
        "year":    "2019",
        // Optional
        // "month":    "7",
        // "day":      "4",
        // "previous": "true",
        // "upcoming": "true",
        // "public":   "true",
        // "pretty":   "true",
    })

    if err != nil {
        // Error handling...
    }

    fmt.Println("%#v\n", holidays)
}

```

