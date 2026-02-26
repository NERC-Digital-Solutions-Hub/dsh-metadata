# Description of the Data and file structure

- The dataset records freshwater macroinvertebrate abundance from the Environment Agency in England, collected 2002–2019, primarily during spring (March–May) and autumn (September–November).
- Data format: a single rds file accessible via R, containing long-form records (year, month, day, site, sample, taxon, abundance) processed to family- and wider taxonomic groupings.
- Data origin: processed from EA Ecology and Fish Explorer Macroinvertebrate database; abundance data are pooled to the family level.
- Sampling method: three-minute kick-samples (net sampling for 3 minutes downstream of a river area).
- Pre-2002 data excluded due to limited abundance recording; analysis focused on 2002–2019 for quality and consistency.

## What the data contain

- Core fields (with human-readable descriptions in the dataset):
  - riverbasin, agency_area, waterbody, wfd_waterbody_id, site_id
  - full_easting, full_northing (spatial coordinates)
  - latitude, longitude (decimal degrees)
  - season, year, month, day (sampling period)
  - sample_id, order_taxon, family_taxon, total_abundance, year_scaled, group
- Data type and units:
  - Missing data coded as NA
  - Recorded values are discrete counts of individuals (abundance)

## Data structure and access

- File structure: a single rds file containing the processed dataset
- Access link: https://environment.data.gov.uk/ecology-fish
- Data can be loaded and explored in R; designed for analysis and product creation (dashboards, pivot tables)

## Collection and processing methods

- Source: Environmental Agency ecological monitoring database
- Primary method: three-minute kick-samples; ~99% of samples
- Inclusion criteria: sites sampled for at least three years out of 18 in both spring and autumn
- Taxa retained: Ephemeroptera, Plecoptera, Hemiptera, Megaloptera, Odonata, Coleoptera, Trichoptera, Turbellaria, Annelida, Crustacea, Diptera, Mollusca
- Aggregation: abundances summed at the family level within these taxa
- Coverage: final dataset includes 67,757 samples from 5,009 sites across ten WFD river basins in England (e.g., Anglian, Humber, North West, Northumbria, Severn, Solway Tweed, South East, South West, Thames)
- Analysis toolkit: dataset manipulated and analyzed using R (2019–2022)

## Quality control and limitations

- Quality control: since 2002, one in every ten samples independently re-analysed
- Data window: restricted to 2002–2019 (original data include 1991 onward, but earlier years not used)
- Bias and representativeness: dataset biased toward mid to lower perennial reaches due to monitoring program design
- Nature of data: discrete abundance counts; designed for broad policy and environmental assessment rather than exhaustive biodiversity capture

## How this data can be used (Data Support perspective)

- End-user ready outputs
  - Self-serve dashboards or pivot tables by river basin, season, year, taxon group, or family
  - Maps showing sampling sites with abundance indicators
- Data products and workflows
  - Load the rds, filter by site-year, and aggregate to family level for trends analyses
  - Combine with external environmental covariates (e.g., water quality) while accounting for sampling bias
  - Produce summaries and charts with guidance on interpretation and uncertainty
- Data quality and governance
  - Provide clear notes on QC steps (e.g., 2002–2019 window, re-analysis procedure)
  - Document potential biases due to site distribution and monitoring design
- Practical considerations for data support
  - Emphasize data loading, cleaning (handling NA values), and reproducible workflows
  - Offer early prototypes (e.g., sample dashboards) and collect feedback for iteration
  - Highlight licensing and sharing conditions via the public data portal and linked publication (Powell et al., 2022)