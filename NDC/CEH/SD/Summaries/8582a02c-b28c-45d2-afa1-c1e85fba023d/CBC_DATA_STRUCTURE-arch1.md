# ECN CBC Bird Data: Dataset Originator, Usage, and Codes

- The dataset comes from the UK Environmental Change Network (ECN) Data Centre and documents Common Birds Census (CBC) data collected across multiple ECN sites.
- Used to understand environmental change through bird populations, with site-specific time series and standardized protocols for comparability.

## Provenance and Access

- Dataset Originator: ECN Data Centre (http://data.ecn.ac.uk; ecn@ceh.ac.uk), Centre for Ecology and Hydrology.
- Dataset Owners: UK Environmental Change Network programme, funded by a consortium of government departments and agencies (e.g., DEFRA, Natural England, Environment Agency, Natural Resources Wales, Scottish Government, etc.).
- Usage requirements:
  - Acknowledge data use in publications.
  - Send one reprint of any publication that cites the data.
- Data availability and portals: data and documentation are accessible via the CEH Environmental Information Platform; additional site information is available through provided links.

## Protocol and Data Collection

- Methodology: CBC (Common Birds Census) as organized by the British Trust for Ornithology.
- Data collection approach:
  - Conduct a series of visits to all parts of a defined plot during the breeding season.
  - Record bird contacts by sight or sound on large-scale maps.
  - Derive CLUST (territories) and, for some species, NEST (nest counts) alongside territory estimates.
- Design considerations:
  - CBC is a national-scale survey; site-level ECN data have limitations for linking population changes directly to environmental changes.
  - Recommend combining ECN data with broader monitoring (e.g., BTO data) to mitigate limitations.
- Temporal scope and changes:
  - CBC was the standard at lowland ECN sites until 1999; replaced by the Breeding Bird Survey (BBS) thereafter, with some sites continuing CBC for comparison.
  - Historical data exist for some sites (e.g., pre-ECN data for Wytham).
  - Date ranges vary by site; ECN data cover multiple sites with different years of operation.
- Quality information: Use accompanying quality documentation when using the data.

## Site Coverage and Temporal Range

- Alice Holt: 1994–2007
- Drayton: 1993–1999
- Hillsborough: 1993–2001
- North Wyke: 1993–2002
- Porton Down: 1994–1998
- Rothamsted: 1991–1997
- Wytham: 1971–2003

## Data Content and Structure

- Data download fields:
  - SITECODE: Unique ECN site code
  - SYEAR: Sampling year
  - BI_SPEC: Bird species code
  - CLUST: Number of territories (clusters)
  - NEST: Number of nests (where applicable)
- Supporting documentation:
  - ECN_cbc_qtext.csv includes SITECODE, SYEAR, BI_SPEC, and DESCRIPTION of data issues affecting data
- Site and data metadata (Explanatory information):
  - Site codes with names, coordinates, and BTO classification (e.g., T01 Drayton, T03 Hillsborough, T05 North Wyke, T06 Rothamsted, T08 Wytham, T09 Alice Holt, T10 Porton Down).
  - Link to further site information: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27

## Species Codes and Interpretation

- The dataset uses two-letter (and short-code) species codes mapped to species names (a comprehensive, long list including common birds such as BLUE TIT (BT), BLACKBIRD (AV/BB), CHAFFINCH (CC), GREAT TIT (GT), ROBIN (Q), WREN (WP), WOODPIGEON (WP), WILLOW WARbler (WW), etc.).
- The code table enables interpretation of species observations in the CLUST and NEST fields.

## Practical Considerations for Analysts

- When using ECN CBC data:
  - Be mindful of the national-scale design and the recommended supplementation with broader data sources (e.g., BTO data) for robust relationship analyses with environmental change.
  - Verify data quality using the accompanying QA documentation.
  - Acknowledge the dataset and cite appropriately; provide reprints if possible.
- Data integration:
  - Prepare to unify data across sites with variable year ranges and ensure consistent interpretation of CLUST and NEST metrics.
  - Use the SITECODE and BI_SPEC mappings to align bird observations across datasets.
- Location and context:
  - Site-specific ecological contexts (habitat type via BTO Class, coordinates) are provided to aid interpretation and potential environmental covariate alignment.

## Additional Information

- Further information about ECN sites is available at the CEH catalogue link provided in the documentation.
- The dataset is designed to be discoverable and usable, with emphasis on data provenance, standardization, and cross-site comparability.