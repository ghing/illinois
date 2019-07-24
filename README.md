# Data about the state of Illinois

## Generated data

### Crosswalk of census tracts to places

Filename: `data/out/illinois_tract_to_place__2018.csv`

Data sources:

- Census Place Boundaries
- Census Tract Boundaries

Process:

I used QGIS to do a spatial join on the tracts and places using a technique similar to the one described in the tutorial [Performing Spatial Joins (QGIS3)](https://www.qgistutorials.com/en/docs/3/performing_spatial_joins.html). However, I used "Join Attributes by Location" instead of "Join Attrivutes by Location (summary)."

Then in Excel, I made the following changes:

I deleted these columns from the tract data:

MTFCC
FUNCSTAT 
ALAND
AWATER
INTPTLAT
INTPTLON

I deleted the duplicate state FIPS code column from the

And deleted these columns that originated in the place data:

STATEFP_2
MTFCC_2
FUNCSTAT_2
ALAND_2
AWATER_2
INTPTLAT_2
INTPTLON_2

I renamed these columns to clarify that they refer to tracts or places:

COUNTYFP > TRACT_COUNTYFP
GEOID > TRACT_GEOID
NAME > TRACT_NAME
NAMELSAD > TRACT_NAMELSAD
GEOID_2 > PLACE_GEOID
NAME_2 > PLACE_NAME
PLACE_NAMELSAD

## Data sources

### Census Places Boundaries

Source: [TIGER/Line Shapefiles](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.2018.html)

Vintage: 2018

### Census Tract Boundaries

Source: [TIGER/Line Shapefiles](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.2018.html)

Vintage: 2018
