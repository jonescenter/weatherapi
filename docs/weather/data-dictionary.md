# Data Dictionary

This page describes all columns available in the Jones Center Weather API. Data is collected by a Campbell Scientific CR1000X datalogger at the Crafton Palmer Weather Station at Ichauway.

---

## CraftonWS_FifteenMin

15-minute interval sensor readings. This is the primary table for analysis and the default table used in the quickstart guide.

| Column | Type | Description | Units |
|--------|------|-------------|-------|
| TmStamp | datetime2 | Timestamp of the observation | UTC |
| RecNum | bigint | LNDB record number | — |
| AirTC_Avg | real | Air temperature average | °C |
| RH | real | Relative humidity | % |
| VPD | real | Vapour pressure deficit | kPa |
| BP_Abs | real | Absolute barometric pressure | hPa |
| WS_ms | real | Wind speed | m/s |
| WS_ms_Max | real | Maximum wind speed | m/s |
| WS_Avg | real | Average wind speed | m/s |
| WD_avg | real | Average wind direction | degrees |
| WD_StdDev | real | Wind direction standard deviation | degrees |
| WS_ms_WVc | real | Wind speed vector component | m/s |
| SlrkW | real | Solar radiation | kW |
| Par_Den | real | Photosynthetically active radiation density | µmol/m²/s |
| Rain_mm_Tot | real | Total rainfall | mm |
| SoilTemp4inches | real | Soil temperature at 4 inches depth | °C |
| SoilMoisture4 | real | Soil moisture at 4 inches depth | % VWC |
| SoilMoisture8 | real | Soil moisture at 8 inches depth | % VWC |
| SoilMoisture24 | real | Soil moisture at 24 inches depth | % VWC |
| FuelM | real | Fine fuel moisture | % |
| BattV | real | Datalogger battery voltage | V |

---

## CraftonWS_Daily

Daily aggregate table. Contains minimum, maximum, and average values for most measurements, along with the timestamp of when the daily extreme occurred.

| Column Group | Columns | Description |
|-------------|---------|-------------|
| Timestamp | TmStamp | Date of the daily aggregate |
| Air Temperature | AirTC_Avg, AirTC_Max, AirTC_TMx, AirTC_Min, AirTC_TMn | Average, max, time of max, min, time of min (°C) |
| Relative Humidity | RH_Avg, RH_Max, RH_TMx, RH_Min, RH_TMn | Average, max, time of max, min, time of min (%) |
| Vapour Pressure Deficit | VPD_Avg, VPD_Max, VPD_TMx, VPD_Min, VPD_TMn | Average, max, time of max, min, time of min (kPa) |
| Barometric Pressure | BP_Abs_Avg, BP_Abs_Max, BP_Abs_TMx, BP_Abs_Min, BP_Abs_TMn | Average, max, time of max, min, time of min (hPa) |
| Wind | WS_ms_Max, WS_ms_TMx, WS_Avg, WD_avg, WD_StdDev, WS_ms_WVc | Max speed, time of max, avg speed, avg direction, std dev, vector component |
| Solar / PAR | SlrkW_Avg, SlrkW_Max, SlrkW_TMx, Par_Tot_Tot, Par_Den_Max, Par_Den_TMx | Solar radiation averages and PAR totals |
| Rainfall | Rain_mm_Tot, max_rain, Rain_TimeofMax | Total rainfall, max rate, time of max (mm) |
| Soil Moisture | SoilMoisture4_Avg, SoilMoisture8_Avg, SoilMoisture24_Avg | Average soil moisture at 4, 8, 24 inches (% VWC) |
| Fuel Moisture | FuelM_Max, FuelM_TMx, FuelM_Min, FuelM_TMn | Max, time of max, min, time of min (%) |

---

## Query Examples

Filter by date range:
