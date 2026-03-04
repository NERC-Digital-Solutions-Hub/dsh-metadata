## Id

bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8


## Uri

[https://catalogue.ceh.ac.uk/id/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8](https://catalogue.ceh.ac.uk/id/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8)


## Type

dataset


## Title

Land Cover Map 1990 (1km percentage target class, GB) v2


## Description

This dataset consists of the 1km raster, percentage target class version of the Land Cover Map 1990 (LCM1990) for Great Britain. The 1km percentage product provides the percentage cover for each of 21 land cover classes for 1km x 1km pixels. This product contains one band per target habitat class (producing a 21 band image). The 21 target classes are based on the Joint Nature Conservation Committee (JNCC) Broad Habitats, which encompass the entire range of UK habitats. This dataset is derived from the vector version of the Land Cover Map, which contains individual parcels of land cover and is the highest available spatial resolution. 

LCM1990 is a land cover map of the UK which was produced at the UK Centre for Ecology & Hydrology by classifying satellite images (mainly from 1989 and 1990) into 21 Broad Habitat-based classes. It is the first in a series of land cover maps for the UK, which also includes maps for 2000, 2007, 2015, 2017, 2018 and 2019.  

LCM1990 consists of a range of raster and vector products and users should familiarise themselves with the full range (see related records, the UKCEH web site and the LCM1990 Dataset documentation) to select the product most suited to their needs.

This work was supported by the Natural Environment Research Council award number NE/R016429/1 as part of the UK-SCAPE programme delivering National Capability.


## Metadata Date

2026-01-09T10:18:02


## Resource Identifiers

### Code

[https://catalogue.ceh.ac.uk/id/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8](https://catalogue.ceh.ac.uk/id/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8)


### Code

10.5285/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8


### Code Space

doi:




## Relationships

### Relation

[https://vocabs.ceh.ac.uk/eidc#supersedes](https://vocabs.ceh.ac.uk/eidc#supersedes)


### Target

0172cc8c-8b5c-46cf-b08a-785ab832e88c


### Relation

[https://vocabs.ceh.ac.uk/eidc#memberOf](https://vocabs.ceh.ac.uk/eidc#memberOf)


### Target

[https://catalogue.ceh.ac.uk/id/2ec9916d-d938-4212-ba1b-31468ddde8fe](https://catalogue.ceh.ac.uk/id/2ec9916d-d938-4212-ba1b-31468ddde8fe)


### Relation

[https://vocabs.ceh.ac.uk/eidc#supersedes](https://vocabs.ceh.ac.uk/eidc#supersedes)


### Target

[https://catalogue.ceh.ac.uk/id/0172cc8c-8b5c-46cf-b08a-785ab832e88c](https://catalogue.ceh.ac.uk/id/0172cc8c-8b5c-46cf-b08a-785ab832e88c)


### Relation

[https://vocabs.ceh.ac.uk/eidc#memberOf](https://vocabs.ceh.ac.uk/eidc#memberOf)


### Target

2ec9916d-d938-4212-ba1b-31468ddde8fe




## Lineage

The percentage target class is produced from the 25m raster (which is derived from the vector product) by:
1. Using gdal_calc to split the 21 target classes into 21 individual images for each class where the presence of the class in question is recorded as 100 and absence is assigned 0.
2. Gdal_warp is then applied to each of the 21 presence/absence images to resample to 1km, using the 'average' option under resample. This produces images of percentage cover for each class.
3. Gdal_merge is then used to create a single file with 21 bands, where each band provides the percentage cover for the class i.e. band 1 provides percentage cover for class 1 etc.



## Reason Changed

The original 1990 Land Cover Map data set had a different spatial structure and set of land cover classes to the Land Cover Maps from 2015 onwards. To facilitate change mapping Land Cover Map 1990 has been recreated with the same thematic and spatial structures as the Land Cover Maps from 2015 onward. This new version supersedes the old version.


## Version

2


## Spatial Representation Types

- grid


## Topic Categories

imageryBaseMapsEarthCover

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/imageryBaseMapsEarthCover](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/imageryBaseMapsEarthCover)


geoscientificInformation

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/geoscientificInformation](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/geoscientificInformation)




## Keywords Theme

Land cover

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/11](http://onto.nerc.ac.uk/CEHMD/topic/11)


Land use

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/12](http://onto.nerc.ac.uk/CEHMD/topic/12)


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

1000




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

Rowland, C.S.


### Point Of Contact

UK Centre for Ecology & Hydrology


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

rightsHolder


### Email

enquiries@ceh.ac.uk


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




## Temporal Extents

### Begin

1990-01-01


### End

1990-12-31




## Online Resources

### Url

[https://data-package.ceh.ac.uk/data/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8](https://data-package.ceh.ac.uk/data/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8)


### Name

Download the data


### Description

Download a copy of this data


### Function

download


### Type

OTHER


### Url

[https://data-package.ceh.ac.uk/sd/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8.zip](https://data-package.ceh.ac.uk/sd/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8.zip)


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

### Publication Date

2020-10-09



## Resource Maintenance

### Frequency Of Update

notPlanned




## Use Constraints

Land Cover Map licence

### Code

license


### Uri

[https://eidc.ac.uk/licences/lcm-raster/plain](https://eidc.ac.uk/licences/lcm-raster/plain)




## Resource Type

dataset

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/ResourceType/dataset](http://inspire.ec.europa.eu/metadata-codelist/ResourceType/dataset)



## Access Limitation

Registration is required to access this data

### Code

Available


### Uri

[https://www.eidc.ac.uk/help/faq/registration](https://www.eidc.ac.uk/help/faq/registration)



## Not G E M I N I

False


## Licences

Land Cover Map licence

### Code

license


### Uri

[https://eidc.ac.uk/licences/lcm-raster/plain](https://eidc.ac.uk/licences/lcm-raster/plain)




## Incoming Citation Count

0


## Topics

- [http://onto.nerc.ac.uk/CEHMD/topic/11](http://onto.nerc.ac.uk/CEHMD/topic/11)
- [http://onto.nerc.ac.uk/CEHMD/topic/12](http://onto.nerc.ac.uk/CEHMD/topic/12)
- [http://onto.nerc.ac.uk/CEHMD/topic/18](http://onto.nerc.ac.uk/CEHMD/topic/18)


## Resource Status

Available


## Points Of Contact

### Family Name

Rowland


### Given Name

C.S.


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

Rowland, C.S.


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

[https://data-package.ceh.ac.uk/sd/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8.zip](https://data-package.ceh.ac.uk/sd/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8.zip)


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




## Publication Date

2020-10-09T00:00:00.000+00:00


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

2026-01-09T10:18:02.000+00:00


## Citation

### Authors

- Rowland, C.S.
- Marston, C.G.
- Morton, R.D.
- O'Neil, A.W.


### Doi

10.5285/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8


### Title

Land Cover Map 1990 (1km percentage target class, GB) v2


### Publisher

NERC Environmental Information Data Centre


### Resource Type General

dataset


### Year

2020


### Month

10


### Day

9


### Bibtex

[https://catalogue.ceh.ac.uk/documents/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8/citation?format=bib](https://catalogue.ceh.ac.uk/documents/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8/citation?format=bib)


### Ris

[https://catalogue.ceh.ac.uk/documents/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8/citation?format=ris](https://catalogue.ceh.ac.uk/documents/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8/citation?format=ris)


### Url

[https://doi.org/10.5285/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8](https://doi.org/10.5285/bb381b5b-d44e-4dbd-a9d1-efffd4c3e4a8)


