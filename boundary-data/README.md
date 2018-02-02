This directory contains boundary GeoJSON data e.g. Queensland and various administrative boundaries

## Boundary services

Services exist that need to be explored further...

E.g. In a browser, enter

`https://gisservices.information.qld.gov.au/arcgis/rest/services/PlanningCadastre/LandParcelPropertyFramework/MapServer/20/query?f=json&where=ADMINAREANAME+<>+%27Null%27&returnGeometry=false&spatialRel=esriSpatialRelIntersects&outFields=ADMINAREANAME&orderByFields=ADMINAREANAME`

A list of the 77 LGA's in Queensland is returned (without geometry). [View the result](https://jsoneditoronline.org/?url=https%3A%2F%2Fgisservices.information.qld.gov.au%2Farcgis%2Frest%2Fservices%2FPlanningCadastre%2FLandParcelPropertyFramework%2FMapServer%2F20%2Fquery%3Ff%3Djson%26where%3DADMINAREANAME%2B%253c%253e%2B%2527Null%2527%26returnGeometry%3Dfalse%26spatialRel%3DesriSpatialRelIntersects%26outFields%3DADMINAREANAME%26orderByFields%3DADMINAREANAME) in JSON Online Editor.

Knowing the name of one of those LGAs, "AURUKUN SHIRE", you can then request the geometry

`https://gisservices.information.qld.gov.au/arcgis/rest/services/PlanningCadastre/LandParcelPropertyFramework/MapServer/20/query?f=json&where=ADMINAREANAME%20%3D%20%27AURUKUN%20SHIRE%27&returnGeometry=true&spatialRel=esriSpatialRelIntersects&outSR=102100` 

[View the result](https://jsoneditoronline.org/?url=https%3A%2F%2Fgisservices.information.qld.gov.au%2Farcgis%2Frest%2Fservices%2FPlanningCadastre%2FLandParcelPropertyFramework%2FMapServer%2F20%2Fquery%3Ff%3Djson%26where%3DADMINAREANAME%2520%253D%2520%2527AURUKUN%2520SHIRE%2527%26returnGeometry%3Dtrue%26spatialRel%3DesriSpatialRelIntersects%26outSR%3D102100) in JSON Online Editor.
