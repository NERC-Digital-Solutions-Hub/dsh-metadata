# Annual abundance indices and trends for moths in Britain and Ireland from the Rothamsted Insect Survey light-trap network, 1968-2021, including country-level results for England, Scotland and Wales

## What the dataset contains
- Long-term dataset of annual abundance indices and trends for moths estimated from the Rothamsted Insect Survey (RIS) light-trap network, covering 1968–2021.
- Analyzed across 477 species of moths (mostly macro-moths) with indices and trends, plus 4,934,822 abundance counts from 844 species in the full dataset.
- Trends are presented as year coefficients from a Generalized Abundance Index (GAI) model, expressed as Annual Growth Rates (AGR), and total percentage changes over the time series.
- 95% confidence intervals (CIs) for indices and trends estimated via bootstrapping (1,000 replicates).
- Regional analyses include results for Britain, Ireland & Channel Islands as well as country-level results for England, Scotland, and Wales.
- Data quality criteria determine which species’ results are reported (477 species network-wide; 441 England, 242 Scotland, 232 Wales meet criteria).

## Data structure and formats
- Delivered as CSV files in region-specific sets:
  - Indices files (suffix _indices)
  - Trends files (suffix _trends)
  - Region prefixes: bi_ (Britain, Ireland & Channel Islands), eng_ (England), scot_ (Scotland), wales_ (Wales)
- Columns in abundance indices:
  - species, name, common_name, year, nsites, nsites_pos, index, index_low, index_upp, nboot
- Columns in trends:
  - species, name, common_name, nboot, agr, agr_low, agr_upp, perc_cng, perc_cng_low, perc_cng_upp, n_years, first_year, last_year
- Supplementary taxonomic names lookup file: supplementary_spp_names.csv, mapping Rothamsted IDs to BRC codes, UKSI names, Agassiz et al. checklist IDs, Bradley & Fletcher codes, and region indicators (england, scotland, wales, bi).

## Spatial and sampling context
- RIS operates two insect networks; this dataset focuses on the light-trap network for moths.
- Light-traps are fixed, standardized units with a 200 W tungsten bulb, sampling near local scales (attributed to local fauna rather than high-flying dispersal).
- Current network: around 60 active traps; historically sampled around 560 locations with an average of ~90 traps operating per year.
- Traps are distributed across the British Isles with good coverage in England, Scotland, Wales, and the Channel Islands; Ireland has comparatively limited coverage.
- Each trap is sited near power sources and accessible for maintenance, introducing local anthropogenic influences.
- The light-trap network has captured over 14 million moths across more than 1,500 species since inception.

## Data content details for mapping and GIS use
- Indices provide annual, network-wide and country-level relative abundance per species, suitable for map-based visualization when joined with trap/site locations.
- nsites and nsites_pos indicate how many traps operated and recorded the species in a given year, enabling assessment of data density for confidence in maps.
- Indices have 95% CIs, useful for shaded confidence intervals in choropleth or change-detection maps.
- Trends include AGR and total percentage change over the time series, enabling animated or time-sliced trend mapping.
- First_year and last_year indicate the span of data used for a given species in the model, informing temporal extents of maps.

## Analytical method (GAI) at a glance
- Two-stage Generalized Abundance Index (GAI) approach:
  - Stage 1: Generalized Additive Models (GAMs) estimate annual abundance curves for each species, standardized so area under the curve totals one; accounts for within-year recording gaps.
  - Stage 2: Poisson GAMs estimate abundance indices and trends with site and year as explanatory terms; indices scaled to the network by site counts.
- Temporal trends derived by modeling year as a continuous variable; yield Annual Growth Rate (AGR) and total percentage change.
- Confidence intervals based on 1,000 bootstrap replicates.
- Quality thresholds determine which species’ results are reported at the network and regional levels.

## Caveats and limitations for GIS use
- Data are aggregated at regional and network levels; to map spatial patterns at fine resolution, you should link indices/trends to trap/site coordinates (coordinates not included in the CSVs themselves).
- Most analyses focus on macro-moths; a subset of micro-moths with consistent identification are included; many micro-moths are excluded.
- Some species have time periods shortened (e.g., due to taxonomic or data issues), and a few taxa are reported as aggregates rather than as single species.
- Data quality criteria mean not all species are reported for all regions (e.g., England, Scotland, Wales have different counts of qualifying species).
- Local sampling bias due to trap placement and maintenance proximity to human activity.

## Potential GIS uses and visualization ideas
- Map long-term indices by region or country and animate across years to show trend dynamics.
- Create choropleth maps of AGR or percent change per species across England, Scotland, and Wales (where data permit) or at aggregated taxon level.
- Combine with trap-location data to visualize spatial density of sampling effort (nsites, nsites_pos) and identify data gaps.
- Overlay species-specific trends with environmental covariates (climate, habitat types) to explore drivers.
- Produce time-series plots per species alongside spatial maps to support biodiversity monitoring and policy reporting.

## Supplemental data, codes, and access notes
- Supplementary names lookup file (supplementary_spp_names.csv) links Rothamsted species IDs to BRC, UKSI, Agassiz et al. checklists, and Bradley & Fletcher codes.
- Regional and network results require joining to external geographic data (trap coordinates, administrative boundaries) to produce GIS-ready maps.

## Acknowledgements and references
- Funded by Defra (Outcome Indicator Framework Wildlife Indicator Development).
- RIS is a nationally funded data resource; related model development supported by NERC UK-SCAPE.
- Foundational references cited for the RIS network, GAI methodology, and long-term moth research.