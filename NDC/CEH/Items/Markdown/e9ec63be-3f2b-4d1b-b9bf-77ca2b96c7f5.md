## Id

e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5


## Uri

[https://catalogue.ceh.ac.uk/id/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5](https://catalogue.ceh.ac.uk/id/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5)


## Type

dataset


## Title

Data describing pollen identified from honey samples originating from the UKCEH National Honey Monitoring Scheme for 2019


## Description

The following data set describes regional and temporal occurrence of plants foraged upon by managed honey bees (Apis mellifera).  This data was derived from DNA meta-barcoding of pollen extracted from honey samples provided by bee keepers archived as part of the UK National Honey Monitoring Scheme ([https://honey-monitoring.ac.uk/](https://honey-monitoring.ac.uk/) All data provided is from the first full year of the scheme in 2019. 

Working in partnership with UK beekeepers, the National Honey Monitoring Scheme aims to use honeybees to monitor long-term changes in the condition and health of the UK countryside. Data associated with subsequent years will be made available as samples are processed.

The Honey Monitoring Scheme is supported by national capability funding from UK Centre for Ecology & Hydrology under the ASSIST programme. 


## Metadata Date

2025-11-13T16:26:12


## Resource Identifiers

### Code

[https://catalogue.ceh.ac.uk/id/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5](https://catalogue.ceh.ac.uk/id/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5)


### Code

10.5285/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5


### Code Space

doi:




## Lineage

All honey samples were submitted following an application though the National Honey Monitoring Scheme online portal which required minimum meta-data on site location and sample date which was verified.   This included in some cases additional data on hive health metrics.  DNA meta-barcoding to rapidly process samples to identify plant species.  Quality assurance of the DNA metabarcoding was delivered through operational deployment of sophisticated protocols for barcoding and interpreting large volumes of honey samples. To do this we developed the HONEYPI pipeline implemented in python 2.7 and is open access ([https://github.com/hsgweon/honeypi](https://github.com/hsgweon/honeypi)  The HONEYPI pipeline is divided into several parts as follows: 1) the raw amplicon sequences are quality filtered and adapters removed; 2) DADA2 pipeline is subsequently used to generate an Amplicon Sequence Variant (ASV) abundance table containing chimera-removed, high-quality error-corrected sequences. 3). For each ASV, conserved regions flanking ITS2 are removed; and (4) resulting sequences taxonomically classified using the naive Bayesian classifier against in-house ITS2 database.  Since HONEYPI uses ASVs rather than clusters of sequences for classification, it allows combining of ASV tables, i.e. data from two or more separate sequencing runs can be merged without re-clustering sequences. 

A full open access methodological paper describing this approach is given in Oliver et al (2021) MethodsX, 8, 101303 ([https://doi.org/10.1016/j.mex.2021.101303](https://doi.org/10.1016/j.mex.2021.101303)


## Spatial Representation Types

- textTable


## Topic Categories

biota

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/biota](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/biota)




## Keywords Place

United Kingdom



## Keywords Theme

Agriculture

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/1](http://onto.nerc.ac.uk/CEHMD/topic/1)


Biodiversity

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/2](http://onto.nerc.ac.uk/CEHMD/topic/2)


Pollinators

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/14](http://onto.nerc.ac.uk/CEHMD/topic/14)




## Keywords Other

Honey

DNA Metabarcoding

Forage plants

National Honey Monitoring Scheme

Assist

Apis mellifera

### Uri

[http://www.wikidata.org/entity/Q30034](http://www.wikidata.org/entity/Q30034)


Honeybee

### Uri

[http://www.wikidata.org/entity/Q30034](http://www.wikidata.org/entity/Q30034)


pollen

### Uri

[http://www.eionet.europa.eu/gemet/concept/6392](http://www.eionet.europa.eu/gemet/concept/6392)


forage crop

### Uri

[http://www.eionet.europa.eu/gemet/concept/11177](http://www.eionet.europa.eu/gemet/concept/11177)




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




## Funding

### Funder Name

Natural Environment Research Council


### Funder Identifier

[https://ror.org/02b5d8509](https://ror.org/02b5d8509)


### Award Title

Achieving Sustainable Agricultural Systems (ASSIST)


### Award Number

NE/N018125/1


### Award U R I

[https://gtr.ukri.org/projects?ref=NE/N018125/1](https://gtr.ukri.org/projects?ref=NE/N018125/1)


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

Woodcock


### Given Name

B.A. 


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-0300-9951](https://orcid.org/0000-0003-0300-9951)


### Full Name

Woodcock, B.A.


### Family Name

Oliver


### Given Name

A.E.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-4923-277X](https://orcid.org/0000-0003-4923-277X)


### Full Name

Oliver, A.E.


### Family Name

Newbold


### Given Name

L.K.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0001-8895-1406](https://orcid.org/0000-0001-8895-1406)


### Full Name

Newbold, L.K.


### Family Name

Gweon


### Given Name

H.S.


### Organisation Name

University of Reading


### Organisation Identifier

[https://ror.org/05v62cm79](https://ror.org/05v62cm79)


### Role

author


### Email

h.s.gweon@reading.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-6218-6301](https://orcid.org/0000-0002-6218-6301)


### Full Name

Gweon, H.S.


### Family Name

Roy


### Given Name

D.B.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-5147-0331](https://orcid.org/0000-0002-5147-0331)


### Full Name

Roy, D.B.


### Family Name

Pywell


### Given Name

R.F.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0001-6431-9959](https://orcid.org/0000-0001-6431-9959)


### Full Name

Pywell, R.F.


### Organisation Name

NERC EDS Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

publisher


### Email

info@eidc.ac.uk


### Organisation Name

NERC EDS Environmental Information Data Centre


### Organisation Identifier

[https://ror.org/04xw4m193](https://ror.org/04xw4m193)


### Role

custodian


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


### Family Name

Woodcock


### Given Name

B.A. 


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

pointOfContact


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-0300-9951](https://orcid.org/0000-0003-0300-9951)


### Full Name

Woodcock, B.A.


### Point Of Contact

UK Centre for Ecology & Hydrology




## Temporal Extents

### Begin

2019-01-01


### End

2019-12-31




## Online Resources

### Url

[https://data-package.ceh.ac.uk/data/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5](https://data-package.ceh.ac.uk/data/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5)


### Name

Download the data


### Description

Download a copy of this data


### Function

download


### Type

OTHER


### Url

[https://data-package.ceh.ac.uk/sd/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5.zip](https://data-package.ceh.ac.uk/sd/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5.zip)


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

unknown


### Title

UK regions




## Supplemental

### Name

National Honey Monitoring Scheme website


### Url

[https://honey-monitoring.ac.uk/](https://honey-monitoring.ac.uk/)


### Function

website


### Description

Oliver, A. E., Newbold, L. K., Gweon, H. S., Read, D. S., Woodcock, B. A., & Pywell, R. F. (2021). Integration of DNA extraction, metabarcoding and an informatics pipeline to underpin a national citizen science honey monitoring scheme. In MethodsX (Vol. 8, p. 101303). Elsevier BV


### Url

[https://doi.org/10.1016/j.mex.2021.101303](https://doi.org/10.1016/j.mex.2021.101303)


### Function

relatedArticle




## Dataset Reference Date

### Publication Date

2022-01-18



## Resource Maintenance

### Frequency Of Update

asNeeded




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

- [http://onto.nerc.ac.uk/CEHMD/topic/1](http://onto.nerc.ac.uk/CEHMD/topic/1)
- [http://onto.nerc.ac.uk/CEHMD/topic/2](http://onto.nerc.ac.uk/CEHMD/topic/2)
- [http://onto.nerc.ac.uk/CEHMD/topic/14](http://onto.nerc.ac.uk/CEHMD/topic/14)


## Resource Status

Available


## Points Of Contact

### Family Name

Woodcock


### Given Name

B.A. 


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

pointOfContact


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-0300-9951](https://orcid.org/0000-0003-0300-9951)


### Full Name

Woodcock, B.A.


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

[https://data-package.ceh.ac.uk/sd/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5.zip](https://data-package.ceh.ac.uk/sd/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5.zip)


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

Woodcock


### Given Name

B.A. 


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-0300-9951](https://orcid.org/0000-0003-0300-9951)


### Full Name

Woodcock, B.A.


### Family Name

Oliver


### Given Name

A.E.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-4923-277X](https://orcid.org/0000-0003-4923-277X)


### Full Name

Oliver, A.E.


### Family Name

Newbold


### Given Name

L.K.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0001-8895-1406](https://orcid.org/0000-0001-8895-1406)


### Full Name

Newbold, L.K.


### Family Name

Gweon


### Given Name

H.S.


### Organisation Name

University of Reading


### Organisation Identifier

[https://ror.org/05v62cm79](https://ror.org/05v62cm79)


### Role

author


### Email

h.s.gweon@reading.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-6218-6301](https://orcid.org/0000-0002-6218-6301)


### Full Name

Gweon, H.S.


### Family Name

Roy


### Given Name

D.B.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-5147-0331](https://orcid.org/0000-0002-5147-0331)


### Full Name

Roy, D.B.


### Family Name

Pywell


### Given Name

R.F.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0001-6431-9959](https://orcid.org/0000-0001-6431-9959)


### Full Name

Pywell, R.F.




## Publication Date

2022-01-18T00:00:00.000+00:00


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

2025-11-13T16:26:12.000+00:00


## Citation

### Authors

- Woodcock, B.A.
- Oliver, A.E.
- Newbold, L.K.
- Gweon, H.S.
- Roy, D.B.
- Pywell, R.F.


### Doi

10.5285/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5


### Title

Data describing pollen identified from honey samples originating from the UKCEH National Honey Monitoring Scheme for 2019


### Publisher

NERC EDS Environmental Information Data Centre


### Resource Type General

dataset


### Year

2022


### Month

1


### Day

18


### Bibtex

[https://catalogue.ceh.ac.uk/documents/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5/citation?format=bib](https://catalogue.ceh.ac.uk/documents/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5/citation?format=bib)


### Ris

[https://catalogue.ceh.ac.uk/documents/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5/citation?format=ris](https://catalogue.ceh.ac.uk/documents/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5/citation?format=ris)


### Url

[https://doi.org/10.5285/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5](https://doi.org/10.5285/e9ec63be-3f2b-4d1b-b9bf-77ca2b96c7f5)


