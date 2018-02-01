# Source Data

A sample of service location data.

Data downloaded from data.qld.gov.au on 2018-01-26. There is no intention to keep this data up-to-date.

Where multiple formats are offered, CSV is preferred.

- [Government service counter locations](https://data.qld.gov.au/dataset/government-service-counter-locations) - [data](qgap.csv)
- [Queensland public hospitals](https://data.qld.gov.au/dataset/queensland-public-hospitals) - [data](130711-public-hospitals.xls)
- [Queensland Ambulance Service Locations and Co-ordinates](https://data.qld.gov.au/dataset/queensland-ambulance-service-locations-and-co-ordinates) - [data](qas-locations-and-coordinates-2014-16-v1-0-20171220.xlsx) 2017
- [BreastScreen Queensland - Service Locations](https://data.qld.gov.au/dataset/breastscreen-queensland-service-locations) - [data](breastscreen-qld-locations-v5.csv)
- [Queensland Fire and Emergency Services - Urban Fire Stations](https://data.qld.gov.au/dataset/queensland-urban-fire-stations) - [data](UrbanFireStations.csv)
- [Queensland Fire and Emergency Services - Rural Fire Stations](https://data.qld.gov.au/dataset/rural-fire-stations) - [data](RuralFireStations.csv)
- [Queensland Agricultural Training Colleges Sites](https://data.qld.gov.au/dataset/queensland-agricultural-training-colleges-sites) - [data](2014-15-queensland-agricultural-trainingcolleges-sites.csv)
- [Cattle tick clearing facilities—locations](https://data.qld.gov.au/dataset/cattle-tick-clearing-facilities-locations) - [data](Cattle-Tick-clearing-facilities-by-location-2014-15.csv)
- [Q-Ride providers](https://data.qld.gov.au/dataset/q-ride-providers) - [data](171027qrideprovidersa.csv)
- [Go card retailers](https://data.qld.gov.au/dataset/go-card-retailers) - [data](gocard-retailers.csv)
- [Contact a Housing Service Centre](https://data.qld.gov.au/dataset/contact-a-housing-service-centre) - [data](housing-service-centres.csv)
- [QPS Police Stations](https://data.qld.gov.au/dataset/qps-police-stations) - [data](https://data.qld.gov.au/dataset/qps-police-stations/resource/b0aa480e-f023-4bbf-9c54-3a8036edfb14) (zipped SHP file)
- [Justice of the Peace and Commissioner of Declarations signing locations](https://data.qld.gov.au/dataset/jp-or-cdec-location) - [data](jps-in-the-community.csv)
- [Probation and parole reporting locations](https://data.qld.gov.au/dataset/probation-and-parole-reporting-locations) - [data](probation-parole-reporting-locations.csv)
- [Prison locations](https://data.qld.gov.au/dataset/prison-locations) - [data](prison-locations.csv)
- [Youth justice centre locations](https://data.qld.gov.au/dataset/youth-justice-centre-locations) - [data](youth-detention-centre-locations.csv)
- [Courthouse locations](https://data.qld.gov.au/dataset/courthouse-locations) - [data](courthouses.csv)
- [Contacts list—Department of Communities, Child Safety and Disability Services](https://data.qld.gov.au/dataset/contacts-list-department-of-communities-child-safety-and-disability-services) - [data](dccsds-contact-details.csv)
- [Sport and recreation services training-providers](https://data.qld.gov.au/dataset/sport-and-recreation-services-training-providers) - [data](registered-training-organisations-july-2013.csv)
- [Training organisations](https://data.qld.gov.au/dataset/training-organisations) - [data](registered-training-organisations-july-2013.csv)
- [Queensland state schools—geographic information](https://data.qld.gov.au/dataset/queensland-state-schools-geographic-information) - data not available for download
- [Non-State school details](http://www.nssab.qld.edu.au/OpenData/index.php#SchoolDetails) - [data](OpenData_ListofSchools_1217.xlsx)

Having visited all the above pages, there are opportunities to adopt a consistent approach to:

- naming datasets and resources
- versioning resources over time
- applying CKAN tags
- the file format i.e. CSV
- storing the data so it downloads instead of [displaying in the browser](http://www.justice.qld.gov.au/media/data/courthouses.csv?timestamp=2017-03-16AEST07-47-58)
- the data structure

Some datasets appear to be out-of-date.

It seems [GDA94](https://en.wikipedia.org/wiki/Geocentric_Datum_of_Australia_1994) is used for coordinates. This will need to be changed to [GDA2020](http://www.ga.gov.au/scientific-topics/positioning-navigation/datum-modernisation) if an Australia Datum is continued to be used. An alternative is to use WGS84 (aka [EPSG:4326](https://epsg.io/4326)) so data can be combined with International data and easily display in mapping applications.
