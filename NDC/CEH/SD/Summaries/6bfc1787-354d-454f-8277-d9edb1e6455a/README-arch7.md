# Supporting documentation for 'Macroinvertebrate sampling in the River Beas, India, 2017' data

## Overview
- Macroinvertebrate kick-sampling data collected at four sites on the River Beas, India, on 3–4 November 2017.
- Method: UK Environment Agency standard semiquantitative protocol (Murray-Bligh, 1999).
- Collected by S. Ncube; documentation prepared by Visser-Quinn, Beevers, Adeloye; corresponding author: a.visser-quinn@hw.ac.uk.

## Data collection details
- Four sampling sites: SiteNumber 1, 2, 3, and 4 with corresponding SiteName.
- Sampling dates:
  - Sites 1 and 2: 3 November 2017
  - Sites 3 and 4: 4 November 2017
- Data components include precise site locations and taxonomy-based observations.

## Column definitions (explanation of headings)
- SiteNumber: Site number (1, 2, 3, 4)
- SiteName: Name of the sampling site
- Longitude: Site longitude (degrees, minutes, seconds)
- Latitude: Site latitude (degrees, minutes, seconds)
- SamplingDate: Sampling date per site (3 Nov 2017 for sites 1–2; 4 Nov 2017 for sites 3–4)
- MacroinvertebrateOrder: Taxonomic order of observed macroinvertebrates
- MacroinvertebrateFamily: Taxonomic family of observed macroinvertebrates
- NumberOfTaxa: Count of macroinvertebrate taxa recorded during kick sampling

## Spatial data considerations
- Data are point observations with explicit longitude and latitude.
- For GIS use, convert coordinates to decimal degrees if needed and assign an appropriate coordinate reference system (e.g., WGS84) for mapping and analysis.
- The dataset is suitable for creating site-based maps, spatial analyses of biodiversity, and integration with other geospatial layers (hydrology, land use, etc.).

## Data quality and protocol context
- Data follow the UK Environment Agency’s semi-quantitative protocol, ensuring comparability across sites and samples.
- Protocol reference: Murray-Bligh (1999) Quality management systems for environmental monitoring: biological techniques; Procedure for collecting and analysing macro-invertebrate samples.
- Documentation provides a schema for consistent interpretation of column headings and data fields.

## Usage for GIS and data integration
- Create a GIS point layer with attributes:
  - SiteNumber, SiteName, Longitude, Latitude, SamplingDate, MacroinvertebrateOrder, MacroinvertebrateFamily, NumberOfTaxa
- Potential analyses:
  - Spatial distribution of taxa richness (NumberOfTaxa)
  - Taxonomic composition by site (orders and families)
  - Temporal comparison if integrated with additional sampling dates
- Consider data harmonization when combining with other datasets (e.g., ensuring consistent taxonomic levels, date formats, and coordinate precision).

## References
- Murray-Bligh, J. 1999. Quality management systems for environmental monitoring: biological techniques, BT001. Procedure for collecting and analysing macro-invertebrate samples. Environment Agency: Bristol.

## Contact and provenance
- Corresponding author: a.visser-quinn@hw.ac.uk
- Data attributed to Visser-Quinn, A; Ncube, S; Beevers, L.; Adeloye, A.J.