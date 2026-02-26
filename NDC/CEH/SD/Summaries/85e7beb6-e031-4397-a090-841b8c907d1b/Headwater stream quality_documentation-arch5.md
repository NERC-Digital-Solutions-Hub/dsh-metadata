# Headwater stream quality (Countryside Survey)

- Two survey years (1998 and 2007) assessed headwater streams downstream of sources on 1:50,000 maps.
- Main metrics: Observed vs. Expected BMWP scores for macroinvertebrates; BMWP is an index of river biological quality based on taxa sensitivity to pollution.
- Output products: A 1 km raster map showing water quality by headwater stream location; dataset includes observed, expected, and their ratio.

## Experimental Design and Sampling Regime

- Macroinvertebrates sampled using standard protocols; each sample area covers 5–15 m of stream bed and up to three minutes of active sampling plus one minute of hand search.
- Supplemental physical site measurements collected: width, depth, substrate composition (required for RIVPACS).
- BMWP scores calculated for each site; RIVPACS used to generate expected macroinvertebrate communities based on site characteristics.
- Sites selected to align with headwater streams appropriate for RIVPACS; 478 sites across two years were surveyed in both years.

## Data Collection and Processing

- Samples collected with a standard Freshwater Biological Association pond net; specimens sent to CEH for sorting/identification.
- Field protocol documented in Murphy & Weatherby (2008); further details in Murphy et al. (2008) QA report.
- Taxonomic data harmonised to a modern, common taxonomy to ensure comparability across surveys; a standardisation step defines a mutually exclusive taxa list for species richness calculations.
- Quality control followed Defra/NERC Joint Codes of Practice.

## Data Products and Attributes

- Primary dataset attributes:
  - Observed BWMP score
  - Expected BWMP score
  - Value: Observed BWMP score divided by Expected BWMP score (O/E BWMP)
- Spatial data:
  - Projection: OSGB 1936 / British National Grid (EPSG:27700)
  - Included scale: 1 km grid squares; areas without Strahler order 1–3 headwater streams excluded from models
- Model outputs:
  - Boosted Regression Tree model parameters to predict stream quality
  - Model inputs include land cover percentages, slope, altitude, Strahler order, easting/northing, and survey year
  - Model-derived Expected BWMP scores aggregated by land class for random river sampling sites
- Tables and documentation:
  - Table 1: Water quality measure (Observed vs. Expected BWMP)
  - Table 2: Model parameters (percent arable, improved grassland, urban, woody cover, slope, altitude, Strahler order, coordinates, year)

## Analytical Methods and Data Handling

- Biological data processed to produce species counts, BMWP taxa counts (TAXA), and RIVPACS status classes.
- Taxonomic harmonisation to ensure comparability across surveys; standardisation to derive a mutually exclusive taxa list for richness.
- Model training/testing: Subset of data used to train, with remainder used for testing; extrapolation to 1 km grid squares nationwide.
- Documentation and references:
  - RIVPACS methodology and related supporting documents
  - Model and dataset referenced in Dunbar et al. (2010) and Norton et al. (2016)

## Quality Assurance and Documentation

- QA procedures aligned with Defra/NERC Joint Codes of Practice; detailed in related reports (Dunbar et al. 2008, 2010; Murphy & Weatherby 2008; Murphy et al. 2008).
- Data harmonisation and standardisation steps conducted to ensure consistency across survey years.
- Supporting documents and references provide methodological context and validation.

## Supporting References and Data Sources

- Armitage et al. (1983): BMWP scoring framework
- Bunce et al. (2007): Land classification framework
- Dunbar et al. (2010): Countryside Survey Headwater Streams report
- Morton et al. (2011): Land Cover Map 2007
- Murphy & Weatherby (2008); Murphy et al. (2008): QA and Freshwater Manuals
- Norton et al. (2016): Ecosystem indicators and scale
- Additional project reports and technical notes linked to Countryside Survey outputs

## Implications for Data Stewards

- Governance and standardisation:
  - Maintain consistent protocols across survey years to support longitudinal analyses.
  - Preserve harmonised taxonomy and standardized taxa lists; document standardisation procedures for reproducibility.
- Metadata and provenance:
  - Capture detailed metadata on sampling protocols, site coordinates, physical measurements, and processing steps.
  - Document model parameters, spatial extent, and data exclusions (e.g., Strahler order 1–3 only).
- Data accessibility and reuse:
  - Ensure availability of both observed/expected BWMP data and the rasterized 1 km output, with clear usage notes and references.
  - Track data lineage from field collection through processing, QA, and modeling to final products.
- Limitations and caveats:
  - Restricted to headwater streams (Strahler orders 1–3); exclude unmonitored or non-headwater areas.
  - Model outputs rely on land cover and geographic predictors; users should consider scale and grid-based aggregation when applying results.
- Potential for integration:
  - Combine with other Countryside Survey datasets or national river quality indicators to support broader data discovery and reuse.