# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- ECN Ground Beetles data collected to monitor abundance of ground predators (Carabidae) using pitfall traps.
- Fortnightly data collection between May and October.
- Data intended for map-based visualization and GIS analyses; supports understanding environmental change impacts across multiple sites.

## Data content and structure
- Primary data download format (ECN dataset):
  - SITECODE: Unique code for each ECN site.
  - LCODE: Location ID (unique within site).
  - SDATE: Sampling date.
  - TRAP: Trap number.
  - FIELDNAME: Variable measured (e.g., quality codes or taxa).
  - VALUE: Measured value.
  - TYPE: Additional info for Pterostichus madidus (species 6453 2714) including gender and leg color morphs (M=female, F, R=red legs, B=black legs).
- Data rows include long-form taxon information (e.g., 6453 codes for ground beetle genera/species) and associated quality codes.
- Quality information accompanies data to indicate data reliability and potential issues.

## Supporting data and documentation
- ECN_IG2.csv: Trap deployment context
  - SITECODE, LCODE, FROMDATE (trap set date), SDATE (collection date).
- ECN_IG3.csv: Habitat information
  - SITECODE, LCODE, HABDESC (habitat description).
- ECN_IG_qtext.csv: Quality text
  - SITE/LOCATION, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING, DESCRIPTION (text explanations for quality issues; 999 indicates unusual event; associated detailed quality text in this file).
- Quality Codes (ECN_IG_qtext.csv provides context for QC values)
  - Standard codes (e.g., 100, 101, …) describe issues like data loss, sampling problems, equipment failures, or environmental disturbances.
  - 999 indicates an unusual event; accompanying text explains circumstances.

## Site codes and geography
- Explanatory site codes with coordinates (12 ECN sites):
  - T01 Drayton (52°11'37.95"N, 1°45'51.95"W)
  - T02 Glensaugh (56°54'33.36"N, 2°33'12.14"W)
  - T03 Hillsborough (54°27'12.24"N, 6°04'41.26"W)
  - T04 Moor House - Upper Teesdale (54°41'42.15"N, 2°23'16.26"W)
  - T05 North Wyke (50°46'54.96"N, 3°55'4.10"W)
  - T06 Rothamsted (51°48'12.33"N, 0°22'21.66"W)
  - T07 Sourhope (55°29'23.47"N, 2°12'43.32"W)
  - T08 Wytham (51°46'52.86"N, 1°20'9.81"W)
  - T09 Alice Holt (51°09'16.46"N, 0°51'47.58"W)
  - T10 Porton Down (51°07'37.83"N, 1°38'23.46"W)
  - T11 Snowdon (53°04'28.38"N, 4°02'00.64"W)
  - T12 Cairngorms (57°06'58.84"N, 3°49'46.98"W)
- Additional site information available via CEH catalogue link.

## Data standards, quality, and governance
- ECN has standard operating procedures (protocols) to ensure cross-site data comparability.
- Usage notes emphasize using accompanying quality information when using data.
- Quality codes and QC text provide context for data reliability; 999 used for unusual events with narrative explanations.
- Data citation and acknowledgement:
  - ECN requests acknowledgement in publications citing their data.
  - Request to send one reprint of any publication that cites the data.

## Access, usage, and GIS considerations
- Data download fields (SITECODE, LCODE, SDATE, TRAP, FIELDNAME, VALUE, TYPE) enable linking observations to precise locations and times for GIS mapping.
- Join considerations for GIS:
  - Use SITECODE + LCODE to align observations with site/habitat metadata.
  - Combine with ECN_IG2.csv (trap dates) and ECN_IG3.csv (habitat) for spatial-temporal context.
  - Quality information should be applied to filter or weight observations in analyses and visualizations.
  - The FIELDNAME taxonomy includes a comprehensive list of taxa (down to species) under codes like 6453 2714 (Pterostichus madidus) and many related genera/species.
  - For biological indicators, data are primarily presence/abundance by trap and date; TYPE provides additional sex/color morph information for a subset.
- Data scope and limitations:
  - Ground beetle data are collected fortnightly May–October, across multiple UK sites; resolutions and completeness may vary by site and date.
  - Data availability depends on site quality codes and transportability of traps; QC text helps interpret potential biases.
- Documentation and provenance:
  - Protocol document (ig.pdf) explains data collection methods.
  - Supporting CSVs provide spatial, temporal, and habitat context to enhance GIS analyses.

## Practical notes for GIS specialists
- Create GIS layers for trap locations by SITECODE/LCODE with attributes: trap number, sampling date, species codes, and values.
- Map habitat types per site using ECN_IG3.csv to enrich spatial analyses.
- Integrate quality codes to filter datasets or to create uncertainty layers for choropleth or heatmap visualizations.
- Maintain citation and acknowledgement workflow when publishing map-based data products or analyses derived from ECN data.