# API Reference

The Jones Center Weather API is built on Microsoft Azure Data API Builder and automatically exposes an OpenAPI 3.0 specification. The interactive reference below is generated live from that specification.

## Authentication

All requests require two headers:

| Header | Value |
|--------|-------|
| `Authorization` | `Bearer <token>` — acquired via the [Quickstart](quickstart.md) guide |
| `X-MS-API-ROLE` | `WeatherAPI.Read` |

## Base URL

`https://api.jonesctr.org/weather/api`

## Endpoints

[OAD(https://api.jonesctr.org/weather/api/openapi)]
