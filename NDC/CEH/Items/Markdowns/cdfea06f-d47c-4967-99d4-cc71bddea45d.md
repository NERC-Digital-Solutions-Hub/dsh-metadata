## Id

cdfea06f-d47c-4967-99d4-cc71bddea45d


## Uri

[https://catalogue.ceh.ac.uk/id/cdfea06f-d47c-4967-99d4-cc71bddea45d](https://catalogue.ceh.ac.uk/id/cdfea06f-d47c-4967-99d4-cc71bddea45d)


## Type

dataset


## Title

Exposure datasets representing a synthetic future urban context, including socio-demographic, building, and land-use data from 10 cities, for natural hazard risk modelling


## Description

This dataset includes synthetically produced data from 10 different cities (Istanbul, Nablus, Chattogram, Cox’s Bazaar, Nairobi, Nakuru, Quito, Kokhana, Rapti and Darussalam) for a future urban context. The data includes physical elements in a city such as buildings, roads, and power networks, as well as social elements such as households and individuals. The dataset contains a maximum of 9 different data types, described below. For some cities power and road network data were not considered due to context specific priorities. 

landuse: The land use plan data depicting how the land will be zoned and used in the next fifty years within the area or interest. The attributes include the land use type, areal coverage in hectares, maximum population density and existing population. 

building: Data representing the building footprints that will emerge as a result of the future exposure generation procedure. It includes the attributes of the building such as its identifier number, construction type, number of floors, footprint area, occupation type and construction code level.

road nodes: Data representing the points where road segments (edges) are connected to each other, including the identifier number for each node.

road edges: Data representing the road segments, including the ID numbers of the starting and ending point (node).

power nodes: Data representing the points where power lines (edges) are connected to each other, including the identifier number for each node.

power edges: Data representing the power segments, including the including the ID numbers of the starting and ending point (node).

household: Data that contains social attributes of a household living in a building. The attributes include number of individuals, income level and commonly used facility ID (such as hospital). 

individual: Data that contains the attributes of the individuals that are a part of a household. The attributes are age, gender, school ID (if relevant), workplace ID (if relevant) and last attained education level.

Distribution table: The future projections for each city that identifies the socio-demographic changes and expected physical development in the next 50 years.

The data can be used in geospatial platforms. The nomenclature for the data is as follows:
“CitynameFutureExposureDataset/Cityname_CommunityCode_DataType”. This dataset was created as case studies for the Tomorrows Cities: Tomorrowville virtual testbed. It is supported by NERC as part of the GCRF Urban Disaster Risk Hub (NE/S009000/1).


## Metadata Date

2025-11-13T16:15:51


## Resource Identifiers

### Code

[https://catalogue.ceh.ac.uk/id/cdfea06f-d47c-4967-99d4-cc71bddea45d](https://catalogue.ceh.ac.uk/id/cdfea06f-d47c-4967-99d4-cc71bddea45d)


### Code

10.5285/cdfea06f-d47c-4967-99d4-cc71bddea45d


### Code Space

doi:




## Lineage

For generating the future exposure dataset for each city, a specific computational algorithm that takes into account the land use plan and user defined future projections is used. The algorithm is explained in detail by Mentese et al., 2023.

The production of the land use plan relies on a community based process, that includes different community groups’ involvement and participatory engagement. In these engagements, in each city, specific groups are identified with the guidance of local experts as part of the Tomorrow’s Cities Project. After the identification, experts from Tomorrow’s Cities Project, local experts and community representatives from the community groups gather for participatory spatial planning for their future urban contexts.

Then, the produced land use plan is integrated (using the software algorithm) with the future socio-demographic projections and expected physical development defined by the local experts and existing literature on the context. As a result of this procedures, building data, socio-demographic datasets and network related data (where relevant) is produced.



## Spatial Representation Types

- textTable
- vector


## Topic Categories

geoscientificInformation

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/geoscientificInformation](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/geoscientificInformation)


economy

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/economy](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/economy)




## Keywords Theme

Environmental risk

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/5](http://onto.nerc.ac.uk/CEHMD/topic/5)




## Keywords Other

Future

risk exposure

### Uri

[http://www.eionet.europa.eu/gemet/concept/12778](http://www.eionet.europa.eu/gemet/concept/12778)


exposure

### Uri

[http://www.eionet.europa.eu/gemet/concept/3067](http://www.eionet.europa.eu/gemet/concept/3067)


hazard

### Uri

[http://www.eionet.europa.eu/gemet/concept/3852](http://www.eionet.europa.eu/gemet/concept/3852)


urban

Tomorrow's cities

GCRF Urban Disaster Risk Hub



## Distribution Formats

### Name

Comma-separated values (CSV)


### Type

text/csv


### Version

unknown


### Name

json


### Version

unknown


### Name

geojson


### Version

unknown


### Name

qmd


### Version

unknown




## Funding

### Funder Name

Natural Environment Research Council


### Funder Identifier

[https://ror.org/02b5d8509](https://ror.org/02b5d8509)


### Award Title

GCRF Urban Disaster Risk Hub


### Award Number

NE/S009000/1


### Award U R I

[https://gtr.ukri.org/projects?ref=NE/S009000/1](https://gtr.ukri.org/projects?ref=NE/S009000/1)


### Ror

True


### Orcid

False




## Bounding Boxes

### West Bound Longitude

-82.267


### East Bound Longitude

77.696


### South Bound Latitude

-13.582


### North Bound Latitude

44.214


### Bounds

{"type": "Feature",      "properties": {},      "geometry": {        "type": "Polygon",        "coordinates": [[[-82.267, -13.582], [-82.267, 44.214], [77.696, 44.214], [77.696, -13.582], [-82.267, -13.582]]]      }}


### Coordinates

[[[-82.267, -13.582], [-82.267, 44.214], [77.696, 44.214], [77.696, -13.582], [-82.267, -13.582]]]




## Distributor Contacts

### Organisation Name

NERC EDS Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

distributor


### Email

info@eidc.ac.uk




## Responsible Parties

### Family Name

Menteşe


### Given Name

E.Y.


### Organisation Name

Anofa Engineering, Planning and Informatics Ltd.


### Role

pointOfContact


### Email

emin.mentese@anofa.co 


### Name Identifier

[https://orcid.org/0000-0002-7187-4384](https://orcid.org/0000-0002-7187-4384)


### Address

#### Delivery Point

Environment Centre Wales, Deiniol Road


#### City

Bangor


#### Administrative Area

Gwynedd


#### Postal Code

LL57 2UW


#### Country

United Kingdom



### Full Name

Menteşe, E.Y.


### Point Of Contact

Anofa Engineering, Planning and Informatics Ltd.


### Family Name

Menteşe


### Given Name

E.Y.


### Organisation Name

Anofa Engineering, Planning and Informatics Ltd.


### Role

author


### Email

emin.mentese@anofa.co 


### Name Identifier

[https://orcid.org/0000-0002-7187-4384](https://orcid.org/0000-0002-7187-4384)


### Full Name

Menteşe, E.Y.


### Family Name

Özer


### Given Name

E.


### Organisation Name

Anofa Engineering, Planning and Informatics Ltd.


### Role

author


### Email

Erdem.ozer@anofa.co


### Name Identifier

[https://orcid.org/0000-0003-3484-4183](https://orcid.org/0000-0003-3484-4183)


### Full Name

Özer, E.


### Family Name

Rawal


### Given Name

P.


### Organisation Name

National Society for Earthquake Technology


### Organisation Identifier

[https://ror.org/058m30p27](https://ror.org/058m30p27)


### Role

author


### Email

prashantrawal@nset.org.np 


### Name Identifier

[https://orcid.org/0000-0001-7940-8014](https://orcid.org/0000-0001-7940-8014)


### Full Name

Rawal, P.


### Family Name

Comelli


### Given Name

T.


### Organisation Name

University College London


### Organisation Identifier

[https://ror.org/02jx3x895](https://ror.org/02jx3x895)


### Role

author


### Email

thaisa.comelli@ucl.ac.uk 


### Name Identifier

[https://orcid.org/0000-0003-3173-2602](https://orcid.org/0000-0003-3173-2602)


### Full Name

Comelli, T.


### Family Name

Cetin


### Given Name

N.İ.


### Organisation Name

Gebze Technical University


### Organisation Identifier

[https://ror.org/01sdnnq10](https://ror.org/01sdnnq10)


### Role

author


### Email

cetinnipek@gmail.com 


### Name Identifier

[https://orcid.org/0000-0002-8141-8112](https://orcid.org/0000-0002-8141-8112)


### Full Name

Cetin, N.İ.


### Family Name

Dabeek


### Given Name

J.


### Organisation Name

An-Najah National University


### Organisation Identifier

[https://ror.org/0046mja08](https://ror.org/0046mja08)


### Role

author


### Email

jamal.dabbeek@najah.edu 


### Name Identifier

[https://orcid.org/0000-0001-8369-4105](https://orcid.org/0000-0001-8369-4105)


### Full Name

Dabeek, J.


### Family Name

Kyesii


### Given Name

A.


### Organisation Name

Ardhi University


### Organisation Identifier

[https://ror.org/05k903r09](https://ror.org/05k903r09)


### Role

author


### Email

akyessi@gmail.com 


### Name Identifier

[https://orcid.org/0000-0002-7058-5070](https://orcid.org/0000-0002-7058-5070)


### Full Name

Kyesii, A.


### Family Name

Chengo


### Given Name

V.


### Organisation Name

Africa Research and Impact Network


### Role

author


### Email

v.chengo@arin-africa.org 


### Name Identifier

[https://orcid.org/0000-0001-5116-5874](https://orcid.org/0000-0001-5116-5874)


### Full Name

Chengo, V.


### Family Name

Zisan


### Given Name

B.


### Organisation Name

Chittagong University of Engineering & Technology


### Organisation Identifier

[https://ror.org/052qsay17](https://ror.org/052qsay17)


### Role

author


### Email

basirzisan@cuet.ac.bd 


### Name Identifier

[https://orcid.org/0000-0002-6959-0235](https://orcid.org/0000-0002-6959-0235)


### Full Name

Zisan, B.


### Family Name

Cubillo


### Given Name

P.


### Organisation Name

Centro de Informacion Urbana de Quito


### Role

author


### Email

pcubillo@ciuq.ec 


### Name Identifier

[https://orcid.org/0009-0009-6117-9466](https://orcid.org/0009-0009-6117-9466)


### Full Name

Cubillo, P.


### Organisation Name

NERC EDS Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

custodian


### Email

info@eidc.ac.uk


### Organisation Name

NERC EDS Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

publisher


### Email

info@eidc.ac.uk


### Organisation Name

University of Edinburgh


### Organisation Identifier

[https://ror.org/01nrxwf90](https://ror.org/01nrxwf90)


### Role

rightsHolder


### Email

emin.mentese@anofa.co




## Online Resources

### Url

[https://data-package.ceh.ac.uk/data/cdfea06f-d47c-4967-99d4-cc71bddea45d](https://data-package.ceh.ac.uk/data/cdfea06f-d47c-4967-99d4-cc71bddea45d)


### Name

Download the data


### Description

Download a copy of this data


### Function

download


### Type

OTHER


### Url

[https://data-package.ceh.ac.uk/sd/cdfea06f-d47c-4967-99d4-cc71bddea45d.zip](https://data-package.ceh.ac.uk/sd/cdfea06f-d47c-4967-99d4-cc71bddea45d.zip)


### Name

Supporting information


### Description

Supporting information available to assist in re-use of this dataset


### Function

information


### Type

OTHER




## Spatial Reference Systems

### Code

[http://www.opengis.net/def/crs/EPSG/0/3857](http://www.opengis.net/def/crs/EPSG/0/3857)


### Title

WGS 84 / Pseudo-Mercator




## Supplemental

### Description

Menteşe, E. Y., Cremen, G., Gentile, R., Galasso, C., Filippi, M. E., & McCloskey, J. (2023). Future exposure modelling for risk-informed decision making in urban planning. International Journal of Disaster Risk Reduction, 90, 103651.


### Url

[https://doi.org/10.1016/j.ijdrr.2023.103651](https://doi.org/10.1016/j.ijdrr.2023.103651)


### Function

relatedArticle




## Dataset Reference Date

### Publication Date

2025-08-20



## Use Constraints

This resource is available under the terms of the Open Government Licence

### Code

license


### Uri

[https://eidc.ac.uk/licences/ogl/plain](https://eidc.ac.uk/licences/ogl/plain)




## Resource Type

dataset

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/ResourceType/dataset](http://inspire.ec.europa.eu/metadata-codelist/ResourceType/dataset)



## Access Limitation

no limitations to public access

### Code

Available


### Uri

[http://purl.org/coar/access_right/c_abf2](http://purl.org/coar/access_right/c_abf2)



## Not G E M I N I

True


## Has Online Service Agreement

False


## Licences

This resource is available under the terms of the Open Government Licence

### Code

license


### Uri

[https://eidc.ac.uk/licences/ogl/plain](https://eidc.ac.uk/licences/ogl/plain)




## Incoming Citation Count

0


## Topics

- [http://onto.nerc.ac.uk/CEHMD/topic/5](http://onto.nerc.ac.uk/CEHMD/topic/5)


## Resource Status

Available


## Points Of Contact

### Family Name

Menteşe


### Given Name

E.Y.


### Organisation Name

Anofa Engineering, Planning and Informatics Ltd.


### Role

pointOfContact


### Email

emin.mentese@anofa.co 


### Name Identifier

[https://orcid.org/0000-0002-7187-4384](https://orcid.org/0000-0002-7187-4384)


### Address

#### Delivery Point

Environment Centre Wales, Deiniol Road


#### City

Bangor


#### Administrative Area

Gwynedd


#### Postal Code

LL57 2UW


#### Country

United Kingdom



### Full Name

Menteşe, E.Y.


### Point Of Contact

Anofa Engineering, Planning and Informatics Ltd.




## Rights Holders

### Organisation Name

University of Edinburgh


### Organisation Identifier

[https://ror.org/01nrxwf90](https://ror.org/01nrxwf90)


### Role

rightsHolder


### Email

emin.mentese@anofa.co




## Info Links

### Url

[https://data-package.ceh.ac.uk/sd/cdfea06f-d47c-4967-99d4-cc71bddea45d.zip](https://data-package.ceh.ac.uk/sd/cdfea06f-d47c-4967-99d4-cc71bddea45d.zip)


### Name

Supporting information


### Description

Supporting information available to assist in re-use of this dataset


### Function

information


### Type

OTHER




## Publishers

### Organisation Name

NERC EDS Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

publisher


### Email

info@eidc.ac.uk




## Authors

### Family Name

Menteşe


### Given Name

E.Y.


### Organisation Name

Anofa Engineering, Planning and Informatics Ltd.


### Role

author


### Email

emin.mentese@anofa.co 


### Name Identifier

[https://orcid.org/0000-0002-7187-4384](https://orcid.org/0000-0002-7187-4384)


### Full Name

Menteşe, E.Y.


### Family Name

Özer


### Given Name

E.


### Organisation Name

Anofa Engineering, Planning and Informatics Ltd.


### Role

author


### Email

Erdem.ozer@anofa.co


### Name Identifier

[https://orcid.org/0000-0003-3484-4183](https://orcid.org/0000-0003-3484-4183)


### Full Name

Özer, E.


### Family Name

Rawal


### Given Name

P.


### Organisation Name

National Society for Earthquake Technology


### Organisation Identifier

[https://ror.org/058m30p27](https://ror.org/058m30p27)


### Role

author


### Email

prashantrawal@nset.org.np 


### Name Identifier

[https://orcid.org/0000-0001-7940-8014](https://orcid.org/0000-0001-7940-8014)


### Full Name

Rawal, P.


### Family Name

Comelli


### Given Name

T.


### Organisation Name

University College London


### Organisation Identifier

[https://ror.org/02jx3x895](https://ror.org/02jx3x895)


### Role

author


### Email

thaisa.comelli@ucl.ac.uk 


### Name Identifier

[https://orcid.org/0000-0003-3173-2602](https://orcid.org/0000-0003-3173-2602)


### Full Name

Comelli, T.


### Family Name

Cetin


### Given Name

N.İ.


### Organisation Name

Gebze Technical University


### Organisation Identifier

[https://ror.org/01sdnnq10](https://ror.org/01sdnnq10)


### Role

author


### Email

cetinnipek@gmail.com 


### Name Identifier

[https://orcid.org/0000-0002-8141-8112](https://orcid.org/0000-0002-8141-8112)


### Full Name

Cetin, N.İ.


### Family Name

Dabeek


### Given Name

J.


### Organisation Name

An-Najah National University


### Organisation Identifier

[https://ror.org/0046mja08](https://ror.org/0046mja08)


### Role

author


### Email

jamal.dabbeek@najah.edu 


### Name Identifier

[https://orcid.org/0000-0001-8369-4105](https://orcid.org/0000-0001-8369-4105)


### Full Name

Dabeek, J.


### Family Name

Kyesii


### Given Name

A.


### Organisation Name

Ardhi University


### Organisation Identifier

[https://ror.org/05k903r09](https://ror.org/05k903r09)


### Role

author


### Email

akyessi@gmail.com 


### Name Identifier

[https://orcid.org/0000-0002-7058-5070](https://orcid.org/0000-0002-7058-5070)


### Full Name

Kyesii, A.


### Family Name

Chengo


### Given Name

V.


### Organisation Name

Africa Research and Impact Network


### Role

author


### Email

v.chengo@arin-africa.org 


### Name Identifier

[https://orcid.org/0000-0001-5116-5874](https://orcid.org/0000-0001-5116-5874)


### Full Name

Chengo, V.


### Family Name

Zisan


### Given Name

B.


### Organisation Name

Chittagong University of Engineering & Technology


### Organisation Identifier

[https://ror.org/052qsay17](https://ror.org/052qsay17)


### Role

author


### Email

basirzisan@cuet.ac.bd 


### Name Identifier

[https://orcid.org/0000-0002-6959-0235](https://orcid.org/0000-0002-6959-0235)


### Full Name

Zisan, B.


### Family Name

Cubillo


### Given Name

P.


### Organisation Name

Centro de Informacion Urbana de Quito


### Role

author


### Email

pcubillo@ciuq.ec 


### Name Identifier

[https://orcid.org/0009-0009-6117-9466](https://orcid.org/0009-0009-6117-9466)


### Full Name

Cubillo, P.




## Publication Date

2025-08-20T00:00:00.000+00:00


## Custodians

### Organisation Name

NERC EDS Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

custodian


### Email

info@eidc.ac.uk




## Updated Date

2025-11-13T16:15:51.000+00:00


## Citation

### Authors

- Menteşe, E.Y.
- Özer, E.
- Rawal, P.
- Comelli, T.
- Cetin, N.İ.
- Dabeek, J.
- Kyesii, A.
- Chengo, V.
- Zisan, B.
- Cubillo, P.


### Doi

10.5285/cdfea06f-d47c-4967-99d4-cc71bddea45d


### Title

Exposure datasets representing a synthetic future urban context, including socio-demographic, building, and land-use data from 10 cities, for natural hazard risk modelling


### Publisher

NERC EDS Environmental Information Data Centre


### Resource Type General

dataset


### Year

2025


### Month

8


### Day

20


### Bibtex

[https://catalogue.ceh.ac.uk/documents/cdfea06f-d47c-4967-99d4-cc71bddea45d/citation?format=bib](https://catalogue.ceh.ac.uk/documents/cdfea06f-d47c-4967-99d4-cc71bddea45d/citation?format=bib)


### Ris

[https://catalogue.ceh.ac.uk/documents/cdfea06f-d47c-4967-99d4-cc71bddea45d/citation?format=ris](https://catalogue.ceh.ac.uk/documents/cdfea06f-d47c-4967-99d4-cc71bddea45d/citation?format=ris)


### Url

[https://doi.org/10.5285/cdfea06f-d47c-4967-99d4-cc71bddea45d](https://doi.org/10.5285/cdfea06f-d47c-4967-99d4-cc71bddea45d)


