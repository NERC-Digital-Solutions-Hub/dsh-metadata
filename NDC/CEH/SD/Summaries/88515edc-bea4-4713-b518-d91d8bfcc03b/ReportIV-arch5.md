# SUMMARY

## Overview
- Four-year field programme at Sourhope (Scottish Borders) within the NERC Soil Biodiversity Thematic Programme.
- Focus on linking below-ground soil biodiversity with above-ground plant communities, monitoring changes in productivity (above-ground biomass), species composition, and diversity.
- Experimental setup includes five replicate blocks with six main plots per block, subdivided into sub-plots assigned to sixteen projects. Treatments include mowing, insecticide application, nitrogen fertiliser, lime, and combinations thereof.
- Key aim for data stewards: ensure these long-term, multi-treatment datasets are well-governed, stored, shared, and maintainable for diverse users.

## Datasets and Variables (data types and key measures)
- Above-ground biomass (productivity)
  - Collected yearly May–Sept via harvesting a 0.5 m2 cell per sub-plot; samples oven-dried at 80°C and weighed.
  - Data used to generate annual biomass per plot and summarized as ln-transformed values for analysis.
- Plant species composition and diversity
  - Point analysis surveys using a 0.5 m2 cell with 25-point baseline and later 100-hole grid surveys (2000–2002).
  - Bryophyte inclusion expanded in 2002; complete species lists available (Appendix 3).
  - Shannon Diversity Index calculated for each treatment/year.
  - Functional groups categorized (stress-tolerators S; competitive-stress-ruderal CSR; SR/CSR) with tracking of how groups shift by treatment.
- Soil properties
  - Soil pH measured at ~5 cm depth (baseline 1998; ongoing monitoring; in 2002 central plots measured).
  - Soil moisture measured with theta probe (August 2002) in point-analysis cells.
- Climate and site conditions
  - On-site Automatic Weather Station data since 1999: rainfall, radiation, air and soil temperatures.
- Management activity and treatments
  - Site-wide mowing to ~6 cm (May–Sept), plus insecticide applications (Dursban 4) on designated plots.
  - Plot-level treatments: Control 1, Control 2, Nitrogen, Lime, Nitrogen+Lime, Insecticide (formerly Biocide).
  - Annual treatment dates and rates documented (Appendix 2 and Appendix 1).
- Additional data
  - Baseline vegetation survey (1998) and subsequent year-by-year data (2000–2002); Appendix 6–8 provide per-plot biomass, rank analyses, and species-hits data.
  - Research group activities, including Phase I vs Phase II project data collection and lab-based experiments (e.g., labelled 13CO2 pulses).

## Data Collection, Structure, and Provenance
- Experimental design: 5 blocks, 6 main plots per block, main plots subdivided into 10 sub-plots; treatments allocated at random with 0.5 m x 0.5 m cell tagging for group allocation.
- Data collection cadence
  - Regular weather data (facility-maintained since 1999).
  - Biomass sampling preceding each mow (May–Sept; five cuts per year).
  - Annual point analyses (baseline in 1998; annual surveys 2000–2002).
  - Soil sampling and pH monitoring since 1998; 2002 added soil moisture measurements in survey cells.
- Data documentation
  - Appendices document site activities, treatment details, and species lists (Appendices 1–8).
  - Full species lists and bryophyte identifications provided; biodiversity indices calculated.
- Data volumes and scope
  - Field data collected across multiple projects, with cumulative soil samples totaling 11,621 by 2002.
  - Phase II (2002) fieldwork included major field activities, including 13CO2 pulses and gas measurements.

## Data Quality, Processing, and Analysis
- Benchmarking and normalization
  - Biomass results compared relative to Control 1; data ln-transformed for ANOVA analyses.
- Statistical analyses
  - Split-plot ANOVA with factors: Treatment, Year, and their interaction (significant treatment and year effects observed in 2002).
  - PCA applied to point-analysis data with treatment-based ranking to differentiate improved vs unimproved plots.
- Data integrity and caveats
  - 2002 weather data included missing periods due to equipment malfunction; substitutions from Konza weather station noted.
  - Insecticide treatment (Dursban 4) interpretation requires caution due to lack of exact control over herbivory; acknowledged as potentially indirect effects on diversity.
  - trampling effects in C2 plots in 2002 attributed to intensive sampling activities (13CO2 pulses) rather than treatment alone.
- Key findings by data type
  - Biomass: fertilised plots (N and/or Lime) show higher productivity; combined N+L forms strongest response but may approach a plateau; productivity trends vary by block and moisture/pH interactions.
  - Diversity: Shannon index generally increases in insecticide-treated plots; declines or slower gains in fertilised plots; bryophyte abundance rises across the site, especially in unimproved plots.
  - Community composition: shift toward Festuca rubra under fertilised conditions; reductions in Agrostis spp. under mowing; moss expansion linked to reduced disturbance and mowing regime.
  - Functional groups: shift toward competitive-stress-ruderal types in fertilised plots (N+L) and toward stress-tolerators in unfertilised/unimproved plots; SR-C-S-R groups decline where lime and insecticide are applied.
  - Soil-biotic interactions: soil pH increases with lime; soil moisture negatively correlated with pH; relationships between pH, moisture, and biomass vary by treatment.

## Data Availability, Documentation, and Access
- Primary data sources and documentation are embedded in the report and Appendices; key data files and species lists are described in Appendices 2–8.
- Public access pathways
  - Background details and project data available via the Soil Biodiversity website (URL provided in Introduction).
  - Contact points: CEH at Windermere Road for project details and data requests.
- Metadata and standardization
  - Clear definitions for plot-level treatments, mowing regime, sampling methods, and units (e.g., g dry weight; pH; mm rainfall; dates of mowing and insecticide applications).
  - Appendices provide detailed treatment schedules, survey methodologies, and species lists to support reproducibility.

## Governance, Stewardship, and Recommendations
- Data governance implications
  - Longitudinal, multi-year data with complex design require robust metadata, consistent naming conventions (e.g., Biocide renamed to Insecticide in 2002), and versioned data records.
  - Documentation of site activity, treatment regimes, and data processing steps is essential for reuse by future researchers and for cross-project integration.
- Recommendations for data stewardship
  - Maintain a centralized, versioned data repository with:
    - Datasets by measurement type (biomass, diversity, soil properties, weather).
    - Clear provenance: block, plot, sub-plot, treatment, date, and researcher responsible.
    - Metadata fields for units, sampling methods, and any data adjustments (e.g., normalization against Control 1, log transformations).
  - Preserve appendices as structured data files (e.g., CSV/CSV-like formats) to enable reuse of biomass, PCA loadings, and point-analysis results.
  - Ensure bryophyte and vascular plant taxonomic lists are standardized and kept up to date; document any taxonomic changes and nomenclature used.
  - Implement data quality checks for missing weeks (weather data) and annotate any substitutions or data imputation.
  - Facilitate access controls and licensing that align with project consent and publication plans; provide data dictionaries and methodological notes for end users.
- Conservation of value
  - The dataset supports analyses of how mowing, fertilisation, and insecticide use shape productivity and biodiversity over time, offering valuable horizon for meta-analyses and policy-relevant insights on grassland management and soil-plant interactions.

Key insights for data stewards: this is a richly multi-faceted, long-running data collection effort with careful treatment control and diverse response variables. It benefits from careful standardization, thorough metadata, and accessible documentation to enable reuse across researchers and later phases of the programme.