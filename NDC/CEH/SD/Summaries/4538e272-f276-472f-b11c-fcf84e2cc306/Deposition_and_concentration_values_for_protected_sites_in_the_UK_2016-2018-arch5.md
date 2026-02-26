UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

## Overview
- Documents the generation and structure of CBED and PCM model outputs used to assess deposition and concentration of atmospheric pollutants over the UK, with a focus on protected sites (SAC, SPA, SSSI).
- Uses 2016–2018 rolling three-year means, with outputs at 5x5 km grid for deposition and 1x1 km grid for concentrations, plus site-averaged and ecosystem-specific variants.

## Methodology

- CBED Modelling
  - Produces 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations from concentration data and precipitation data.
  - Dry deposition uses gas/PM concentrations, deposition velocities, and land-cover categories; wet deposition uses precipitation and occult deposition components.
  - Includes ecosystem-specific deposition (moorland, forest) and grid-average values; accounts for orographic enhancement and sea-salt distinctions.
  - Deposition values are averaged over three years to smooth inter-annual variability.
- PCM Modelling
  - Generates background pollution maps and 1x1 km grids of pollutant concentrations (NOx, NO2, PM10, PM2.5, SO2, etc.) plus road-side values.
  - Supports scenario analysis, population exposure calculations, and regulatory reporting (TEN applications for PM10/NOx).
- Step 1: Spatial Mapping to Protected Sites
  - Create a 5x5 km UK grid; clip to protected site boundaries (SAC/SPA/SSSI); merge with 3-year CBED output to obtain UK protected sites CBED dataset.
  - Repeat for 1x1 km concentration datasets (NOx, SO2) from PCM.
- Step 2: Generating Min/Max/Grid-Average Values
  - Use SQL on the gridded data to derive minimum, maximum, and grid-average deposition/concentration for each site.
  - Grid-average deposition calculated as: CBEDDepositionValue × (GridArea / TotalSiteArea), summed over grid squares within the site.

## Data Outputs and Structure

- Data outputs combine deposition and concentration values across multiple datasets and formats:
  - Datasets 1-3: 5x5 km grid deposition by ecosystem (forest, moorland) and grid-average values.
  - Dataset 4: NH3 concentrations by 5x5 km grid (NH3_NH4_CONC) for 2016–2018.
  - Dataset 5: NOx concentrations by 1x1 km grid (NO2_CONC) for 2016–2018.
  - Dataset 6: SO2 concentrations by 1x1 km grid (SO2_CONC) for 2016–2018.
  - Dataset 7: Forest site 3-year means for min/max/avg NO2/NO3, NH3/NH4, SO2/SO4.
  - Dataset 8: Moorland site 3-year means for min/max/avg NO2/NO3, NH3/NH4, SO2/SO4.
  - Dataset 9: (Not explicitly named in the extract, but implied as additional forest/moorland site data).
  - Dataset 10: Grid-average values by site for min/max/avg NO2/NH3/SO2.
  - Dataset 11: NH3 concentrations by site (max/min/avg) for 2016–2018.
  - Dataset 12: NOx concentrations by site (max/min/avg) for 2016–2018.
- Units and data types
  - Deposition values: kilo-equivalents per hectare per year (keq ha-1 year-1); can be converted to kg S ha-1 year-1 or kg N ha-1 year-1 via fixed factors (S 16, N 14).
  - Concentrations: micrograms per cubic meter (µg m-3).
  - A wide set of site attributes included (SiteCode, SiteName, SITEAREA, CENTROID coordinates, GRIDAREA, YEAR, DESIGNATION, etc.).

- Data structure notes
  - Datasets capture three-year means (2016–2018) across grid and site aggregations, with 5x5 km and 1x1 km resolutions, and ecosystem-specific depositions (moorland/forest) or grid averages.
  - Detailed dataset schemas list field names, units, descriptions (e.g., NH3_NH4_FOREST, NO2_NO3_MOORLAND, etc.).

## Data Quality and Governance

- Quality control
  - Methods align with government QA standards for analytical models; extensive peer review and participation in model inter-comparison exercises (e.g., Carslaw 2011).
  - Documented method developments, version numbering, and centralized storage.
  - Mass-balance checks and comparisons with historical years to ensure numerical consistency.
- Provenance and documentation
  - Clear data lineage from raw PCM/CBED inputs to site-level and grid-averaged outputs.
  - Centralized repository and published documentation referenced in supporting literature.

## Data Access and Stewardship Considerations

- Relevance for data stewards
  - Provides robust, governance-ready deposition and concentration datasets for UK protected sites, suitable for data cataloguing, discovery, and reuse.
  - Clear metadata structure (site codes, designations, grid areas, year, ecosystem type) supports data discovery and user needs.
  - Rolling three-year means offer a stable basis for trend analysis while acknowledging inter-annual variability.
- Publishing and updates
  - Data are prepared as standardized, versioned datasets with explicit 3-year windows; updating would require re-running CBED/PCM processes and re-deriving statistics.
  - Tools and workflows implied (SQL queries, grid clipping, FME merging) should be documented and version-controlled for reproducibility.

## Limitations and Considerations

- Inter-annual variability and weather influence deposition, even within three-year averages.
- Orographic enhancement is applied for precipitation concentration in upland areas; applicability to all sites may vary.
- Data are aggregated by ecosystem type (moorland/forest) and grid-average assumptions; site-specific heterogeneity within grid cells may be underrepresented.
- Some datasets and fields in the source description include formatting quirks; ensure consistent schema during data ingestion.

## References and Resources

- Key methodological and supporting references include peer-reviewed studies and Defra/Defra-equivalent materials (e.g., Carslaw 2011; Beswick et al.; RoTAP reports; UKEAP network documentation).
- Related data portals and PCM/UK-EAP resources are listed for access to model data and supporting information.