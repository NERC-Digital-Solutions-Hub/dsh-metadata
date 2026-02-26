Step 1: Spatial Mapping of Deposition and concentration to UK protected sites (SAC, SPA, SSSI)

- Purpose: create gridded deposition and concentration datasets aligned to UK protected sites for further analysis (e.g., critical load exceedance assessments).
- Process:
  - Build a 5x5 km grid covering the UK and clip to UK protected site boundaries (SAC, SPA, SSSI) to produce site-specific gridded data.
  - Merge the gridded data with the 3-year CBED output data (2015–2017) using the Feature Manipulation Engine (FME) to produce a UK protected sites CBED dataset.
  - Repeat the process for 1x1 km concentration datasets for NOx and SO2 (based on PCM model outputs).
- Data sources: boundary and feature lists for UK protected sites downloaded from respective national websites.
- Output: consolidated gridded datasets linking protected site boundaries with CBED deposition and PCM concentration data (illustrated in Figure 1).

Step 2: Generating minimum, maximum, and grid average deposition/concentration values

- Purpose: derive per-site deposition and concentration metrics (minimum, maximum, and grid-average) from gridded data.
- Method:
  - Use SQL queries on the Step 1 gridded dataset.
  - Calculate grid-average deposition by weighting each grid square’s area within the site: GridArea/TotalSiteArea × CBEDDepositionValue, then sum across all grid squares contributing to the site.
- Notation: CBEDDepositionValue × (Grid Area / Total Site area).
- Output: three sets of site-level values (minimum, maximum, grid-average) for deposition/concentration.

CBED Modelling (Concentration-Based Estimated Deposition)

- Overview: CBED generates 5x5 km resolution maps of wet and dry deposition for sulfur, oxidised and reduced nitrogen, and certain base cations from measured air concentrations and precipitation data.
- Key components:
  - Site measurements from the UK Eutrophying and Acidifying Pollutants (UKEAP) network are interpolated to create concentration maps.
  - Wet deposition: combines precipitation concentrations with an annual precipitation map; includes occult deposition (cloud-water deposition) to vegetation.
  - Dry deposition: uses gas/PM concentrations, with deposition velocities across five land-cover categories (forest, moorland, grassland, arable, urban).
  - Deposition to habitats: moorland values applied to all non-woodland habitats; forest values applied to woodland habitats.
  - Orographic enhancement: wet deposition includes an uplift factor for upland regions, based on observations (Great Dun Fell, Holme Moss) to account for higher precipitation concentrations aloft.
  - Inter-annual variability: natural weather variability causes fluctuations; results are averaged over a 3-year period to smooth fluctuations.
- Temporal scope: data calculated annually but provided as rolling 3-year means; ecosystem-specific outputs for moorland and forest/woody habitats or grid-average across ecosystems.
- Output units: deposition values expressed as keq ha-1 year-1; conversions to kg S ha-1 year-1 or kg N ha-1 year-1 via keq-to-kg conversions (multiply by 16 for S, by 14 for N).

PCM Modelling (Pollution Climate Mapping)

- Purpose: produce background maps and 1x1 km grids of pollutant concentrations for the UK, supporting policy development, exposure assessments, and regulatory reporting.
- Details:
  - PCM is a suite of models run on Defra's behalf; one model per pollutant (e.g., NOx, NO2, SO2, PM10/PM2.5, etc.).
  - Outputs include a national background grid (1x1 km) plus ~9,000 road-side values.
  - Used for scenario analysis, population exposure calculations, and supporting Time Extension Notification (TEN) applications for PM10 and NOx.

Nature and Intervals of Data (3-year means)

- Depositions and concentrations are provided as rolling 3-year means (2015–2017) to damp inter-annual variability.
- Outputs include multiple dataset variants (per site, per grid, and per ecosystem type) to support different analyses:
  - 5x5 km grid deposition data by ecosystem (moorland/forest/grid-average) and 3-year mean.
  - 1x1 km grid concentration data for NOx and SO2 (3-year mean).
  - Site-level deposition/concentration summaries for minimum, maximum, and grid-average values across forest, moorland, or grid-average ecosystems.
  - Separate datasets for each pollutant (NH3/NH4, NO2/NO3, SO2/SO4, etc.) and for each spatial aggregation (site, grid, forest, moorland).

Data Structure and Example Datasets

- Datasets describe 3-year mean values for:
  - Deposition: NH3/NH4, NO2/NO3, SO2/SO4 across 5x5 km grids; and NM (non-marine) components.
  - Concentrations: NH3, NOx, SO2 across 1x1 km grids.
- Examples of dataset types:
  - Dataset 1–3: 5x5 km grid deposition by ecosystem and 3-year mean.
  - Dataset 4–6: Concentrations by grid (NH3, NOx, SO2) at 1x1 km resolution.
  - Dataset 7–9: Site-level minimum/maximum/average deposition by ecosystem (moorland/forest) across 5x5 km grids.
  - Dataset 10: Grid-average deposition and concentration values by site (3-year mean) at 1x1 km grid.
  - Dataset 11–12: Site-level concentrations for NH3 and NOx/SO2 (max/min/avg) respectively.
- Units and conversions:
  - Deposition: keq ha-1 year-1; convert to kg S ha-1 year-1 by multiplying by 16 (for sulfur) or to kg N ha-1 year-1 by multiplying by 14 (for nitrogen).
  - Concentrations: µg m-3 for NH3, NOx, SO2.

Quality Control and Validation

- CBED and PCM methods have undergone extensive peer review and inter-comparison (Defra and external partners).
- Documentation, version control, and central storage of code are standard practices.
- Mass balance checks and comparisons with prior years are routinely performed to ensure numerical consistency.

Practical Implications for Data Support

- Data products enable self-service exploration of deposition and concentration patterns at protected sites, supporting policy analysis and public communication.
- Outputs are designed to be cross-referenced with site boundaries, ecosystem types, and multiple spatial resolutions (5x5 km and 1x1 km).
- The comprehensive dataset structure supports both per-site summaries and grid-level analyses, with clear pathways for data conversion and interpretation.

References and Resources

- UK Acidifying and Eutrophying Atmospheric Pollutants (UKEAP) data pages and PCM data resources (URLs provided in data descriptions) for accessing methodology, datasets, and supporting information.