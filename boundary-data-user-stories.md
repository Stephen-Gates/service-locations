# Boundary Data User Stories

## Describe boundary data

```
As a Data Publisher
I want to describe boundary data in a data package
So that it can be validated, discovered and used with confidence.
```

Supported by the using:
- the [`"spatial-profile": "simple-vector"`](https://research.okfn.org/spatial-data-package-investigation/#package-level-) property, to describe the type of spatial data in the data package
- the [`locations`](https://research.okfn.org/spatial-data-package-investigation/#point-datasets) `"type": "geojson"` property, to describe how to interpret the location data
- the [`spatialExtent`](https://hackmd.io/s/SyyEbQuEM#Describe-and-validate-the-spatial-extent-of-point-data) property to describe the geographic bounding polygon that the boundaries must be inside

## Validate boundary data geometry

```
As a Data Publisher
I want to validate boundary data geometry
So that I can correct any errors and share quality data, or explain the errors in the data.
```

Supported by using software to check that boundary data geometry values
- create valid polygons
- don't overlap or have gaps

## Validate boundary data properties

```
As a Data Publisher
I want to validate boundary data properties
So that I can correct any errors and share quality data, or explain the errors in the data.
```

Supported by using software to check that boundary data property values match the data `type` and comply with any `constraints` defined in the schema.

## Validate boundary data is within geographic area

```
As a Data Publisher
I want to validate that all boundary data geometries are inside a referenced geographic area
So that I can correct any errors and share quality data, or explain the errors in the data.
```

Supported by using software to check that boundary data geometries are inside the geographic area referenced by the `spatialExtent`.

## Discover boundary data

```
As a Data Consumer
I want to search for boundary data
So that I can quickly find the data I'm looking for.
```

Supported by using software to searching for data packages that include the `"spatial-profile": "simple-vector"` property.

## Discover boundary data within a geographic area

```
As a Data Consumer
I want to search for boundary data within a geographic area selected from a map
So that I can quickly find the data I'm looking for.
```

Supported by using software to searching for data packages that:
- include the `"spatial-profile": "simple-vector"` property
- have a `spatialExtent` that intersects with the searched geographic area

*Another user story could be to discover point data using a name of a geographic area (e.g. town, state, country). The name could be converted to  a geographic area and then the above search performed.*

## Display simple-vector data on the Queensland Globe

```
As a Data Consumer
I want to display point data on the Queensland Globe
So that I can see the data on an online map
```

Currently not supported by the `Add my data` function as only .gpx, .kml or .csv files  can be uploaded to the [Queensland Globe](https://qldglobe.information.qld.gov.au/)
