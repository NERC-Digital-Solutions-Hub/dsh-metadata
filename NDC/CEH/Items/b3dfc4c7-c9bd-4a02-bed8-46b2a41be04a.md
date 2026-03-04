## Id

b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a


## Uri

[https://catalogue.ceh.ac.uk/id/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a](https://catalogue.ceh.ac.uk/id/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a)


## Type

dataset


## Title

Land Cover Map 2018 (20m classified pixels, GB)


## Description

This is the 20m classified pixels dataset for the UKCEH Land Cover Map of 2018(LCM2018) representing Great Britain. It describes Great Britain's land cover in 2018 using UKCEH Land Cover Classes, which are based on UK Biodiversity Action Plan broad habitats. This dataset is the Random Forest classification result from classifying a 20m pixel raster containing multi-season spectral information combined with context layers, which help to resolve spectral confusion.  It is provided as a 2-band, 8-bit integer raster.  The band-1 is the UKCEH Land Cover Class identifier, band-2 is an indicator of classification confidence.  For a fuller description please refer to the product documentation.

LCM2018 represents a suite of geospatial land cover datasets (raster and polygon) describing the UK land surface in 2018.  These were produced at the UK Centre for Ecology & Hydrology by classifying satellite images from 2018. LCM2018 was simultaneously released with LCM2017 and LCM2019.  These are the latest in a series of UKCEH land cover maps, which began with the 1990 Land Cover Map of Great Britain (now usually referred to as LCM1990) followed by UK-wide land cover maps LCM2000, LCM2007 and LCM2015.

This work was supported by the Natural Environment Research Council award number NE/R016429/1 as part of the UK-SCAPE programme delivering National Capability.


## Metadata Date

2025-10-30T14:43:11


## Resource Identifiers

### Code

[https://catalogue.ceh.ac.uk/id/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a](https://catalogue.ceh.ac.uk/id/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a)


### Code

10.5285/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a


### Code Space

doi:




## Relationships

### Relation

[https://vocabs.ceh.ac.uk/eidc#memberOf](https://vocabs.ceh.ac.uk/eidc#memberOf)


### Target

ffd42c91-a8ae-469b-855f-762e4ed418ef


### Relation

[https://vocabs.ceh.ac.uk/eidc#memberOf](https://vocabs.ceh.ac.uk/eidc#memberOf)


### Target

[https://catalogue.ceh.ac.uk/id/ffd42c91-a8ae-469b-855f-762e4ed418ef](https://catalogue.ceh.ac.uk/id/ffd42c91-a8ae-469b-855f-762e4ed418ef)




## Lineage

The 20m Classified Pixels datasets are the most spatially detailed in LCM2017, LCM2018 and LCM2019 product range. All other datasets were derived from these. They give land cover information in 21 classes based on UK Biodiversity Action Plan broad habitats. They result from automatic Random Forest classifications of partially overlapping, rectangular classification scenes and are given as 8-bit, 2-band integer 20m pixel rasters. Band-1 is the most likely land cover class, band-2 is the classification probability associated with this class, rescaled over the interval 0 to 100. Classification scenes comprised per-season Sentinel-2 median top of atmosphere reflectance values resampled to 20m pixel resolution, derived using the Google Earth Engine, combined with regional context layers (for example: terrain, coastal proximity). Overlapping classification results were visually ranked to determine precedence. The best classifications were compiled to form seamless national products for Great Britain and Northern Ireland. Classification used bespoke software integrated with a PostGis spatial database. The 20m rasters were exported from PostGIS using open source gdal tools to give the final product in GeoTiff format. GeoTiff is open standard format for raster data and GeoTiff files can be read by most GIS software.


## Spatial Representation Types

- grid


## Topic Categories

environment

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/environment](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/environment)


imageryBaseMapsEarthCover

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/imageryBaseMapsEarthCover](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/imageryBaseMapsEarthCover)




## Keywords Theme

Land cover

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/11](http://onto.nerc.ac.uk/CEHMD/topic/11)


Mapping

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/18](http://onto.nerc.ac.uk/CEHMD/topic/18)




## Keywords Other

UK-SCAPE



## Distribution Formats

### Name

TIFF


### Type

image/tiff


### Version

unknown




## Inspire Themes

### Theme

Land Cover


### Uri

[http://inspire.ec.europa.eu/theme/lc](http://inspire.ec.europa.eu/theme/lc)




## Spatial Resolutions

### Distance

20




## Funding

### Funder Name

Natural Environment Research Council


### Funder Identifier

[https://ror.org/02b5d8509](https://ror.org/02b5d8509)


### Award Title

UK-SCaPE


### Award Number

NE/R016429/1


### Award U R I

[https://gtr.ukri.org/projects?ref=NE/R016429/1](https://gtr.ukri.org/projects?ref=NE/R016429/1)


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

Morton


### Given Name

R.D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-3947-6463](https://orcid.org/0000-0003-3947-6463)


### Full Name

Morton, R.D.


### Family Name

Marston


### Given Name

C.G.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-2070-2187](https://orcid.org/0000-0002-2070-2187)


### Full Name

Marston, C.G.


### Family Name

O'Neil


### Given Name

A.W.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-3591-1034](https://orcid.org/0000-0003-3591-1034)


### Full Name

O'Neil, A.W.


### Family Name

Rowland


### Given Name

C.S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-0459-506X](https://orcid.org/0000-0002-0459-506X)


### Full Name

Rowland, C.S.


### Honorific Prefix

Dr


### Family Name

Morton


### Given Name

Dan


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

Lancaster Environment Centre, Library Avenue, Bailrigg


#### City

Lancaster


#### Administrative Area

Lancashire


#### Postal Code

LA1 4AP


#### Country

United Kingdom



### Full Name

Morton, D.


### Point Of Contact

UK Centre for Ecology & Hydrology


### Organisation Name

NERC EDS Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

custodian


### Email

info@eidc.ac.uk


### Organisation Name

NERC Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

publisher


### Email

info@eidc.ac.uk


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

rightsHolder


### Email

enquiries@ceh.ac.uk




## Temporal Extents

### Begin

2018-01-01


### End

2018-12-31




## Online Resources

### Url

[https://order-eidc.ceh.ac.uk/resources/YRRG5AJW/order](https://order-eidc.ceh.ac.uk/resources/YRRG5AJW/order)


### Name

Download the data


### Description

Order a copy of this data


### Function

order


### Type

OTHER


### Url

[https://data-package.ceh.ac.uk/sd/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a.zip](https://data-package.ceh.ac.uk/sd/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a.zip)


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




## Incoming Citations

### Description

Rayner, M., Balzter, H., Jones, L., Whelan, M., & Stoate, C. (2021). Effects of improved land-cover mapping on predicted ecosystem service outcomes in a lowland river catchment. In Ecological Indicators (Vol. 133, p. 108463). Elsevier BV.


### Url

[https://doi.org/10.1016/j.ecolind.2021.108463](https://doi.org/10.1016/j.ecolind.2021.108463)


### Type

academic


### Description

Baker, S.J., Perry, M.C., Betts, R.A., Schoenecker, J., & Pellegrini, A.F.A. (2025). Spikes in UK wildfire emissions driven by peatland fires in dry years. Environmental Research Letters, 20(3), 034028.


### Url

[https://doi.org/10.1088/1748-9326/adafc6](https://doi.org/10.1088/1748-9326/adafc6)


### Type

academic




## Dataset Reference Date

### Publication Date

2020-06-23


### Released Date

2020-07-08



## Use Constraints

Licence terms and conditions apply

### Code

license


### Uri

[https://eidc.ac.uk/licences/lcm-raster/plain](https://eidc.ac.uk/licences/lcm-raster/plain)




## Resource Type

dataset


## Access Limitation

Registration is required to access this data

### Code

Available


### Uri

[https://www.eidc.ac.uk/help/faq/registration](https://www.eidc.ac.uk/help/faq/registration)



## Not G E M I N I

False


## Licences

Licence terms and conditions apply

### Code

license


### Uri

[https://eidc.ac.uk/licences/lcm-raster/plain](https://eidc.ac.uk/licences/lcm-raster/plain)




## Incoming Citation Count

2


## Topics

- [http://onto.nerc.ac.uk/CEHMD/topic/11](http://onto.nerc.ac.uk/CEHMD/topic/11)
- [http://onto.nerc.ac.uk/CEHMD/topic/18](http://onto.nerc.ac.uk/CEHMD/topic/18)


## Resource Status

Available


## Points Of Contact

### Honorific Prefix

Dr


### Family Name

Morton


### Given Name

Dan


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

Lancaster Environment Centre, Library Avenue, Bailrigg


#### City

Lancaster


#### Administrative Area

Lancashire


#### Postal Code

LA1 4AP


#### Country

United Kingdom



### Full Name

Morton, D.


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




## Info Links

### Url

[https://data-package.ceh.ac.uk/sd/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a.zip](https://data-package.ceh.ac.uk/sd/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a.zip)


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

NERC Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

publisher


### Email

info@eidc.ac.uk




## Authors

### Family Name

Morton


### Given Name

R.D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-3947-6463](https://orcid.org/0000-0003-3947-6463)


### Full Name

Morton, R.D.


### Family Name

Marston


### Given Name

C.G.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-2070-2187](https://orcid.org/0000-0002-2070-2187)


### Full Name

Marston, C.G.


### Family Name

O'Neil


### Given Name

A.W.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-3591-1034](https://orcid.org/0000-0003-3591-1034)


### Full Name

O'Neil, A.W.


### Family Name

Rowland


### Given Name

C.S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-0459-506X](https://orcid.org/0000-0002-0459-506X)


### Full Name

Rowland, C.S.




## Publication Date

2020-06-23T00:00:00.000+00:00


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

2025-10-30T14:43:11.000+00:00


## Citation

### Authors

- Morton, R.D.
- Marston, C.G.
- O'Neil, A.W.
- Rowland, C.S.


### Doi

10.5285/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a


### Title

Land Cover Map 2018 (20m classified pixels, GB)


### Publisher

NERC Environmental Information Data Centre


### Resource Type General

dataset


### Year

2020


### Month

6


### Day

23


### Bibtex

[https://catalogue.ceh.ac.uk/documents/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a/citation?format=bib](https://catalogue.ceh.ac.uk/documents/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a/citation?format=bib)


### Ris

[https://catalogue.ceh.ac.uk/documents/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a/citation?format=ris](https://catalogue.ceh.ac.uk/documents/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a/citation?format=ris)


### Url

[https://doi.org/10.5285/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a](https://doi.org/10.5285/b3dfc4c7-c9bd-4a02-bed8-46b2a41be04a)


