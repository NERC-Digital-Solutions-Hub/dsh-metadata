# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (1960 - 2020)

- Purpose and scope
  - Provides daily averaged atmospheric composition for the UK for main nitrogen, sulphur, particulate matter, and ozone from 1960 to 2020.
  - Generated with EMEP4UK rv5.0 and WRF model v4.4.2; focuses on UK results within the EU domain (27 × 27 km2) with a nested UK domain (3 × 3 km2).

- Experimental design and data sources
  - Atmospheric Chemistry Transport Model (ACTM) derived from EMEP MSC-W rv5.0; simulates hourly to daily averages of pollutants and depositions.
  - Meteorology from WRF v4.4.2 with ERA5 reanalysis nudging (0.25°) every 6 hours.
  - Emissions: UK NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, NMVOC from NAEI; non-UK emissions from CEIP; UK total used for 1960–2020.
  - Daily averaged model outputs are provided.

- Model implementation
  - Codes compiled with Intel FORTRAN compiler (19.1.3.304, 2020).
  - Calculations run on the UKCEH POLAR computing cluster (CentOS Linux 7).

- Variables and data structure
  - Surface concentrations and related fields for a wide range of species, including PM2.5, PMcoarse, PM10, ozone, various gases (NOx, CO, HNO3, NH3, HCHO, etc.), and dust/organic matter components.
  - PM definitions and relationships provided (e.g., PM2.5, PMcoarse, PM10; PM25 water content).
  - NetCDF files carry variables named with specific SURF_ and related codes; units include µg m-3 for PM and ppbv for gases; mixing layer height HMIX (m); daily max ozone SURF_MAXO3, etc.
  - Data are projected on a polar stereographic grid with a defined Proj4 string for use in geographic applications.

- Quality assurance and caveats
  - QA/QC performed for 1960–2020; detailed QA/QC reports available on request.
  - Use of the data is at the user’s risk; no warranty or guarantee of error-free content.

- Usage guidance
  - Data accessible as NetCDF; compatible with R, Python, and FORTRAN.
  - Projections and grid details (Proj4 string) provided to aid integration into analysis workflows.
  - Example data point shown (e.g., SURF_ug_PM25_rh50) illustrating variable naming and structure.

- Bibliography and context
  - References include evaluation studies of EMEP MSC-W and WRF models, UK PM2.5 mitigation analyses, ship emission inventories, and foundational modeling literature (Ge et al. 2021; Gu et al. 2021; Jalkanen et al. 2016; Simpson et al. 2012; Skamarock et al. 2019; Vieno et al. 2016; etc.).

- Overall relevance for analysts monitoring the environment
  - Provides a long-term, standardized daily data product for UK atmospheric composition and fluxes suitable for trend analysis and policy performance assessment.
  - Emphasizes reproducibility and traceability through explicit modeling framework, emissions sources, and data structure.