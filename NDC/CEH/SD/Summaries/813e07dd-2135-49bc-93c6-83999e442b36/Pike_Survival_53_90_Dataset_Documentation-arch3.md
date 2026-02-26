# Pike Survival Data 1953-1990

## Overview
- Dataset used in Vindenes et al. (2013) American Naturalist on trait-based dynamics of a top predator in freshwater ecosystems under climate change.
- Contains survival (binary) data derived from capture-mark-recapture of Pike (Esox lucius) from net and angling sampling.
- Data collection spans from 1944, with ongoing collection by CEH and its predecessor since 1989; originally by the Freshwater Biological Association (FBA).
- Includes both male, female, and undetermined sex individuals.
- Related datasets and metadata available (pike fecundity, growth, windermere lake temperature, and a metadata record).

## Data Content and Format
- File: PikeSurvivalData1953_1990.csv
- Format: CSV, size 68 KB
- Columns:
  - YEAR: Year of first capture of an individual
  - LENGTH: Length at capture (cm)
  - SURVIVAL: 1 if the individual was recorded again (survival over the first period after capture), 0 otherwise

## Study Location
- Windermere Lake, Cumbria, Great Britain
- Approximate centre grid references provided (OS Grid and WGS84 coordinates)

## Species and Sampling
- Species: Esox lucius (Pike)
- Sampling approach:
  - Netting in the north and south basins with variations in sites and effort from 1944 onward
  - Mark-and-release with individually numbered tags
  - Sightings of tagged fish by catch-and-release anglers persisted throughout

## Experimental Design and Sampling Regime
- From 1982 to present: standardized sampling using 64 mm bar mesh multifilament gill nets
- Setup: nets 40 m long, 3 m deep; located on the lake bottom; sampling Oct–Dec at ~10 sites per basin
- Procedure: five nets in water at a time; sites fished for two weeks per season; weekly rotation to cover entire lake
- Sampling effort:
  - 1982–1989: ~348 net days per year
  - Since 1990: ~240 net days per year
- Additional data: sightings of tagged pike by anglers maintained throughout

## Collection Methods and Fieldwork
- Measurements:
  - Length (fork length to 1 mm) and weight (to 100 g)
  - Sex determination via dissection
  - Age estimation from left opercular bone (birth date assumed 1 April)
- Analytical integration: combine with tag sightings to compute survival as defined in Haugen et al. (2007)

## Quality Control
- Quality checks involve measurement verification by permutations of three individuals (quality assurance protocol described in the dataset narrative)

## Related Datasets and Metadata
- Metadata record for data series: Pike 1944-2002
- Related datasets:
  - Pike - Fecundity Data 1963-2002
  - Pike - Growth Data 1944-1995
  - Windermere Lake Temperature 1944-2002
- Cited foundational references for methods and analyses:
  - Frost & Kipling (1959) – aging from scales and opercular bones
  - Le Cren (2001); Winfield et al. (2008); Haugen et al. (2007)

## Data Use and Provenance
- Part of a broader dataset used to explore long-term population dynamics and responses to environmental change
- Data lineage includes acquisition by FBA, subsequent maintenance by CEH and predecessors, and integration with tagging and mark-recapture records
- Primary citation within the data description: Vindenes et al. (2013) American Naturalist

## Relevance for Monitoring Frameworks
- Long-term, standardized time series suitable for evaluating population viability and responses to climate-related changes
- Demonstrates how continuous monitoring, tag-based recapture data, and aging methods can produce survival metrics over decades
- Highlights importance of:
  - Clear data provenance and links to metadata for traceability
  - Consistent sampling protocols (since 1982) to improve comparability over time
  - Integrating multiple data streams (capture data, tag sightings) to derive key indicators like survival
  - Documentation of collection methods, effort, and site coverage to support data governance and transparent analyses

## Challenges and Considerations for Monitoring
- Data continuity across decades depends on standardized methods and consistent effort
- Sex information incomplete for some individuals; potential biases in analyses if not accounted for
- Access to and sharing of underlying data and metadata are essential for reproducibility and external scrutiny
- Metadata completeness and linkage to related datasets are crucial for contextual analyses (e.g., environmental covariates like temperature)