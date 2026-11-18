# Data dictionary: `ohio_counties_acs.gpkg`

One GeoPackage, one layer (`ohio_counties_acs`). The boundaries are the Census Bureau's TIGER/Line county polygons, in EPSG:4269 (NAD83, geographic degrees). The attributes come from the American Community Survey 5-year estimates for 2019 to 2023 (the `ACSDP5Y2023` Data Profile tables), pulled at the county level for Ohio and joined to the polygons on the county FIPS code. There are no missing values.

Columns whose names start with `pct_` are percentages. A value of 37.2 means 37.2 percent, not 0.372. Columns named `median_` are the ACS median for that county. The two area columns are in square kilometers.

| column | ACS table and variable | units | kind | how to read it |
|---|---|---|---|---|
| `geoid` | TIGER `GEOID` | text | identifier | Five-digit state plus county FIPS code, as text with the leading `39`. |
| `name` | TIGER `NAME` | text | identifier | County name without the word "County". |
| `name_long` | TIGER `NAMELSAD` | text | identifier | County name with "County". |
| `aland_km2` | TIGER `ALAND` | km² | value | Land area. |
| `awater_km2` | TIGER `AWATER` | km² | value | Water area. Lake Erie counties have large values here. |
| `total_population` | DP05, `DP05_0001E` | people | count | Total population estimate. |
| `median_age` | DP05, `DP05_0018E` | years | value | Median age of all residents. |
| `pct_age_65_plus` | DP05, `DP05_0024PE` | percent | rate | Share of all residents aged 65 and over. |
| `median_hh_income` | DP03, `DP03_0062E` | dollars (2023) | value | Median household income, inflation-adjusted to 2023 dollars. |
| `pct_poverty` | DP03, `DP03_0119PE` | percent | rate | Share of families whose income in the past 12 months was below the poverty level. |
| `pct_bachelors_plus` | DP02, `DP02_0068PE` | percent | rate | Share of residents aged 25 and over holding a bachelor's degree or higher. |
| `pct_no_vehicle` | DP04, `DP04_0058PE` | percent | rate | Share of occupied housing units with no vehicle available. |

## Which columns to use for spatial autocorrelation

The rates and the values are reasonable choices: `median_age`, `pct_age_65_plus`, `median_hh_income`, `pct_poverty`, `pct_bachelors_plus`, and `pct_no_vehicle`. Each describes a condition of the people or households in a county, independent of how large the county is.

`total_population` is not a good choice. It is a count, and it is driven mostly by county size and by where the big cities are. A Moran's I on population would mostly tell you that Cuyahoga, Franklin, and Hamilton are large, which you already know. If you want a population variable, normalize by area first.

## Source

American Community Survey 2019 to 2023 5-year estimates, Data Profile tables DP02, DP03, DP04, and DP05, accessed through data.census.gov on 2026-11-16. Boundaries: TIGER/Line counties, via the course's `ohio_counties.gpkg`. ACS estimates carry margins of error that this file does not include; for a county with a small population, a rate can move by a point or two between vintages.
