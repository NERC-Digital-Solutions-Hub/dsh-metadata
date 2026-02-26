# File Uploaded to EIDC: hydroscape_norfolk_core_metadata.csv

## Overview
- Metadata file for lake sediment core samples within the Hydroscape Norfolk project, uploaded to EIDC.
- Captures core-specific identifiers, location, sampling details, corer types, and dating status to enable data linking, mapping, and downstream analyses.

## Key fields and meanings
- WBID: Waterbody Identification number; links to the UK Centre for Ecology & Hydrology Lakes index.
- Hydroscape: Hydroscape region name.
- Name: Lake Name.
- General location of core: Core collected from the central (often deepest) area of the lake.
- OSGB36_E / OSGB36_N: Easting and Northing coordinates in UK Ordnance Survey OSGB36 datum.
- Water depth at core site (m): Water surface to sediment surface depth at the core site.
- Core length and type: Core length in metres and its type.
- Corer types: Big Ben and Livingstone, with bibliographic references for each corer.
  - Big Ben: Patmore et al. 2014; a wide-bore piston corer.
  - Livingstone: Livingstone 1955; a lightweight piston sampler.
- Date core collected: Date of fieldwork/core collection (dd/mm/yyyy); year-only shown when the precise date is unknown.
- UCL_Code: Internal UCL coding used on bags/databases.
- UCL Sample ID: Internal unique ID for the entire sample core (Amphora code).
- 210 Pb-dated (Y/N): Indicates whether the core has been dated using ^210Pb.
- Hydroscape: Hydroscape-related descriptor (field present but description in excerpt is incomplete).

## How this supports analysis
- Enables spatial alignment of cores with their lakes and hydroscape region for comparative analyses.
- Facilitates data integration across datasets via common identifiers (WBID, UCL codes).
- Documents sampling details (depth, core length, corer type) and dating status to assess data quality and comparability.

## Usage considerations
- Coordinate system (OSGB36) must be accounted for in spatial analyses.
- Dating status (210Pb: Yes/No) influences age-model construction and interpretation.
- Precise collection dates are preferred; if unknown, only the year is provided.
- Corer references should be consulted for methodological context when interpreting core data.