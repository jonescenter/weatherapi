# Weather API

The Jones Center Weather API provides access to real-time and historical weather data from the Crafton Palmer Weather Station at Ichauway. Data is collected by a Campbell Scientific CR1000X datalogger and written to a cloud database every 15 minutes.

## What's Available

| Table | Description | Update Frequency |
|-------|-------------|-----------------|
| CraftonWS_FifteenMin | 15-minute interval sensor readings | Every 15 minutes |
| CraftonWS_Daily | Daily aggregates — min, max, average | Once per day |

## Measurements

The weather station collects the following measurements:

- Air temperature (°C)
- Relative humidity (%)
- Vapour pressure deficit
- Barometric pressure
- Wind speed and direction
- Solar radiation
- Photosynthetically active radiation (PAR)
- Rainfall (mm)
- Soil temperature at 4 inches
- Soil moisture at 4, 8, and 24 inches
- Fine fuel moisture
- Datalogger battery voltage

## API Endpoint
