# Soil Biodiversity Site, Sourhope

## Overview and context
- Four years into the NERC Soil Biodiversity Thematic Programme at the Sourhope field site (Scottish Borders).
- Focus on linking soil biodiversity studies with above-ground plant productivity, composition, and diversity.
- Experimental design includes five plot-level treatments plus controls: Nitrogen, Lime, Nitrogen + Lime (N&L), Insecticide, and Control.
- Long-running, multi-project data collection across plant communities, soil chemistry, moisture, and micro/climate conditions.

## Data assets and collection methods (Data inventory)
- Site structure and treatments
  - Rigg Foot Experimental Site: 5 replicate blocks on a downslope gradient; 6 main plots per block, subdivided into 10 sub-plots; 0.5 m2 cells used for data collection.
  - Treatments logged for each plot; detailed treatment map provided in Appendices.
- Weather and climate data
  - On-site Automatic Weather Station since 1999; variables include rainfall, solar radiation, and air/soil temperatures.
  - 2002 period experienced data gaps due to a weather-station outage; some data were substituted from nearby Konza station.
- Above-ground productivity
  - Biomass estimates from randomly chosen 0.5 m2 cells within sub-plots S, T, U, V; mowing occurs May–Sept to ~6 cm height; clippings oven-dried at 80°C and weighed.
  - Baseline data collected in 1998; annual biomass totals calculated and log-transformed for analyses.
- Soil chemistry and moisture
  - Soil pH measured at 5 cm depth in plot centers; full re-measurement in 2002 across plots and cell centers used for botanical surveys.
  - Soil moisture measured (theta probe) in July/August 2002 at corners of each cell; not a standard annual task prior to 2002.
- Botanical surveys and species data
  - Baseline vegetation survey in 1998; subsequent annual or periodic point analyses (2000, 2001, 2002) using 0.5 m2 cells with a 100-hole grid and 25-pin hits; bryophytes identified to species in 2002.
  - Appendix 3 provides a full species list; bryophytes (e.g., Rhytidiadelphus squarrosus) show increasing presence over time.
- Data processing and analyses
  - Point analysis data subjected to PCA; biomass data analyzed with split-plot ANOVA; functional group analysis employing CSR classification (Grime) to interpret responses to nutrient status and disturbance.
  - Appendix 6–8 provide detailed biomass, species rank data, and functional-group distributions.
- Data governance and provenance
  - Detailed site activity logs (Appendix 4) and treatment schedules (Appendix 2) accompany datasets.
  - Clear mapping between measurements, mowing events, and applied treatments to support reproducibility.

## Key results and interpretation (From the Results and Discussion)
- Overall productivity trends
  - Biomass productivity increased relative to 1999 across most treatments, but 2002 showed reductions versus 2001, with declines ranging from ~14% to ~31% depending on treatment.
  - The strongest productivity gains occur where both nitrogen and lime are applied; control plots generally lag behind.
- Mowing and disturbance effects
  - Regular mowing (with grazing exclusion) correlates with declines in Agrostis capillaris and Agrostis vinealis across all treatments, suggesting mowing-specific pressures.
  - Festuca rubra expands particularly in more fertile (lime/N) plots; mosses/bryophytes expand across the site, especially in unimproved plots.
  - Moss expansion linked to mowing height (~6 cm) and absence of grazing; possible interaction with nutrient status.
- Fertilisation effects
  - Nitrogen and/or lime improve productivity; lime raises soil pH toward ~7.0 in upper soil horizons; possible link to reduced soil moisture and chlorosis in high-lime plots.
  - Higher pH and nutrients favor competitive, CSR-type species; N&L plots show a stronger shift toward competitive (C-S-R) groups.
  - In unimproved plots, stress-tolerant (S) species dominate as disturbance is reduced and fertility declines due to nutrient loss in clippings.
- Insecticide effects
  - Dursban 4 OPA insecticide may influence plant diversity indirectly via herbivore suppression; evidence suggests higher diversity could accompany reduced herbivory, but causal links remain cautious due to varying responses among functional groups.
- Trampling and experimental pulses
  - 13CO2 pulse experiments in C2 plots likely caused trampling and reduced vegetation growth, contributing to lower productivity relative to C1.
- Community composition and diversity
  - Shannon diversity: 2002 shows declines in N&L plots relative to baseline; insecticide plots often show relatively higher diversity; bryophyte proportion increases in unimproved plots.
  - Point-analysis and PCA reveal clear separation between improved (fertilised) vs unimproved plots, with lime-treated plots clustering distinctly; certain nitrogen-treated plots align with limed plots in species composition.
  - Functional-group analysis (CSR framework) shows: strong rise of C-S-R species in N&L; stress-tolerant (S) species rise in unimproved treatments; SR/CSR groups decline where lime and nitrogen are applied.

## Data quality, standards, and governance considerations
- Metadata completeness and consistency
  - Treatments, mowing schedules, plot and sub-plot layouts, measurement protocols, and units must be well documented to enable cross-year comparisons.
  - Key variables and units include biomass (g m-2, annual totals), soil pH (unitless), soil moisture (theta probe readings; m3 m-3 or %), and climate variables (standard meteorological units).
- Data provenance and lineage
  - Ensure traceability of biomass measurements to specific mowing events and sub-plot cells; link species hits and bryophyte identifications to year and plot data.
  - Maintain taxonomy resolution for bryophytes and vascular plants; capture changes in species identification confidence (e.g., 2002 bryophyte species-level identifications).
- Data interoperability and sharing
  - Multiple data streams (vegetation, soil chemistry/moisture, weather, and disturbance) require harmonised schemas for cross-dataset analyses.
  - Potential data dissemination via Soil Biodiversity website or CEH data repositories; ensure proper licensing, versioning, and data-package documentation.
- Data gaps and outages
  - 2002 weather station outage caused missing data; document gaps and any corrective actions or substitutions (e.g., from Konza station) to support transparent analyses.

## Challenges and implications for Data Stewards
- Aligning user needs with data richness
  - The project generates rich, multi-year datasets; ensure metadata and data dictionaries support reuse by plant ecologists, soil scientists, and biodiversity researchers.
- Interoperability across treatments and datasets
  - Integrating biomass, species composition, soil chemistry, and moisture data across years and plots requires standardized coding for treatments and consistent measurement intervals.
- Updating and maintaining datasets for Phase II
  - As Phase II data accumulate (e.g., more intensive 13CO2 pulses, additional tracers), maintain versioned datasets with clear provenance and change logs.

## Practical next steps for data management
- Develop comprehensive data dictionaries
  - Define variable names, units, measurement methods, and data types for all years and all data streams.
- Standardize data submission templates
  - Create templates for biomass, pH, moisture, species hits, and weather data to facilitate consistent data capture across teams.
- Establish a central, versioned data repository
  - Enable data provenance, traceability, and re-use; provide access controls where necessary (e.g., Phase II-sensitive data).
- Create machine-readable data packages
  - Align Appendices (species lists, treatment mappings, biomass time series) into downloadable datasets with metadata files.
- Document data quality checks
  - Implement routine QC steps (outliers, unit checks, missing data flags) and publish data quality notes alongside datasets.

## Conclusion
- The Sourhope site yields valuable, long-term datasets linking mowing, fertilisation, insecticide application, and trampling to above-ground productivity and plant community dynamics, including functional-group shifts and bryophyte expansion.
- For data stewardship, the datasets offer rich opportunities for cross-disciplinary analyses but require robust metadata, standardized data schemas, and clear data provenance to enable reuse and long-term data integrity across ongoing and future research.