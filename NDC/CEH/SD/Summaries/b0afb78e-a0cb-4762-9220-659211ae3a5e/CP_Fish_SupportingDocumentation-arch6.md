# Fish abundance, habitat, water quality, flow and climate in English rivers 1975-2017 dataset

## Overview
- Open data product assembled to investigate whether chemical releases affect wildlife populations in rivers, and to relate fish demographic changes to chemical exposure.
- Covers 1975–2017 for English rivers, using long-term EA/NFPD fish data and multiple environmental covariates.
- Aims to enable exploration and self-service data analysis across a broad range of topics, including ecology, hydrology, and water quality.

## Data Sources and Purpose
- Primary fish data: Environment Agency's National Fish Population Database (NFPD) and University of Hull (UoH) fish population data.
- Habitat and habitat-related covariates: River Habitat Survey (RHS) and HABSCORE (habitat quality score for salmon/trout).
- Water quality and chemistry: Environment Agency Water Quality Archive (41 determinands; 1960–2017) and UK Centre for Ecology and Hydrology (UKCEH) data.
- Hydrology and climate: river flow (NRFA), water temperature modeling, Base Flow Index (BFI), Land Cover Map 2015, CHESS-MET meteorology, Gulf Stream Index (GSI), North Atlantic Oscillation Index (NAOI).
- Effluent dilution: EDF estimates via LF2000-WQX model to approximate wastewater influence across GB.
- Data assembled to link fish site observations to covariates across multiple spatial/temporal scales and to support modelling of chemical exposure effects.

## Data Integration and Site Matching
- Two main fish data sources combined: EA NFPD (adult densities) and UoH data (additional habitat data).
- Spatial-temporal matching approach:
  - Fish sites aligned with covariates by proximity along river networks (nearest RHS/HABSCORE sites, water quality sites, NRFA stations, etc.).
  - Fish sites linked to RHS/HABSCORE within 5 km along the river.
  - Water quality and hydrology covariates matched to nearest suitable site along the river network or nearest grid cell when appropriate.
  - Land cover covariates derived for upstream catchments using Land Cover Map 2015 and IHDTM, aggregated to macro-categories (Woodlands, Arable, Seminatural, Urban).
- Coverage:
  - 1180 fish sites with data for 10+ surveys (1975–2017) across seven regions.
  - Table-level summaries indicate region-specific counts for fish sites, water quality matches, river flow matches, RHS/HABSCORE matches, and EDF matches.
- Data completeness:
  - 100% completeness for some covariates (Altitude, land use, BFI, Gulf Stream index, NAOI) in at least a subset; other covariates have variable coverage due to temporal overlap and near-site availability.

## Data Content and File Structure
- Five main data file types (region-specific or aggregated by region):
  - CP_Fish_SpeciesTable.csv: fish species information (scientific name, common name, EA species codes, etc.).
  - CP_Fish_SiteVariables_region.csv: site-level covariates (location, habitat scores, altitude, land-cover metrics, BFI, EDF metrics, etc.).
  - CP_Fish_DataTable_region.csv: survey-level data for each fish observation (site, survey date, species densities, HABSCORE/HQS, GSI, NAOI, Degree_Days).
  - CP_Fish_HydrologyStats_Region.csv: hydrology-related statistics per site (flow metrics from NRFA, thresholds, exceedance metrics, etc.).
  - Region_FISHWIMSStats_DET.csv: water quality determinand statistics by region (WQ site, WQ determinand metrics for 12/25/75/95th percentile thresholds, LOQ handling, sample counts, etc.).
- Additional data documentation:
  - Region_FISHWIMSStats_DET.csv comprises 329 data tables for chemical determinands; 33 fish sites excluded due to licensing restrictions (no public water quality data).
  - Appendix Table A1 lists 41 water quality determinands (variables such as metals, nutrients, organics, pH, conductivity, etc.).
  - Appendix Table A2 lists fish sites excluded due to licensing restrictions.
- Data fields and codes:
  - Missing data code: -9999 (for numeric fields); -NA in some sections.
  - Data tables include explicit links between site IDs, survey IDs, coordinates, and covariate values to support joinable datasets and self-service analyses.

## Covariates and Modelling Approaches
- Habitat and ecology:
  - RHS: habitat modification scores (HMS) and habitat quality assessment (HQA) with reassignment for comparability across years.
  - HABSCORE: species-specific habitat quality scores (for Atlantic salmon and brown trout) linked to observed vs. expected densities.
- Land cover and catchment context:
  - Land Cover Map 2015 aggregated to four macro-categories: Woodlands, Arable, Seminatural, Urban; upstream catchment areas quantified in both percentage and area (km2).
- Temperature and climate:
  - Water temperature: modeled as cumulative degree days (days ≥ 12°C) for the year prior to each fish survey.
  - Temperature modeling approach:
    - Seven GAMMs (one per 0.1 BF index range from 0.3 to 0.99) using combination of month, time, and air temperature as predictors, with ARMA error structures.
    - Best-performing Model 1 (month, time, and air temperature) selected for each BFI range to generate per-site temperature time series.
  - Climate indices: Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI) included to capture broader climatic influences on river conditions.
- Hydrology and river flow:
  - River flow matched to nearest NRFA station; statistics computed over full period and thresholds over 3-, 6-, and 12-month windows preceding each survey.
  - Flow metrics include mean, median, standard deviation, coefficient of variation, quantiles (Q5, Q95), threshold exceedances, event lengths, and related duration metrics.
- Effluent and wastewater:
  - EDF: derived from LF2000-WQX model to estimate the percentage of wastewater in river flows, focusing on significant wastewater treatment works (top contributors to 95% of DWF).
  - EDF statistics reported as EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95, with site-level EDF site IDs.
- Water quality chemicals:
  - 41 determinands (Appendix Table A1) drawn from WQ Archive (1960–2017) and UKCEH repository (1960–1999).
  - Matching: nearest WQ determinand sites within criteria (>= 12 surveys, time overlap, upstream/downstream relation to WWTPs, similar river order, etc.).
  - Water quality statistics calculated for antecedent periods (12 months) with multiple LOQ handling schemes (LoQ treated as LoQ, 0, or LoQ/2) and several data quality filters (minimum, maximum, median, mean, standard deviation, sample counts, LOQ counts).
- Data quality checks:
  - Distances between fish observation points and nearest EF/Determinant points validated; 1 km tolerance for closeness.
  - Total covariate category completeness checked; aggregation sums approach 100% for land cover categorization.

## Data Quality, Limitations, and Gaps
- Some data are inherently patchy due to different data collection purposes and non-standardised formats across sources.
- Final data product contains gaps (noData) in many variables for some sites or years, reflecting limited temporal overlap or lack of proximate covariate data.
- Water quality data had licensing restrictions for a subset of sites (excluded from public dataset).
- HABSCORE availability is spatially and temporally limited; RHS-derived scores may not be directly comparable across all sites/years without adjustments.
- EDF estimation deliberately excludes smaller WWTWs (those contributing to <95% of DWF in a catchment) to maintain computational tractability; interpretation should consider potential underestimation of smaller sources.

## Data Usage, Access, and Structure
- Data organization supports region-based analyses with clearly defined region files for species, data, site variables, and hydrology.
- Core user benefits for Data Support archetype:
  - Enables creation of self-serve dashboards and pivot-table-like analyses across fish abundance, habitat quality, hydrology, and water quality determinants.
  - Facilitates exploratory analyses to examine potential links between fish populations and chemical/hydrological/climatic drivers.
- Data provenance and acknowledgments emphasize open data origins, licensing considerations, and credit to contributing institutions.

## Data Provenance, Access, and Documentation
- Data sources and access URLs provided for:
  - NFPD (Environment Agency)
  - RHS and HABSCORE (Environment Agency; University of Hull)
  - Water Quality Archive (EA)
  - EDF/LF2000-WQX (UKCEH)
  - CHESS-MET (UKCEH)
  - NRFA/NRFA API (UKCEH)
  - Land Cover Map 2015 (UKCEH)
  - Gulf Stream Index (Plymouth Marine Laboratory)
  - NAOI (NCAR)
- Data paper includes extensive methodological detail, data-coding conventions, and author contributions.
- Acknowledgments note funding by NERC and data licensing constraints.

## Practical Takeaways for Data Support
- The Chempop dataset offers a rich, multi-source basis for exploring fish population responses to environmental and chemical drivers in English rivers, using open-data principles.
- The integration approach provides a replicable workflow for linking species observations to habitat, hydrology, land cover, and water quality covariates across large spatial extents.
- While comprehensive, users should account for data gaps, regional variability in covariate coverage, and licensing-related exclusions when designing analyses or dashboards.
- The dataset supports broad data-product development, from dashboards to reproducible analyses, with explicit structures for species, sites, surveys, hydrology, and determinands.