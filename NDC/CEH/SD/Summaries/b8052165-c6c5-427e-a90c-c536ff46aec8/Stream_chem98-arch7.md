# Headwater stream water chemistry data 1998 [Countryside Survey] Data Table Descriptions

## Overview
- Dataset describing freshwater headwater stream water chemistry from the Countryside Survey (1998).
- Chemical measurements include field measurements of conductivity and pH, plus laboratory analyses of soluble reactive phosphorus (SRP) and alkalinity (50 ml filtered).
- Data table intended to support GIS-based mapping and analysis of headwater stream chemistry.

## Data table: STREAM_CHEMISTRY_98.csv
- Brief Description: Freshwater Stream - Water chemistry data; chemical analyses from stream waters sampled in 1998.
- Measured elements at each headwater site:
  - Conductivity and pH (field measurements)
  - Soluble reactive phosphorus (SRP), alkalinity (50 ml filtered)
- Key fields:
  - YEAR: Year of Survey (CS +Yr) [Text]
  - SQUARE: 1km square sampling site code [Text]
  - SITE_ID: Site identifier (count within 1 km square) [Number]
  - SAMPLE_DATE: Date sample taken [Date]
  - SAMPLE_TYPE: Sample type [Text]
  - DETERMINAND_NAME: Chemical determinand [Text]
  - DETERMINAND_UNITS: Units of chemical determinand [Text]
  - VALUE: Value of chemical determinand [Number]
  - LC07: Land class 2007 (see ITE Land Classification) [Text]
  - LC07_NUM: Land class 2007 (numeric code) [Number]
  - EZ_DESC_07: Environmental zone [Text]
  - COUNTY07: County (England & Wales) or Council (Scotland) for the 1km square [Text]
  - COUNTRY: England (Eng), Scotland (Sco) or Wales (Wal) [Text]

## Data types and structure
- YEAR, SQUARE, SAMPLE_DATE, SAMPLE_TYPE, DETERMINAND_NAME, DETERMINAND_UNITS, LC07, EZ_DESC_07, COUNTY07, COUNTRY are Text.
- SITE_ID, VALUE, LC07_NUM are Numbers.
- SAMPLE_DATE is a Date type.

## Spatial and classification context
- SQUARE provides 1km square grid reference for spatial joining.
- SITE_ID counts within each 1km square.
- LC07 and LC07_NUM give 2007 land classification.
- EZ_DESC_07 provides environmental zone information.
- COUNTY07 and COUNTRY offer regional context for mapping.

## Data usage and attribution
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text to be used on copies, publications, and presentations: 
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Related resources and references
- Countryside Survey 1998 and 2000 modules and accompanying manuals:
  - Furse et al. 1998. Module 2: survey of freshwater habitats. Field handbook v.2.0.
  - Murphy & Weatherby 2008. Freshwater Manual.
- Additional supporting documents and reports:
  - Headwater Streams Report from 2007 (Dunbar et al.)
  - Countryside Survey 2000. Module 2: Freshwater Studies (CEH R&D/Technical Reports)
- Data provenance linked to ITE Land Classification of Great Britain 2007 for LC07, and environmental zone descriptors.

## GIS considerations and usage
- Suitable for map-based visualization of headwater stream chemistry by 1km square and site.
- Join strategies:
  - Use SQUARE for grid-based aggregation or joins to spatial layers.
  - Use SITE_ID to distinguish multiple sites within a square.
  - Combine with LC07, EZ_DESC_07, COUNTY07, and COUNTRY for contextual mapping (land class, environmental zones, administrative regions).
- Temporal context: 1998 sampling date; dataset supports historical comparisons with other Countryside Survey years.

## Limitations and notes
- Data from 1998; field measurements (conductivity, pH) and 50 ml filtered laboratory analyses (SRP, alkalinity) may have method-specific limitations not detailed here.
- Data quality and completeness depend on survey conditions and reporting in accompanying manuals.
- Proper data use requires acknowledgement as specified above.