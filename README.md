# Service Locations

*An experiment in repackaging service location data*

There are many [tabular location datasets published on data.qld.gov.au](https://data.qld.gov.au/dataset?q=location). A subset of these describe service locations, e.g. the locations of hospitals, schools and fire stations.

These are not published in a consistent way making it hard to combine the data. Some location datasets also include services available at the location and opening times, e.g. [Transport and motoring customer service centres](https://data.qld.gov.au/dataset/transport-csc).

Some datasets are messy e.g.

- missing column headers
- column headers with no dataset
- inconsistent data types in columns
- markdown in columns
- html fragments in column to support a specific use case

In some cases these datasets drive the display of [service locations on qld.gov.au](https://www.qld.gov.au/transport/contacts/centres). While it's great to see organisations using their own open data to deliver information, this should not be at the expense of others wanting to use the same information.

Recently [Open Knowledge International](https://okfn.org) produced a report, [Spatial Data Package Investigation](https://research.okfn.org/spatial-data-package-investigation/), to explore how the [Frictionless Data specification](https://frictionlessdata.io/specs/) could be refined to improve the publishing of location data.

This repository:
- collects [service location data](/source-data/README.md) from data.qld.gov.au
- suggests a template to capture service location and related data. The template uses the recommendations from the Spatial Data Package Investigation and explores [refinements discussed on the Open Knowledge Forum](https://discuss.okfn.org/t/geo-data-package/6143/25)
- repackages the service location data in line with the recommendations

The aim is to:

- recommend a new way to publish service location data on data.qld.gov.au
- provide feedback to Open Knowledge on the [Spatial Data Package Investigation recommendations](https://research.okfn.org/spatial-data-package-investigation/#recommendations)
