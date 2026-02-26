# Beech tree ring data from hot and dry European distribution edges, 2019

## Aim
- Utilize the relationship between European Beech tree growth and environmental factors, including climate, to monitor and forecast drought-related declines in forest growth across Europe.
- Measure inter-annual growth using dendroecology (ring width).

## Data collection scope
- To address climatic gaps in the European Beech Tree Ring Network (EBTRN), 12 European Beech sites were sampled in late 2019.
- Sites span Bulgaria, Albania, Kosovo, and Spain.
- Focused on lower elevational ends of local beech distributions to better represent hot and dry edge conditions.

## Field sampling and processing
- At each site, sampled at least 15 standard canopy-level trees; two cores per tree.
- Cores processed using standard dendrology procedures: air-dried, mounted, and sanded (grits 80, 120, 300, 600, 1200).
- Cores scanned into 2400 PPI images for CDendro measurements with 0.01 mm precision.
- Cross-dating performed virtually and statistically for each site; COFECH used to control cross-dating quality.

## Data files and structure
- site_meta.csv: metadata for the 12 sites ( Bulgaria, Albania, Kosovo, Spain) as of late 2019, including latitude, longitude, elevation, and nearest town.
- 12 site-specific measurement files: ring width measurements for each core by year, units in mm, resolution 0.01 mm.
  - File naming: by site ID.
  - Each file layout: first column = year; subsequent columns = ring width measurements for each core.
  - Tree core IDs: combination of site ID and tree ID; cores labeled with 'a' and 'b' for the two cores from the same tree.
  - NA indicates missing values for a given year.

## Data quality and assurance
- Cross-dating performed virtually and statistically; quality controlled with COFECH.
- High-precision measurements (0.01 mm) and standardized processing ensure comparability across sites.

## Potential analyses and uses
- Investigate climate-growth relationships across multiple European sites, focusing on drought response.
- Combine site metadata with ring-width series to model growth trends and forecast declines under drying scenarios.
- Create self-serve data products (dashboards, time-series views) for end users; support broader policy or conservation planning.
- Extend or harmonize data with other EBTRN data to fill climatic gaps and improve spatial coverage.

## Considerations and limitations
- Data cover 12 sites with a focus on edge conditions; may require integration with additional sites for broader inference.
- Missing values (NA) present in year-by-year records; handling required for cross-site analyses.
- Data acquisition concentrated in late 2019; temporal coverage is site-specific and may need augmentation for long-term trend analyses.