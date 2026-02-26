# Dataset Originator E CN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- Internationally coordinated dataset from the UK Environmental Change Network (ECN) focusing on butterfly monitoring.
- Data are collected through a standardized butterfly monitoring protocol across multiple ECN sites.
- Aims to enable analysis of environmental change impacts on butterfly populations by providing structured, self-serve data and supporting data use across topics.

## Data Providers and Origin
- ECN programme funded by a consortium of UK government departments and agencies.
- Contributing organisations include Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, Scottish Environment Protection Agency, Scottish Government, and others.
- Data use should be acknowledged; request to send one reprint of any publication citing ECN data.

## Protocol
- Butterflys are recorded on transects divided into up to 15 sections.
- Follows the national Butterfly Monitoring Scheme methodology via the Biological Records Centre.
- Transect walked weekly from 1 April to 29 September; observers record butterflies within a 5m x 5m x 5m imaginary box.
- Conditions: temperature 13–17°C and at least 60% sunshine.
- Use accompanying quality information when using the data.

## Data Structure
- SITECODE: Unique ECN site code (e.g., T01, T02, …).
- LCODE: Location ID.
- SDATE: Date of data recording.
- SECTION: Transect section ID.
- FIELDNAME: Species code (numerical).
- VALUE: Measured value for the field.

## Site Codes
- 12 sites (T01–T12) with site names, coordinates, and dataset date ranges (e.g., Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, etc.).
- Date ranges span predominantly 1993–2012, with varying start/end dates per site.

## Species List
- Contains numeric codes mapped to Latin and common names for butterfly species (e.g., 10 = Black-veined white, 2 = Small tortoiseshell, 29 = Small heath, 90 = Swallowtail, etc.).
- Extensive mapping covering a wide range of butterfly taxa; includes entries like XX for no butterflies present.

## Additional Information
- Additional data in accompanying ECN_IB2.csv, with fields: SITECODE, LCODE, SDATE, SHOUR, SMINS, RECORDER, RECCODE, TEMP, SUNPERC, WSPEEDB, WEEK.
- Providing richer context for sampling times, personnel, weather, and weekly timing.

## Quality Information
- Quality notes are provided in accompanying ECN_IB_qtext.csv, detailing quality issues with locations, dates, and related metadata.
- Fields include LCODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, SITECODE, DESCRIPTION.

## Usage and Outputs
- Outputs commonly include structured data tables (SITECODE, LCODE, SDATE, SECTION, FIELDNAME, VALUE) suitable for dashboards, pivot analyses, and self-service exploration.
- Outputs can be supplemented with additional information on sampling conditions (TEMP, SUNPERC, WSPEEDB, WEEK) for more robust analyses.
- Encouraged practices include acknowledging data use and leveraging quality metadata to assess data suitability for specific analyses.