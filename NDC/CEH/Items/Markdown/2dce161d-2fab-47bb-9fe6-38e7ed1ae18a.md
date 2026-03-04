## Id

2dce161d-2fab-47bb-9fe6-38e7ed1ae18a


## Uri

[https://catalogue.ceh.ac.uk/id/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a](https://catalogue.ceh.ac.uk/id/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a)


## Type

dataset


## Title

Daily and sub-daily hydrometeorological and soil moisture data (2013-2024) [COSMOS-UK]


## Description

This dataset contains daily and sub-daily hydrometeorological and soil moisture observations from the COSMOS-UK (cosmic-ray soil moisture) monitoring network from October 2013 to the end of 2024 . These data are from 51 sites across the UK recording a range of hydrometeorological and soil variables.

Each site in the network records the following hydrometeorological and soil data at 30-minute resolution: Radiation (short wave, long wave, and net), precipitation, atmospheric pressure, air temperature, wind speed and direction, humidity, soil heat flux, and soil temperature and volumetric water content (VWC), measured by point sensors at various depths.

Each site hosts a cosmic-ray sensing probe; a novel sensor technology which counts fast neutrons in the surrounding atmosphere. In combination with the recorded hydrometeorological data, neutron counts are used to derive VWC over a field scale (COSMOS VWC), provide at daily resolution.

The presence of snow leads to erroneously high measurements of COSMOS VWC due to all the extra water in the surrounding area. Included in the daily data are indications of snow days, on which, the COSMOS VWC are adjusted, and the snow water equivalent (SWE) is given.

The potential evapotranspiration (PE), derived from recorded hydrometeorological and soil are also included at daily resolution.

Two levels of quality control are carried out, firstly data is run through a series of automated checks, such as range tests and spike tests, and then all data is manually inspected each week  where any other faults are picked up, including sensor faults or connection issues. Quality control flags are provided for all recorded (30 minute) data , indicating the reason for any missing data.

This  work was supported by the Natural Environment Research Council award number NE/Y006208/1 as part of the UKCEH NC-UK programme delivering National Capability.



## Metadata Date

2025-11-13T16:26:24


## Resource Identifiers

### Code

[https://catalogue.ceh.ac.uk/id/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a](https://catalogue.ceh.ac.uk/id/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a)


### Code

10.5285/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a


### Code Space

doi:




## Relationships

### Relation

[https://vocabs.ceh.ac.uk/eidc#supersedes](https://vocabs.ceh.ac.uk/eidc#supersedes)


### Target

399ed9b1-bf59-4d85-9832-ee4d29f49bfb




## Lineage

Hydrometeorological and soil observations are recorded at sites around the UK using an array of sensors. Every hour, the raw data collected is sent to UKCEH in Wallingford, where it is subject to quality control. Soil volumetric water content data are derived from 30-minute hydrometeorological data and data from the cosmic-ray sensing probe by Python scripts run every hour. The data are calculated using the method outlined in Evans et al. 2016. Snow water equivalents are derived by Python scripts at the end of the day from the hydrometeorological data according to Wallbank et al., 2020. Potential evapotranspiration data are derived by Python scripts at the end of the day from the hydrometeorological data according to the Penman-Monteith method, (FAO Crop evapotranspiration - Guidelines for computing crop water requirements - FAO Irrigation and drainage paper 56). All data (including raw, quality controlled and derived) is saved in an Oracle database.



## Spatial Representation Types

- textTable


## Temporal Resolution

- 30m
- 1d


## Topic Categories

climatologyMeteorologyAtmosphere

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/climatologyMeteorologyAtmosphere](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/climatologyMeteorologyAtmosphere)


environment

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/environment](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/environment)


geoscientificInformation

### Uri

[http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/geoscientificInformation](http://inspire.ec.europa.eu/metadata-codelist/TopicCategory/geoscientificInformation)




## Keywords Project

COSMOS-UK



## Keywords Theme

Agriculture

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/1](http://onto.nerc.ac.uk/CEHMD/topic/1)


Climate and climate change

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/4](http://onto.nerc.ac.uk/CEHMD/topic/4)


Ecosystem services

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/6](http://onto.nerc.ac.uk/CEHMD/topic/6)


Environmental survey

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/7](http://onto.nerc.ac.uk/CEHMD/topic/7)


Hydrology

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/9](http://onto.nerc.ac.uk/CEHMD/topic/9)


Land use

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/12](http://onto.nerc.ac.uk/CEHMD/topic/12)


Soil

### Uri

[http://onto.nerc.ac.uk/CEHMD/topic/17](http://onto.nerc.ac.uk/CEHMD/topic/17)




## Keywords Other

Absolute humidity

Atmospheric pressure

Cosmic-Ray sensing probe

Longwave radiation

Shortwave radiation

Net radiation

Potential evapotranspiration

Rainfall

Relative humidity

Soil heat flux

Soil humidity

Soil temperature

Soil water content

Soil wetness

Soil depth 2cm

Soil depth 5cm

Soil depth 10cm

Soil depth 20cm

Soil depth 50cm

UK

Volumetric water content

VWC

Wind direction

Wind speed

Latent heat

Sensible heat

atmospheric humidity

### Uri

[http://www.eionet.europa.eu/gemet/concept/626](http://www.eionet.europa.eu/gemet/concept/626)


air temperature

### Uri

[http://www.eionet.europa.eu/gemet/concept/281](http://www.eionet.europa.eu/gemet/concept/281)


soil

### Uri

[http://www.eionet.europa.eu/gemet/concept/7843](http://www.eionet.europa.eu/gemet/concept/7843)


soil moisture

### Uri

[http://www.eionet.europa.eu/gemet/concept/7874](http://www.eionet.europa.eu/gemet/concept/7874)


atmospheric precipitation

### Uri

[http://www.eionet.europa.eu/gemet/concept/637](http://www.eionet.europa.eu/gemet/concept/637)


evapotranspiration

### Uri

[http://www.eionet.europa.eu/gemet/concept/3022](http://www.eionet.europa.eu/gemet/concept/3022)




## Fileset

### Fileset Name

Sub-hourly (30 minute) hydrometeorological and soil data


### Encoding Format

text/csv


### Includes

COSMOS-UK_*_HydroSoil_SH_*-2024.csv


### Fileset Regex

^COSMOS-UK_.+_HydroSoil_SH_.+-2024\.csv$


### Observed Property

DATE_TIME

#### Title

DateTime


#### Type

datetime


#### Format

YYYY-MM-DDThh:mm:ssZ


LWIN

#### Title

Incoming longwave radiation


#### Type

number


#### Units

Watts per square metre (W m^-2)


LWIN

#### Title

Mean incoming longwave radiation


#### Type

number


#### Units

Watts per square metre


LWOUT

#### Title

Mean outgoing longwave radiation


#### Type

number


#### Units

Watts per square metre


SWIN

#### Title

Mean incoming shortwave radiation


#### Type

number


#### Units

Watts per square metre


SWOUT

#### Title

Mean outgoing shortwave radiation


#### Type

number


#### Units

Watts per square metre


RN

#### Title

Mean Net radiation


#### Type

number


#### Units

Watts per square metre


PRECIP

#### Title

Total precipitation from Pluvio


#### Type

number


#### Units

Millimetres


PRECIP_TIPPING

#### Title

Total precipitation from tipping bucket


#### Type

number


#### Units

Millimetres


PRECIP_RAINE

#### Title

Total precipitation from rain[e]


#### Type

number


#### Units

Millimetres


PA

#### Title

Mean atmospheric pressure


#### Type

number


#### Units

HectoPascals


TA

#### Title

Mean air temperature


#### Type

number


#### Units

Degrees Celsius


WS

#### Title

Mean wind speed


#### Type

number


#### Units

Metres per second


WD

#### Title

Mean wind direction


#### Type

number


#### Units

Degrees


Q

#### Title

Maen absolute humidity


#### Type

number


#### Units

Grams per cubic metre


RH

#### Title

mean relative humidity


#### Type

number


#### Units

Percent


SNOW_DEPTH

#### Title

Snow depth


#### Type

number


#### Units

Millimetres


UX

#### Title

Mean X component of wind speed


#### Type

number


#### Units

Metres per second


UY

#### Title

Mean Y component of wind speed


#### Type

number


#### Units

Metres per second


UZ

#### Title

Mean Z component of wind speed


#### Type

number


#### Units

Metres per second


G1

#### Title

Mean heat flux 1


#### Type

number


#### Units

Watts per square metre


G2

#### Title

Mean heat flux 2


#### Type

number


#### Units

Watts per square metre


TDT1_TSOIL

#### Title

Soil temperature from TDT sensor 2 at 10 cm


#### Type

number


#### Units

Degrees Celsius


TDT2_TSOIL

#### Title

Soil temperature from TDT sensor 1 at 10 cm


#### Type

number


#### Units

Degrees Celsius


TDT1_VWC

#### Title

Volumetric water content from TDT sensor 1 at 10 cm


#### Type

number


#### Units

Percent


TDT2_VWC

#### Title

Volumetric water content from TDT sensor 2 at 10 cm


#### Type

number


#### Units

Percent


TDT3_TSOIL

#### Title

Soil temperature from TDT sensor 4 at 5 cm


#### Type

number


#### Units

Degrees Celsius


TDT4_TSOIL

#### Title

Soil temperature from TDT sensor 3 at 5 cm


#### Type

number


#### Units

Degrees Celsius


TDT3_VWC

#### Title

Volumetric water content from TDT sensor 3 at 5 cm


#### Type

number


#### Units

Percent


TDT4_VWC

#### Title

Volumetric water content from TDT sensor 4 at 5 cm


#### Type

number


#### Units

Percent


TDT5_TSOIL

#### Title

Soil temperature from TDT sensor 5 at 15 cm


#### Type

number


#### Units

Degrees Celsius


TDT6_TSOIL

#### Title

Soil temperature from TDT sensor 6 at 15 cm


#### Type

number


#### Units

Degrees Celsius


TDT5_VWC

#### Title

Volumetric water content from TDT sensor 5 at 15 cm


#### Type

number


#### Units

Percent


TDT6_VWC

#### Title

Volumetric water content from TDT sensor 6 at 15 cm


#### Type

number


#### Units

Percent


TDT7_TSOIL

#### Title

Soil temperature from TDT sensor 7 at 25 cm


#### Type

number


#### Units

Degrees Celsius


TDT8_TSOIL

#### Title

Soil temperature from TDT sensor 8 at 25 cm


#### Type

number


#### Units

Degrees Celsius


TDT7_VWC

#### Title

Volumetric water content from TDT sensor 7 at 25 cm


#### Type

number


#### Units

Percent


TDT8_VWC

#### Title

Volumetric water content from TDT sensor 8 at 25 cm


#### Type

number


#### Units

Percent


TDT9_TSOIL

#### Title

Soil temperature from TDT sensor 9 at 50 cm


#### Type

number


#### Units

Degrees Celsius


TDT10_TSOIL

#### Title

Soil temperature from TDT sensor 10 at 50 cm


#### Type

number


#### Units

Degrees Celsius


TDT9_VWC

#### Title

Volumetric water content from TDT sensor 9 at 50 cm


#### Type

number


#### Units

Percent


TDT10_VWC

#### Title

Volumetric water content from TDT sensor 10 at 50 cm


#### Type

number


#### Units

Percent


STP_TSOIL2

#### Title

Mean soil temperature at depth 2 cm


#### Type

number


#### Units

Degrees Celsius


STP_TSOIL5

#### Title

Mean soil temperature at depth 5 cm


#### Type

number


#### Units

Degrees Celsius


STP_TSOIL10

#### Title

Mean soil temperature at depth 10 cm


#### Type

number


#### Units

Degrees Celsius


STP_TSOIL20

#### Title

Mean soil temperature at depth 20 cm


#### Type

number


#### Units

Degrees Celsius


STP_TSOIL50

#### Title

Mean soil temperature at depth 50 cm


#### Type

number


#### Units

Degrees Celsius






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


### Award Number

NE/Y006208/1


### Award U R I

[https://gtr.ukri.org/projects?ref=NE/Y006208/1](https://gtr.ukri.org/projects?ref=NE/Y006208/1)


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

### Honorific Prefix

Dr


### Family Name

Smith


### Given Name

R.J.


### Display Name

Richard Smith


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

pointOfContact


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-6447-6740](https://orcid.org/0000-0002-6447-6740)


### Full Name

Richard Smith


### Point Of Contact

UK Centre for Ecology & Hydrology


### Family Name

Stanley


### Given Name

S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-8303-2969](https://orcid.org/0000-0002-8303-2969)


### Full Name

Stanley, S.


### Family Name

Antoniou


### Given Name

V.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

vantoniou@aua.gr


### Name Identifier

[https://orcid.org/0000-0001-6011-4075](https://orcid.org/0000-0001-6011-4075)


### Full Name

Antoniou, V.


### Family Name

Askquith-Ellis


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


### Full Name

Askquith-Ellis, A.


### Family Name

Ball


### Given Name

L.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-0203-5958](https://orcid.org/0000-0002-0203-5958)


### Full Name

Ball, L.


### Family Name

Bennett


### Given Name

E.S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0001-7398-9268](https://orcid.org/0000-0001-7398-9268)


### Full Name

Bennett, E.S.


### Family Name

Blake


### Given Name

J.R.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-1033-4712](https://orcid.org/0000-0002-1033-4712)


### Full Name

Blake, J.R.


### Family Name

Boorman


### Given Name

D.B.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

dbboorman@gmail.com


### Name Identifier

[https://orcid.org/0000-0002-6436-5266](https://orcid.org/0000-0002-6436-5266)


### Full Name

Boorman, D.B.


### Family Name

Brookes


### Given Name

M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-7439-0393](https://orcid.org/0000-0002-7439-0393)


### Full Name

Brookes, M.


### Family Name

Clarke


### Given Name

M.A.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

mrmaclarke@gmail.com


### Full Name

Clarke, M.A.


### Family Name

Cooper


### Given Name

H.M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-1382-3407](https://orcid.org/0000-0002-1382-3407)


### Full Name

Cooper, H.M.


### Honorific Prefix

Dr


### Family Name

Cowan


### Given Name

N.J.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-7473-7916](https://orcid.org/0000-0002-7473-7916)


### Full Name

Cowan, N.J.


### Family Name

Cumming


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

[https://orcid.org/0000-0001-5704-9006](https://orcid.org/0000-0001-5704-9006)


### Full Name

Cumming, A.


### Family Name

Evans


### Given Name

J.G.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-4194-1416](https://orcid.org/0000-0003-4194-1416)


### Full Name

Evans, J.G.


### Family Name

Farrand


### Given Name

P.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

pb.farrand@talktalk.net


### Full Name

Farrand, P.


### Family Name

Fry


### Given Name

M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-1142-4039](https://orcid.org/0000-0003-1142-4039)


### Full Name

Fry, M.


### Family Name

Harvey


### Given Name

D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0009-0003-9102-5413](https://orcid.org/0009-0003-9102-5413)


### Full Name

Harvey, D.


### Family Name

Houghton-Carr


### Given Name

H.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-4465-2169](https://orcid.org/0000-0003-4465-2169)


### Full Name

Houghton-Carr, H.


### Family Name

Howson


### Given Name

T.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-9822-316X](https://orcid.org/0000-0002-9822-316X)


### Full Name

Howson, T.


### Family Name

Jiménez-Arranz


### Given Name

G.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

gjarranz@gmail.com


### Name Identifier

[https://orcid.org/0009-0004-4445-8272](https://orcid.org/0009-0004-4445-8272)


### Full Name

Jiménez-Arranz, G.


### Family Name

Keen


### Given Name

Y.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Keen, Y.


### Family Name

Khamis


### Given Name

D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

doran.khamis@gmail.com


### Full Name

Khamis, D.


### Family Name

Leeson


### Given Name

S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Leeson, S.


### Family Name

Lord


### Given Name

W.D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-2987-488X](https://orcid.org/0000-0003-2987-488X)


### Full Name

Lord, W.D.


### Family Name

Morrison


### Given Name

R.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-1847-3127](https://orcid.org/0000-0002-1847-3127)


### Full Name

Morrison, R.


### Family Name

Nash


### Given Name

G.V.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-1611-2042](https://orcid.org/0000-0003-1611-2042)


### Full Name

Nash, G.V.


### Family Name

O'Callaghan


### Given Name

F.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

O'Callaghan, F.


### Family Name

Retter


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


### Full Name

Retter, A.


### Family Name

Rylett


### Given Name

D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

danielrylett@gmail.com


### Name Identifier

[https://orcid.org/0000-0002-7426-1153](https://orcid.org/0000-0002-7426-1153)


### Full Name

Rylett, D.


### Family Name

Scarlett


### Given Name

P.M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Scarlett, P.M.


### Honorific Prefix

Dr


### Family Name

Smith


### Given Name

R.J.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-6447-6740](https://orcid.org/0000-0002-6447-6740)


### Full Name

Smith, R.J.


### Family Name

St Quintin


### Given Name

P.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

pstquintin@googlemail.com


### Full Name

St Quintin, P.


### Family Name

Swain


### Given Name

O.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Swain, O.


### Family Name

Szczykulska


### Given Name

M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-5820-7093](https://orcid.org/0000-0002-5820-7093)


### Full Name

Szczykulska, M.


### Family Name

Teagle


### Given Name

S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

https;//orcid.org/0000-0002-8824-8435


### Full Name

Teagle, S.


### Family Name

Thornton


### Given Name

J.L.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

jenna.l.thornton@hotmail.co.uk


### Name Identifier

[https://orcid.org/0000-0002-8350-4823](https://orcid.org/0000-0002-8350-4823)


### Full Name

Thornton, J.L.


### Family Name

Trill


### Given Name

E.J.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

emilytrill@gmail.com


### Name Identifier

[https://orcid.org/0000-0002-6233-8942](https://orcid.org/0000-0002-6233-8942)


### Full Name

Trill, E.J.


### Family Name

Vincent


### Given Name

P.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Vincent, P.


### Family Name

Ward


### Given Name

H.C.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

helen.ward@uibk.ac.at


### Name Identifier

[https://orcid.org/0000-0001-8881-185X](https://orcid.org/0000-0001-8881-185X)


### Full Name

Ward, H.C.


### Family Name

Warwick


### Given Name

A.C.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Warwick, A.C.


### Family Name

Winterbourn


### Given Name

J.B.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

benwinterbourn@gmail.com


### Name Identifier

[https://orcid.org/0000-0002-1318-5281](https://orcid.org/0000-0002-1318-5281)


### Full Name

Winterbourn, J.B.


### Organisation Name

UK Centre for Ecology & Hydrology


### Role

rightsHolder


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

2013-01-01


### End

2024-12-31




## Online Resources

### Url

[https://catalogue.ceh.ac.uk/datastore/eidchub/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a](https://catalogue.ceh.ac.uk/datastore/eidchub/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a)


### Name

Download the data


### Description

Download a copy of this data


### Function

fileAccess


### Type

OTHER


### Url

[https://data-package.ceh.ac.uk/sd/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a.zip](https://data-package.ceh.ac.uk/sd/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a.zip)


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

[http://www.opengis.net/def/crs/EPSG/0/4326](http://www.opengis.net/def/crs/EPSG/0/4326)


### Title

WGS 84




## Dataset Reference Date

### Publication Date

2025-06-24



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


## Has Online Service Agreement

True


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
- [http://onto.nerc.ac.uk/CEHMD/topic/4](http://onto.nerc.ac.uk/CEHMD/topic/4)
- [http://onto.nerc.ac.uk/CEHMD/topic/6](http://onto.nerc.ac.uk/CEHMD/topic/6)
- [http://onto.nerc.ac.uk/CEHMD/topic/7](http://onto.nerc.ac.uk/CEHMD/topic/7)
- [http://onto.nerc.ac.uk/CEHMD/topic/9](http://onto.nerc.ac.uk/CEHMD/topic/9)
- [http://onto.nerc.ac.uk/CEHMD/topic/12](http://onto.nerc.ac.uk/CEHMD/topic/12)
- [http://onto.nerc.ac.uk/CEHMD/topic/17](http://onto.nerc.ac.uk/CEHMD/topic/17)


## Resource Status

Available


## Points Of Contact

### Honorific Prefix

Dr


### Family Name

Smith


### Given Name

R.J.


### Display Name

Richard Smith


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

pointOfContact


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-6447-6740](https://orcid.org/0000-0002-6447-6740)


### Full Name

Richard Smith


### Point Of Contact

UK Centre for Ecology & Hydrology




## Rights Holders

### Organisation Name

UK Centre for Ecology & Hydrology


### Role

rightsHolder




## Info Links

### Url

[https://data-package.ceh.ac.uk/sd/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a.zip](https://data-package.ceh.ac.uk/sd/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a.zip)


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

Stanley


### Given Name

S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-8303-2969](https://orcid.org/0000-0002-8303-2969)


### Full Name

Stanley, S.


### Family Name

Antoniou


### Given Name

V.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

vantoniou@aua.gr


### Name Identifier

[https://orcid.org/0000-0001-6011-4075](https://orcid.org/0000-0001-6011-4075)


### Full Name

Antoniou, V.


### Family Name

Askquith-Ellis


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


### Full Name

Askquith-Ellis, A.


### Family Name

Ball


### Given Name

L.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-0203-5958](https://orcid.org/0000-0002-0203-5958)


### Full Name

Ball, L.


### Family Name

Bennett


### Given Name

E.S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0001-7398-9268](https://orcid.org/0000-0001-7398-9268)


### Full Name

Bennett, E.S.


### Family Name

Blake


### Given Name

J.R.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-1033-4712](https://orcid.org/0000-0002-1033-4712)


### Full Name

Blake, J.R.


### Family Name

Boorman


### Given Name

D.B.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

dbboorman@gmail.com


### Name Identifier

[https://orcid.org/0000-0002-6436-5266](https://orcid.org/0000-0002-6436-5266)


### Full Name

Boorman, D.B.


### Family Name

Brookes


### Given Name

M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-7439-0393](https://orcid.org/0000-0002-7439-0393)


### Full Name

Brookes, M.


### Family Name

Clarke


### Given Name

M.A.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

mrmaclarke@gmail.com


### Full Name

Clarke, M.A.


### Family Name

Cooper


### Given Name

H.M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-1382-3407](https://orcid.org/0000-0002-1382-3407)


### Full Name

Cooper, H.M.


### Honorific Prefix

Dr


### Family Name

Cowan


### Given Name

N.J.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-7473-7916](https://orcid.org/0000-0002-7473-7916)


### Full Name

Cowan, N.J.


### Family Name

Cumming


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

[https://orcid.org/0000-0001-5704-9006](https://orcid.org/0000-0001-5704-9006)


### Full Name

Cumming, A.


### Family Name

Evans


### Given Name

J.G.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-4194-1416](https://orcid.org/0000-0003-4194-1416)


### Full Name

Evans, J.G.


### Family Name

Farrand


### Given Name

P.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

pb.farrand@talktalk.net


### Full Name

Farrand, P.


### Family Name

Fry


### Given Name

M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-1142-4039](https://orcid.org/0000-0003-1142-4039)


### Full Name

Fry, M.


### Family Name

Harvey


### Given Name

D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0009-0003-9102-5413](https://orcid.org/0009-0003-9102-5413)


### Full Name

Harvey, D.


### Family Name

Houghton-Carr


### Given Name

H.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-4465-2169](https://orcid.org/0000-0003-4465-2169)


### Full Name

Houghton-Carr, H.


### Family Name

Howson


### Given Name

T.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-9822-316X](https://orcid.org/0000-0002-9822-316X)


### Full Name

Howson, T.


### Family Name

Jiménez-Arranz


### Given Name

G.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

gjarranz@gmail.com


### Name Identifier

[https://orcid.org/0009-0004-4445-8272](https://orcid.org/0009-0004-4445-8272)


### Full Name

Jiménez-Arranz, G.


### Family Name

Keen


### Given Name

Y.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Keen, Y.


### Family Name

Khamis


### Given Name

D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

doran.khamis@gmail.com


### Full Name

Khamis, D.


### Family Name

Leeson


### Given Name

S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Leeson, S.


### Family Name

Lord


### Given Name

W.D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-2987-488X](https://orcid.org/0000-0003-2987-488X)


### Full Name

Lord, W.D.


### Family Name

Morrison


### Given Name

R.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-1847-3127](https://orcid.org/0000-0002-1847-3127)


### Full Name

Morrison, R.


### Family Name

Nash


### Given Name

G.V.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0003-1611-2042](https://orcid.org/0000-0003-1611-2042)


### Full Name

Nash, G.V.


### Family Name

O'Callaghan


### Given Name

F.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

O'Callaghan, F.


### Family Name

Retter


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


### Full Name

Retter, A.


### Family Name

Rylett


### Given Name

D.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

danielrylett@gmail.com


### Name Identifier

[https://orcid.org/0000-0002-7426-1153](https://orcid.org/0000-0002-7426-1153)


### Full Name

Rylett, D.


### Family Name

Scarlett


### Given Name

P.M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Scarlett, P.M.


### Honorific Prefix

Dr


### Family Name

Smith


### Given Name

R.J.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-6447-6740](https://orcid.org/0000-0002-6447-6740)


### Full Name

Smith, R.J.


### Family Name

St Quintin


### Given Name

P.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

pstquintin@googlemail.com


### Full Name

St Quintin, P.


### Family Name

Swain


### Given Name

O.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Swain, O.


### Family Name

Szczykulska


### Given Name

M.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

[https://orcid.org/0000-0002-5820-7093](https://orcid.org/0000-0002-5820-7093)


### Full Name

Szczykulska, M.


### Family Name

Teagle


### Given Name

S.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Name Identifier

https;//orcid.org/0000-0002-8824-8435


### Full Name

Teagle, S.


### Family Name

Thornton


### Given Name

J.L.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

jenna.l.thornton@hotmail.co.uk


### Name Identifier

[https://orcid.org/0000-0002-8350-4823](https://orcid.org/0000-0002-8350-4823)


### Full Name

Thornton, J.L.


### Family Name

Trill


### Given Name

E.J.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

emilytrill@gmail.com


### Name Identifier

[https://orcid.org/0000-0002-6233-8942](https://orcid.org/0000-0002-6233-8942)


### Full Name

Trill, E.J.


### Family Name

Vincent


### Given Name

P.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Vincent, P.


### Family Name

Ward


### Given Name

H.C.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

helen.ward@uibk.ac.at


### Name Identifier

[https://orcid.org/0000-0001-8881-185X](https://orcid.org/0000-0001-8881-185X)


### Full Name

Ward, H.C.


### Family Name

Warwick


### Given Name

A.C.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

enquiries@ceh.ac.uk


### Full Name

Warwick, A.C.


### Family Name

Winterbourn


### Given Name

J.B.


### Organisation Name

UK Centre for Ecology & Hydrology


### Organisation Identifier

[https://ror.org/00pggkr55](https://ror.org/00pggkr55)


### Role

author


### Email

benwinterbourn@gmail.com


### Name Identifier

[https://orcid.org/0000-0002-1318-5281](https://orcid.org/0000-0002-1318-5281)


### Full Name

Winterbourn, J.B.




## Publication Date

2025-06-24T00:00:00.000+00:00


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

2025-11-13T16:26:24.000+00:00


## Citation

### Authors

- Stanley, S.
- Antoniou, V.
- Askquith-Ellis, A.
- Ball, L.
- Bennett, E.S.
- Blake, J.R.
- Boorman, D.B.
- Brookes, M.
- Clarke, M.A.
- Cooper, H.M.
- Cowan, N.J.
- Cumming, A.
- Evans, J.G.
- Farrand, P.
- Fry, M.
- Harvey, D.
- Houghton-Carr, H.
- Howson, T.
- Jiménez-Arranz, G.
- Keen, Y.
- Khamis, D.
- Leeson, S.
- Lord, W.D.
- Morrison, R.
- Nash, G.V.
- O'Callaghan, F.
- Retter, A.
- Rylett, D.
- Scarlett, P.M.
- Smith, R.J.
- St Quintin, P.
- Swain, O.
- Szczykulska, M.
- Teagle, S.
- Thornton, J.L.
- Trill, E.J.
- Vincent, P.
- Ward, H.C.
- Warwick, A.C.
- Winterbourn, J.B.


### Doi

10.5285/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a


### Title

Daily and sub-daily hydrometeorological and soil moisture data (2013-2024) [COSMOS-UK]


### Publisher

NERC EDS Environmental Information Data Centre


### Resource Type General

dataset


### Year

2025


### Month

6


### Day

24


### Bibtex

[https://catalogue.ceh.ac.uk/documents/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a/citation?format=bib](https://catalogue.ceh.ac.uk/documents/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a/citation?format=bib)


### Ris

[https://catalogue.ceh.ac.uk/documents/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a/citation?format=ris](https://catalogue.ceh.ac.uk/documents/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a/citation?format=ris)


### Url

[https://doi.org/10.5285/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a](https://doi.org/10.5285/2dce161d-2fab-47bb-9fe6-38e7ed1ae18a)


