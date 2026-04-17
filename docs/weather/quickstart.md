# Quickstart

This guide will get you connected to the Jones Center Weather API from R in a few minutes.

## Prerequisites

You will need:

- R 4.4 or higher
- Positron or RStudio
- A `@jonesctr.org` account with API access — contact [it@jonesctr.org](mailto:it@jonesctr.org) to request access

## Install Required Packages

Run this in your R console:

```r
install.packages(c("AzureAuth", "httr2"))
```

## Authenticate

Copy and run this code block. A browser window will open — sign in with your `@jonesctr.org` account. The token is cached locally so you only need to do this once per session.

```r
library(AzureAuth)
library(httr2)

token <- get_azure_token(
  resource  = "e3ab7f68-9182-412e-bcf3-760e6ba333bc",
  tenant    = "d1f21831-a420-4b90-a1bd-be2d7f4025e1",
  app       = "e3ab7f68-9182-412e-bcf3-760e6ba333bc",
  auth_type = "authorization_code"
)
```

## Make Your First API Call

```r
response <- request("https://api.jonesctr.org/weather/api/CraftonWS_FifteenMin") |>
  req_auth_bearer_token(token$access_token) |>
  req_headers("X-MS-API-ROLE" = "WeatherAPI.Read") |>
  req_url_query(`$top` = 10, `$orderby` = "TmStamp desc") |>
  req_perform() |>
  resp_body_json()
```

This returns the 10 most recent 15-minute readings ordered by timestamp.

## Next Steps

- See the [API Reference](api-reference.md) for all available endpoints and query parameters
- See the [Data Dictionary](data-dictionary.md) for column definitions and units
