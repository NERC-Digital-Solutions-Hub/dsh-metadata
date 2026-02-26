# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information: CBED and PCM Modelling for UK Protected Sites 2018-2020

- Purpose
  - Describe the workflow and data structures for mapping deposition and concentration of pollutants to UK protected sites (SAC, SPA, SSSI) using CBED and PCM models for 2018–2020 (3-year rolling means).

- Data sources and initial processing
  - Create a 1x1 km UK grid and clip to boundaries of protected sites.
  - Merge gridded CBED 2018–2020 data (deposition and concentrations) with protected-site boundaries to produce a site-by-grid CBED dataset.
  - Repeat for NOx and SO2 concentration data using PCM model outputs.
  - Source boundary and site lists from national sources; outputs organized as site-by-grid overlaps with grid areas.

- Deposition and concentration calculations (Step 2)
  - Compute minimum, maximum, and grid-average deposition and concentration values for each protected site using SQL queries on the gridded data.
  - Grid-average deposition per grid square is weighted by the proportion of the grid cell within the site: grid square area / total site area, multiplied by the CBED deposition value; summed across the site (Equation 1).
  - CBED: Concentration-Based Estimated Deposition combining air concentrations, precipitation, ion deposition in five land-cover categories (forest, moorland, grassland, arable, urban); wet deposition from precipitation, occult deposition, and land-cover–specific dry deposition velocities.
  - PCM: Pollution Climate Mapping provides background 1x1 km pollutant concentrations with additional road-side values; used for scenario analysis and TEN applications; one model per pollutant; outputs include base-year and projection data.

- Outputs and time framing
  - CBED results are averaged over three years to smooth inter-annual variability; 3-year means are ecosystem-specific (moorland, forest/woodland) plus a grid-average.
  - Data are provided as annual values but aggregated into rolling 3-year means (except non-marine Ca+Mg for some cases).
  - Wet and dry deposition components cover nitrogen and sulfur species, calcium and magnesium ions, and ammonia.

- Data products and structure (files 1–12)
  - File 1–3: Site-by-grid deposition data by ecosystem (forest, moorland) and grid average; 3-year means (2018–2020) at 1x1 km grid; include SITECODE, SITENAME, SITEAREA, CENTROID coordinates, COUNTRY, DESIGNATION, GRIDAREA, YEAR, and deposition components (NH3/NH4, NO2/NO3, SO2/SO4 NM, Ca/Mg NM).
  - File 4–6: Concentrations by site and grid (ammonia, NOx, SO2) with SITECODE, SITEAREA, YEAR, and concentration values (µg m-3).
  - File 7–9: Generated minimum, maximum, and average deposition values by forest/moorland/grid-average for 2018–2020 (three ecosystem-appropriate metrics per pollutant).
  - File 10–12: Concentrations by site for ammonia, nitrogen oxides, and sulfur dioxide (minimum, maximum, average) for 2018–2020.
  - Data fields include SITECODE, SITENAME, SITEAREA, CENTROID_X/Y, COUNTRY, DESIGNATION, YEAR, GRIDAREA, and pollutant-specific deposition or concentration metrics in keq ha-1 year-1 or µg m-3 as appropriate.

- Units and conversions
  - Deposition: keq ha-1 year-1 (convertible to kg S ha-1 year-1 or kg N ha-1 year-1 using factors: S = 16, N = 14 per keq).
  - Concentrations: µg m-3.
  - Total nitrogen deposition is the sum of NO2/NO3 and NH3/NH4 components.

- Quality control and provenance
  - Methods align with government QA practices; results published in peer-reviewed literature.
  - CBED data undergo extensive peer review and inter-comparison (e.g., Carslaw 2011); mass-balance checks and version control are maintained.
  - Central storage of code and documented method developments; responsible-officer governance for method changes.

- Data structure and fields (overview)
  - Common fields: SITECODE, SITENAME, SITEAREA, CENTROID_X, CENTROID_Y, COUNTRY, DESIGNATION, YEAR, GRIDAREA.
  - Deposition fields (File 1–3, 7–9): NH3_NH4, NO2_NO3, SO2_SO4 NM, CA_MG_NM, with MIN/MAX/AVG and grid-average variants.
  - Concentration fields (File 4–6, 10–12): NH3_CONC, NO2_CONC, SO2_CONC (and MAX/MIN/AVG for site-level data).

- Practical implications for data use
  - Enables end-user self-service access to site-specific deposition and concentration metrics across the UK protected sites for 2018–2020.
  - Supports assessment of exceedances and ecosystem-specific exposure by combining site areas with gridded deposition/concentration maps.
  - Provides a structured data package suitable for policy analysis, scenario testing, and dissemination to stakeholders.