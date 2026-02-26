# SUMMARY

- Four years into the NERC Soil Biodiversity Thematic Programme at Sourhope (Scottish Borders) the site has been monitored for above-ground productivity, species composition, and relative abundance (diversity) under five main treatments across replicated blocks.
- Treatments include mowing (site-wide), fertilisation (Nitrogen and Lime, individually and combined), and Insecticide, plus Control plots; field activities span 1998–2002 with extensive data collection and multiple sub-analyses.
- Key climatic and soil measurements accompany botanical and biomass data, enabling analysis of interactions among management, soil pH, moisture, and productivity.
- Appendices provide detailed treatment maps, species lists (including bryophytes), weather data, biomass data, and point-analysis results.

## Data and Data Governance Context (for Data Stewards)

- Data sources and provenance
  - Rigg Foot Experimental Site at Sourhope with 5 replicate blocks, 6 main plots per block, and 10 sub-plots per main plot; 0.5 m x 0.5 m cells used for data collection.
  - Phase I (1998–2001) and Phase II (2002) projects feeding data; 16 Phase I projects plus 8 Phase II projects referenced.
  - On-site Automatic Weather Station; additional field data collected by multiple research groups.
- Data types and endpoints
  - Above-ground biomass: annual totals from five summer cuts per year (1999–2002); biomass per plot and relative productivity against controls.
  - Plant community data:: species lists, point-quadrat surveys (2000–2002), bryophyte identifications (2002 enhanced to species level).
  - Soil and site properties: soil pH (0–5 cm profile, 1998–2002), soil moisture (theta probe, 2002), and weather variables (rainfall, radiation, temperature).
  - Site activity metadata: mowing dates, treatment application dates and rates, and labelling/treatment changes (e.g., Biocide to Insecticide).
- Data volume and storage
  - Primary site data totals: 11,621 soil samples collected since start; 2002 point analysis and biomass datasets with multiple plots and blocks; weather data compiled since 1999.
  - Appendices contain extensive datasets: biomass by plot, treatment summaries, species abundance, and PCA loadings.
- Data accessibility and documentation
  - Core data and detailed methodologies are documented in the report and appendices; primary data and project outputs are accessible via the Soil Biodiversity website.
  - Documentation includes explicit treatment maps (Appendix 1), treatment definitions (Appendix 2), and species lists (Appendix 3), enabling reproducibility and cross-year comparability.
- Data quality and limitations
  - Baseline (1998) established; ongoing longitudinal measurements allow trend analyses, with some gaps noted (e.g., 2000–2001 for Control 2 surveys; 2002 weather data missing for certain periods due to station malfunction).
  - Data analyses include ANOVA (with Year x Treatment interactions), biomass normalization, and PCA for species-hits patterns; bryophyte identifications improved in 2002.

## Key Findings ( organized by thematic area )

- Mowing effect
  - Agrostis capillaris and Agrostis vinealis decline by >40% since 2000 across treatments.
  - Festuca rubra expands, particularly in plots with lime and, to a lesser extent, nitrogen.
  - Bryophyte abundance increases across the site, aided by ~6 cm mowing height and reduced disturbance; mosses are more prominent in unimproved plots.
  - Stress-tolerant (S) species expand across treatments; ruderal and competitive-stress-ruderal (SR/CSR) groups decline with reduced disturbance.

- Fertilisation effect
  - Fertilised plots show sustained productivity gains; greatest biomass in plots receiving both nitrogen and lime.
  - Soil pH rises toward ~7.0 in limed plots; high lime rates drive pH changes with potential impacts on moisture and plant stress.
  - Relationship between biomass and pH is positive overall, but varies by treatment; in N+L plots, C-S-R species prosper, while in lime- or N-only plots, dynamics differ.
  - Increased nitrogen can reduce soil moisture, contributing to water stress in dry periods; signs of chlorosis observed in lime-treated areas.

- Insecticide effect
  - Shannon diversity tends to be higher in insecticide-treated plots, though causal attribution is cautious due to complexity of plant–insect interactions.
  - Possible mechanism: reduced herbivory permits more palatable species to persist in infertile or shifting environments.

- Trampling effect
  - In 2002, C2 plots (high activity during labelling pulses) show pronounced productivity reductions, suggesting trampling and intensive sampling activities can suppress growth locally.

- Community structure and functional groups
  - Three dominant functional groupings identified: stress-tolerators (S), CSR, and SR/CSR; collectively account for 69–95% of hits per plot.
  - By 2002, CSR and SR/CSR dynamics shift with N and/or Lime treatments; N+L plots show strong C-S-R expansion, while unimproved plots favor S species.
  - Point analysis indicates a shift in species composition: improved pastures (Festuca rubra, Poa pratensis) dominate in N/L plots; unimproved plots show higher bryophyte and low-nutrient specialists.
  - Diversity (Shannon H') declines in some fertilised plots (notably N+L) relative to baseline, while other treatments show increases; overall, diversity patterns become more treatment-specific over time.

- Interactions with soil properties
  - Positive association between soil pH and above-ground productivity across treatments; soil moisture negatively correlates with pH.
  - The pH–productivity relationship remains positive overall, but becomes more nuanced within certain treatments (e.g., becomes negative under combined N+L in some analyses).

- Bryophytes and non-vascular components
  - Bryophyte hits increase markedly over time, particularly in unimproved plots, contributing substantially to overall counts and biomass in 2000–2002.
  - A broad bryophyte inventory (Appendix 3) expands beyond previous years, underscoring the need to integrate bryophyte data into community analyses.

## Appendices and Datasets (What they contain)

- Appendix 1: Site map and treatment allocations by plot.
- Appendix 2: Detailed site treatments (Control 1, Control 2, Nitrogen, Lime, Nitrogen & Lime, Insecticide) and application schedules.
- Appendix 3: Species lists (vascular plants and bryophytes) with codes and identifications.
- Appendix 4: Summary of site activity and research engagement.
- Appendix 5: Weather station headline measures (1999–2002) with notes on data gaps in 2002.
- Appendix 6: Annual biomass data per plot and block means.
- Appendix 7: Rank analyses of biomass per plot across years.
- Appendix 8: Percentage rank abundance of species by treatment across 2000–2002, including PCA outputs.

## Implications for Data Stewards

- Data governance and interoperability
  - The study spans multi-year, multi-project data with consistent but evolving treatments; ensure robust metadata to support cross-year alignment and cross-study comparability.
  - Maintain consistent plot labeling (e.g., Biocide -> Insecticide) and document any renaming or redefinitions to prevent misinterpretation in secondary analyses.
- Metadata and provenance
  - Capture detailed protocols for mowing, fertiliser application, and insecticide use; record dates, rates, and any deviations (e.g., mower downtime).
  - Preserve baseline data and ensure longitudinal continuity with clear versioning.
- Data completeness and quality
  - Document and fill data gaps (e.g., Control 2 survey gaps in 2000–2001; weather data outages in 2002) and annotate any imputed or substituted values (e.g., Konza weather station data).
  - Integrate diverse data streams (biomass, species hits, pH, moisture, litter, bryophyte identifications) with consistent taxonomic nomenclature and data types.
- Accessibility and reuse
  - Provide stable access points (e.g., Soil Biodiversity website) and extractable datasets with clear variable definitions, units, and transformation rules (e.g., ln-transformed biomass for ANOVA).
  - Ensure appendices are machine-readable where possible (tables, species lists, and PCA loadings) to facilitate reuse in meta-analyses.
- Data strategy and planning
  - Develop a long-term data stewardship plan detailing data retention, updating schedules (e.g., ongoing Phase II data beyond 2002), and archiving of voluminous datasets (e.g., 11,621 soil samples, biomass time series).

## Access and Contact (for further data requests)

- Data and project outputs are hosted via the Soil Biodiversity website (national programme context); contact CEH and project PIs for detailed data requests and data-use permissions.