## Id

f83a56ef-15ad-4270-aefd-a6ef4b24b4ee


## Uri

[https://catalogue.ceh.ac.uk/id/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee](https://catalogue.ceh.ac.uk/id/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee)


## Type

dataset


## Title

Deposition and concentration of nitrogen and sulphur for protected sites in the UK, 2018-2020


## Description

This dataset provides deposition values of sulphur and nitrogen deposition, deposition of non-marine base cations and concentration values for ammonia (NH3), sulphur dioxide (SO2) and nitrogen oxide (NOx) on the UK nature conservation protected sites, averaged over the years 2018 to 2020. The dataset also includes calculated minimum, maximum and gridded average values for each site. Protected nature sites covered are: 
(i) Special Areas of Conservation (SAC) 
(ii) Special Protection Areas (SPA) 
(iii) Sites of Special Scientific Interest (SSSI). 

The data consist of values of nitrogen and acid deposition, non-marine base cations deposition, and concentrations of ammonia (NH3) based on the Concentration Based Estimated Deposition (CBED), and concentrations of NOx and SO2 using the Pollution Climate Mapping (PCM) model. 

Nitrogen and acid deposition data is also given for specific habitat types including: 
(i) moorland/short vegetation everywhere, 
(ii) forest everywhere, and 
(iii) the grid square average over multiple land cover types (i.e. arable, grassland, forest, moorland, urban) 

These habitat-specific data are recommended for use with critical loads for the calculation of critical load exceedances using the relevant deposition/habitat type.


## Metadata Date

2025-11-13T16:27:46


## Resource Identifiers

### Code

[https://catalogue.ceh.ac.uk/id/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee](https://catalogue.ceh.ac.uk/id/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee)


### Code

10.5285/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee


### Code Space

doi:




## Lineage

The Air Pollution Information System (APIS), through the 'Site Relevant Critical Loads' tool and APIS new mapping interface, provides critical loads for acidity and nitrogen and critical levels for ammonia, sulphur dioxide and nitrogen oxides for designated features within every SAC, SPA or A/SSSI in the UK. In addition, deposition and concentration data for nitrogen, sulphur pollutants and non-marine base cations are provided at each site to give an estimate of critical load/level exceedance.

The data provided is based on pollutant deposition gridded maps for nitrogen and acid deposition and concentration maps of ammonia, nitrogen oxides, sulphur and non-marine base cations, which are overlayed to a GIS shape file of site boundaries in the UK (e.g. SAC, SPA, SSSI). These gridded maps were then clipped to provide the pollutant values for each grid square including the area of the clipped grid. The resulting data was then queried to generate site statistics in the form of a minimum, maximum and area weighted average values for each of the pollutants.

For nitrogen and acid deposition values, base cations deposition and ammonia concentrations, 3 year average pollutant maps were used at a resolution of 1 x 1 km from the CBED model for the years 2018-2020. For nitrogen dioxide and sulphur dioxide concentrations the 1 x 1 km PCM model was used based on the 3 year average (2018-2020). Deposition values are generated for specific habitat types (forest and semi-natural) to be used in critical load exceedance calculations.

The full methodology is available in the contextual metadata available with this dataset.

The work of APIS is jointly funded between the Centre for Ecology & Hydrology and the UK pollution and conservation agencies including Natural Resources Wales (NRW), the Environment Agency, Northern Ireland Environment Agency, Natural England, the Joint Nature Conservation Committee (JNCC), the Scottish Environment Protection Agency (SEPA), and Scottish Natural Heritage (SNH).


## Reason Changed

A mapping error occurred in the ammonia data of CBED 2018-2020. This also translates to an error in total nitrogen deposition. 

The origin of the error is an R software update problem using the library 'proj4' to project to British National Grid which did not project correctly.  Further QC checks have been put in place to help prevent this type of error occurring again. As an update, CBED and APIS - 2019-2021 will be published soon (see [https://www.apis.ac.uk/revised-APIS-2019](https://www.apis.ac.uk/revised-APIS-2019) )


## Spatial Representation Types

- textTable


## Topic Categories

environment

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/environment](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/environment)




## Keywords Theme

Pollution

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/15](http://onto.nerc.ac.uk/CEHMD/topic/15)




## Keywords Other

sulphate

### Uri

[http://www.eionet.europa.eu/gemet/concept/8190](http://www.eionet.europa.eu/gemet/concept/8190)


ammonia

### Uri

[http://www.eionet.europa.eu/gemet/concept/375](http://www.eionet.europa.eu/gemet/concept/375)


nitrogen

### Uri

[http://onto.nerc.ac.uk/CAST/273](http://onto.nerc.ac.uk/CAST/273)


pollutant deposition

### Uri

[http://www.eionet.europa.eu/gemet/concept/6406](http://www.eionet.europa.eu/gemet/concept/6406)




## Distribution Formats

### Name

Comma-separated values (CSV)


### Type

text/csv


### Version

unknown




## Inspire Themes

### Theme

Environmental Monitoring Facilities


### Uri

[http://inspire.ec.europa.eu/theme/ef](http://inspire.ec.europa.eu/theme/ef)




## Spatial Resolutions

### Distance

1000




## Funding

### Funder Name

Department for Environment Food and Rural Affairs


### Funder Identifier

[https://ror.org/00tnppw48](https://ror.org/00tnppw48)


### Ror

True


### Orcid

False




## Bounding Boxes

### West Bound Longitude

-8.648


### East Bound Longitude

1.768


### South Bound Latitude

49.864


### North Bound Latitude

60.861


### Bounds

{"type": "Feature",      "properties": {},      "geometry": {        "type": "Polygon",        "coordinates": [[[-8.648, 49.864], [-8.648, 60.861], [1.768, 60.861], [1.768, 49.864], [-8.648, 49.864]]]      }}


### Coordinates

[[[-8.648, 49.864], [-8.648, 60.861], [1.768, 60.861], [1.768, 49.864], [-8.648, 49.864]]]




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

Martin Hernandez


### Given Name

Cristina


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

pointOfContact


### Email

enquiries@ceh.ac.uk


### Address

#### Delivery Point

Bush Estate


#### City

Penicuik


#### Administrative Area

Midlothian


#### Postal Code

EH26 0QB


#### Country

United Kingdom



### Full Name

Martin Hernandez, C.


### Point Of Contact

UK Centre for Ecology & Hydrology


### Family Name

Bealey


### Given Name

W.J.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-3708-5864](https://orcid.org/0000-0003-3708-5864)


### Full Name

Bealey, W.J.


### Family Name

Martin Hernandez


### Given Name

C.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Martin Hernandez, C.


### Family Name

Vigier


### Given Name

A.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0001-6798-409X](https://orcid.org/0000-0001-6798-409X)


### Full Name

Vigier, A.


### Family Name

Levy


### Given Name

P.E.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-8505-1901](https://orcid.org/0000-0002-8505-1901)


### Full Name

Levy, P.E.


### Family Name

Stedman


### Given Name

J.R.


### Organisation Name

Ricardo Energy & Environment


### Role

author


### Email

john.stedman@ricardo.com


### Full Name

Stedman, J.R.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

rightsHolder


### Email

enquiries@ceh.ac.uk


### Organisation Name

Natural Resources Wales


### Organisation Identifier

[https://ror.org/04x65hs26](https://ror.org/04x65hs26)


### Role

rightsHolder


### Email

enquiries@naturalresourceswales.gov.uk


### Organisation Name

Environment Agency


### Organisation Identifier

[https://ror.org/01zewfb16](https://ror.org/01zewfb16)


### Role

rightsHolder


### Email

enquiries@environment-agency.gov.uk


### Organisation Name

Northern Ireland Environment Agency


### Organisation Identifier

[https://ror.org/01d29cd45](https://ror.org/01d29cd45)


### Role

rightsHolder


### Email

nieainfo@daera-ni.gov.uk


### Organisation Name

Natural England


### Organisation Identifier

[https://ror.org/00r66pz14](https://ror.org/00r66pz14)


### Role

rightsHolder


### Email

enquiries@naturalengland.org.uk


### Organisation Name

Joint Nature Conservation Committee


### Organisation Identifier

[https://ror.org/05tzsrw37](https://ror.org/05tzsrw37)


### Role

rightsHolder


### Email

data@jncc.gov.uk


### Organisation Name

Scotland and Northern Ireland Forum for Environmental Research (SNIFFER)


### Organisation Identifier

[https://ror.org/00e99w454](https://ror.org/00e99w454)


### Role

rightsHolder


### Email

bib@ceh.ac.uk 


### Organisation Name

Scottish Environment Protection Agency


### Organisation Identifier

[https://ror.org/01kxjy285](https://ror.org/01kxjy285)


### Role

rightsHolder


### Email

bib@ceh.ac.uk


### Organisation Name

Scottish Natural Heritage


### Organisation Identifier

[https://ror.org/01t6g8w08](https://ror.org/01t6g8w08)


### Role

rightsHolder


### Email

enquiries@nature.scot


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




## Temporal Extents

### Begin

2018-01-01


### End

2020-12-31




## Online Resources

### Url

[https://data-package.ceh.ac.uk/sd/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee.zip](https://data-package.ceh.ac.uk/sd/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee.zip)


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

[http://www.opengis.net/def/crs/EPSG/0/27700](http://www.opengis.net/def/crs/EPSG/0/27700)


### Title

OSGB 1936 / British National Grid




## Dataset Reference Date

### Creation Date

2022-08-26


### Publication Date

2022-09-05


### Unavailable Date

2023-02-13



## Use Constraints

This resource is available under the terms of the Open Government Licence

### Code

license


### Uri

[https://eidc.ac.uk/licences/ogl/plain](https://eidc.ac.uk/licences/ogl/plain)


© UK Centre for Ecology & Hydrology, Natural Resources Wales, Environment Agency, the Northern Ireland Environment Agency, Natural England, the Joint Nature Conservation Committee (JNCC), Scotland and Northern Ireland Forum for Environmental Research (SNIFFER), the Scottish Environment Protection Agency (SEPA), Scottish Natural Heritage (SNH)

### Code

copyright




## Resource Type

dataset

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/ResourceType/dataset](http://inspire.ec.europa.eu/metadata-codelist/ResourceType/dataset)



## Access Limitation

withdrawn

### Code

Withdrawn



## Not G E M I N I

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

- [http://onto.nerc.ac.uk/CEHMD/topic/15](http://onto.nerc.ac.uk/CEHMD/topic/15)


## Resource Status

Withdrawn


## Points Of Contact

### Family Name

Martin Hernandez


### Given Name

Cristina


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

pointOfContact


### Email

enquiries@ceh.ac.uk


### Address

#### Delivery Point

Bush Estate


#### City

Penicuik


#### Administrative Area

Midlothian


#### Postal Code

EH26 0QB


#### Country

United Kingdom



### Full Name

Martin Hernandez, C.


### Point Of Contact

UK Centre for Ecology & Hydrology




## Rights Holders

### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

rightsHolder


### Email

enquiries@ceh.ac.uk


### Organisation Name

Natural Resources Wales


### Organisation Identifier

[https://ror.org/04x65hs26](https://ror.org/04x65hs26)


### Role

rightsHolder


### Email

enquiries@naturalresourceswales.gov.uk


### Organisation Name

Environment Agency


### Organisation Identifier

[https://ror.org/01zewfb16](https://ror.org/01zewfb16)


### Role

rightsHolder


### Email

enquiries@environment-agency.gov.uk


### Organisation Name

Northern Ireland Environment Agency


### Organisation Identifier

[https://ror.org/01d29cd45](https://ror.org/01d29cd45)


### Role

rightsHolder


### Email

nieainfo@daera-ni.gov.uk


### Organisation Name

Natural England


### Organisation Identifier

[https://ror.org/00r66pz14](https://ror.org/00r66pz14)


### Role

rightsHolder


### Email

enquiries@naturalengland.org.uk


### Organisation Name

Joint Nature Conservation Committee


### Organisation Identifier

[https://ror.org/05tzsrw37](https://ror.org/05tzsrw37)


### Role

rightsHolder


### Email

data@jncc.gov.uk


### Organisation Name

Scotland and Northern Ireland Forum for Environmental Research (SNIFFER)


### Organisation Identifier

[https://ror.org/00e99w454](https://ror.org/00e99w454)


### Role

rightsHolder


### Email

bib@ceh.ac.uk 


### Organisation Name

Scottish Environment Protection Agency


### Organisation Identifier

[https://ror.org/01kxjy285](https://ror.org/01kxjy285)


### Role

rightsHolder


### Email

bib@ceh.ac.uk


### Organisation Name

Scottish Natural Heritage


### Organisation Identifier

[https://ror.org/01t6g8w08](https://ror.org/01t6g8w08)


### Role

rightsHolder


### Email

enquiries@nature.scot




## Info Links

### Url

[https://data-package.ceh.ac.uk/sd/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee.zip](https://data-package.ceh.ac.uk/sd/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee.zip)


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

Bealey


### Given Name

W.J.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-3708-5864](https://orcid.org/0000-0003-3708-5864)


### Full Name

Bealey, W.J.


### Family Name

Martin Hernandez


### Given Name

C.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Martin Hernandez, C.


### Family Name

Vigier


### Given Name

A.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0001-6798-409X](https://orcid.org/0000-0001-6798-409X)


### Full Name

Vigier, A.


### Family Name

Levy


### Given Name

P.E.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-8505-1901](https://orcid.org/0000-0002-8505-1901)


### Full Name

Levy, P.E.


### Family Name

Stedman


### Given Name

J.R.


### Organisation Name

Ricardo Energy & Environment


### Role

author


### Email

john.stedman@ricardo.com


### Full Name

Stedman, J.R.




## Publication Date

2022-09-05T00:00:00.000+00:00


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

2025-11-13T16:27:46.000+00:00


## Citation

### Authors

- Bealey, W.J.
- Martin Hernandez, C.
- Vigier, A.
- Levy, P.E.
- Stedman, J.R.


### Doi

10.5285/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee


### Title

Deposition and concentration of nitrogen and sulphur for protected sites in the UK, 2018-2020


### Publisher

NERC EDS Environmental Information Data Centre


### Resource Type General

dataset


### Year

2022


### Month

9


### Day

5


### Bibtex

[https://catalogue.ceh.ac.uk/documents/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee/citation?format=bib](https://catalogue.ceh.ac.uk/documents/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee/citation?format=bib)


### Ris

[https://catalogue.ceh.ac.uk/documents/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee/citation?format=ris](https://catalogue.ceh.ac.uk/documents/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee/citation?format=ris)


### Url

[https://doi.org/10.5285/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee](https://doi.org/10.5285/f83a56ef-15ad-4270-aefd-a6ef4b24b4ee)


