# Service Locations

*An experiment in packaging location data*

## Aim

The aim of this repository is to:

- recommend new ways to publish location data on data.qld.gov.au
- provide feedback on the Open Knowledge [Spatial Data Package Investigation recommendations](https://research.okfn.org/spatial-data-package-investigation/#recommendations) to the [Frictionless Data specification](https://frictionlessdata.io/specs/).

## Background

There are many [tabular location datasets published on data.qld.gov.au](https://data.qld.gov.au/dataset?q=location), that describe location using:

- points (longitude and latitude coordinate pairs)  
- boundary identifiers or names

These datasets could be linked to spatial [boundary data](/boundary-data/).

### Service location point data

A subset point location datasets describe service locations, e.g. the locations of hospitals, schools and fire stations.

These are not published in a consistent way making it hard to combine the data. Some location datasets also include services available at the location and opening times, e.g. [Transport and motoring customer service centres](https://data.qld.gov.au/dataset/transport-csc).

Some datasets are messy e.g.

- missing column headers
- column headers with no dataset
- inconsistent data types in columns
- markdown in columns
- html fragments in column to support a specific use case

In some cases these datasets drive the display of [service locations on qld.gov.au](https://www.qld.gov.au/transport/contacts/centres). While it's great to see organisations using their own open data to deliver information, this should not be at the expense of others wanting to use the same information.

This repository for point data:

- collects [service location point data](/point-data/) from data.qld.gov.au
- analyses the [headers in the source data](/template/header-analysis.csv) and [groups common headers](/template/header-grouping.xls) to help design a template.
- suggests a [template](/template/service-locations/) to capture service location and related data. The template uses the recommendations from the Spatial Data Package Investigation and explores [refinements discussed on the Open Knowledge Forum](https://discuss.okfn.org/t/geo-data-package/6143/25)
- repackages the service location data into [data packages](/datapackages/) in line with the recommendations

### Linked Boundary data

This repository for linked boundary data:

- collects [csv files with a link to boundaries](/linked-boundary-data/) and repackages the linked boundary data into data packages that reference spatial [boundary data](/boundary-data/)

### Non-spatial Boundary data

This repository for non-spatial boundary data:
- collects [boundary names](/boundary-names/) and packages then so they can be used to validate boundary names in other csv files.

### Spatial Boundary dataset

This repository for [spatial boundary data](/boundary-data/):

- converts the data to GeoJSON
- packages the data into data packages in line with the recommendations

## Data Validation

Based on the validation settings in [goodtables.yml](goodtables.yml) the tabular data is [![goodtables.io](https://goodtables.io/badge/github/Stephen-Gates/service-locations.svg)](https://goodtables.io/github/Stephen-Gates/service-locations)

## Software

Software is needed to implement the following spatial functions:

- ~~check points are within spatial extent~~
- ~~discover spatial data~~
- ~~discover spatial data in a spatial area~~
- validate point data coordinate pairs

## References

As part of the work we will also explore leveraging existing concepts, data, and services, e.g.

- [When are open (geospatial) identifiers useful?](https://blog.ldodds.com/2018/01/29/when-are-open-geospatial-identifiers-useful/)
- [persistent resolvable identifiers](https://www.gov.uk/government/publications/open-standards-for-government/persistent-resolvable-identifiers)
- [Place names gazetteer - Queensland](http://qldspatial.information.qld.gov.au/catalogue/custom/detail.page?fid={1B19B980-B171-47C1-9AA6-5B95A7158ADC})
- [Services](http://qldspatial.information.qld.gov.au/catalogue/custom/search.page?gp-search-term=region&gp-search-go=)
- [Property Location Service Plus- Queensland Government version](http://qldspatial.information.qld.gov.au/catalogue/custom/detail.page?fid={D77C19E4-5C24-46E4-80C3-244164182572})
- [data versioning](https://www.w3.org/TR/dwbp/#dataVersioning) and [spatial data versioning](https://www.w3.org/TR/sdw-bp/#bp-dataversioning)
- [UK standards](https://www.gov.uk/government/publications/open-standards-for-government/exchange-of-location-point)
- [OpenBanking Branch API Specification - v2.1.1](https://openbanking.atlassian.net/wiki/spaces/DZ/pages/13402282/Branch+API+Specification+-+v2.1.1)
