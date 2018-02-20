@todo

# Boundary-linked Data User Stories

## Describe boundary-linked data

```
As a Data Publisher
I want to describe boundary-linked data in a data package
So that it can be validated, discovered and used with confidence
```

Supported by the using:

- the [`locations`](https://research.okfn.org/spatial-data-package-investigation/#point-datasets) `"type": "lat-lon"` property, to describe which columns represent `latitude` and `longitude`
- the correct data [`type`](https://frictionlessdata.io/specs/table-schema/#types-and-formats) for the fields representing `latitude` and `longitude`
- `minimum` and `maximum` [`constraints`](https://frictionlessdata.io/specs/table-schema/#constraints) to optionally restrict the `latitude` and `longitude` coordinate pairs to a geographic bounding box
- the [`spatialExtent`](https://hackmd.io/s/SyyEbQuEM#Describe-and-validate-the-spatial-extent-of-point-data) property to describe the geographic bounding polygon that the `latitude` and `longitude` coordinate pairs must be inside

*Note there is no `"spatial-profile": "boundary-linked"` property, to describe the type of spatial data in the data package recommended in the [Spatial Data Package Investigation](https://research.okfn.org/spatial-data-package-investigation/#package-level-).*

## Validate boundary-linked data

```
As a Data Publisher
I want to validate boundary identifiers in the data
So that I can correct any errors and share quality data, or explain the errors in the data
```

Supported by using software to check that boundary identifiers values:
- match the referenced property defined in the [`locations`](https://research.okfn.org/spatial-data-package-investigation/#preparing-boundary-linked-tabular-data) property.
- match the data `type` and comply with any `constraints` defined in the schema


## Discover boundary-linked data

```
As a Data Consumer
I want to search for boundary-linked data
So that I can quickly find the data I'm looking for
```

Supported by using software to search for data packages that:
- include the `"spatial-profile": "boundary-linked"` property (if implemented in the specification)

## Discover boundary-linked data within a geographic area

```
As a Data Consumer
I want to search for boundary-linked data within a geographic area selected using a map
So that I can quickly find the data I'm looking for
```

Not directly supported. Possible support by using software to search using the `spatialExtent` of the spatial data referenced in the `locations` property and determine if it intersects with the searched geographic area

*Another user story could be to discover boundary-linked data using a name of a geographic area (e.g. town, state, country). The name could be converted to  a geographic area and then the above search performed.*

## Display point data on the Queensland Globe

```
As a Data Consumer
I want to display point data on the Queensland Globe
So that I can see the data on an online map
```

Not supported by the `Add my data` function in the [Queensland Globe](https://qldglobe.information.qld.gov.au/)
