# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 1750 - 2018

- Purpose and scope
  - Provides annual total atmospheric deposition (surface deposition and wet deposition) of cadmium (Cd), copper (Cu), nickel (Ni), lead (Pb), zinc (Zn), sulphur (S), and nitrogen (N) over the UK from 1750 to 2018.
  - Generated with EMEP4UK model rv4.36 and WRF model v4.2.2; outputs are on a UK-focused domain nested within a 27×27 km EU grid, with UK results at 3×3 km resolution.
  - Outputs include both heavy metals and nitrogen/sulphur deposition, plus rainfall (WDEP_PREC).

- Experimental design and data lineage
  - Atmospheric chemistry transport modelling (ACTM) using EMEP4UK rv4.36, derived from EMEP MSC-W rv4.36.
  - Meteorology from WRF v4.2.2 with data assimilation of NCEP/NCAR GFS reanalysis (1°×1°, every 6 hours); 2018 meteorology used for all runs.
  - Emissions: UK NOx, NH3, SO2, PM2.5, PMcoarse, CO, non-methane VOC from 2019 NAEI, rescaled to 2018; non-UK emissions from CEIP 0.1°×0.1° data; UK totals used for 2018.
  - Historical UK heavy metal emissions 1750–1960 from literature; contemporary 1970–2018 from UK NAEI (2021); future projections (2040, 2070, 2100) via UK-specific SSPs.
  - Data cover 1750–2018 (output years: 1750–1990 every decade, 2005–2010 every 5 years, and 2018).

- Data files, structure, and variables
  - 30 NetCDF files named EMEP4UK_met2018_emisYYYY.nc; timestamp mid-year for each output (e.g., 2018-07-02 12:00:00).
  - Postprocessing: extraction of target variables; additional processing documented in NetCDF history attribute.
  - Grid and data structure: lon/lat grid 240×240; 21 vertical levels; time dimension unlimited; grid metadata described via a specific proj4 string.
  - Key recorded variables and units (examples):
    - Dry deposition: oxidised sulphur (SOX), oxidised nitrogen (OXN), reduced nitrogen (RDN); area-weighted, with variables like DDEP_SOX_m2Grid, DDEP_OXN_m2Grid, DDEP_RDN_m2Grid.
    - Wet deposition: oxidised sulphur (WDEP_SOX), oxidised nitrogen (WDEP_OXN), reduced nitrogen (WDEP_RDN), cadmium (WDEP_CD), copper (WDEP_CU), nickel (WDEP_NI), lead (WDEP_PB), zinc (WDEP_ZN); units in mgS/m2 or mgN/m2 or mg/m2 as applicable.
    - Rainfall: WDEP_PREC (mm).
    - Grid area: Area_Grid_km2 (km2).
  - Example structure excerpt included in documentation.

- Quality assurance and limitations
  - Full QA/QC performed for 2018; visual QA/QC for other years; QA/QC reports available on request (not embedded in the document).
  - Usage disclaimer: content use at user’s own risk; no warranty or guarantee of error-free content or fitness for purpose.
  - Technical provenance: model compilation with FORTRAN Intel compiler (19.1.3.304); computation on the UKCEH POLAR cluster.

- Governance, metadata, and access considerations for Data Stewards
  - Documentation depth: model versions, meteorology source, emission inventories, spatial resolution, year ranges, and variable definitions are provided; ensure metadata captures software versions, emissions sources, and domain definitions for discoverability and reproducibility.
  - Versioning and updates: dataset includes historical (1750–2018) and projections (2040, 2070, 2100); plan for version control as new inventories or SSP scenarios are released.
  - Data availability and access: QA/QC reports available on request; no explicit public download portal stated—clarify access policy and preserve a clear data access route.
  - Metadata completeness: capture file naming convention, timestamping, variable names, units, grid definition, and postprocessing history to support interoperability and reuse.
  - Limitations and scope: UK-domain outputs; 2018 meteorology is used for all runs; emissions and projections depend on external inventories and SSPs; document these dependencies and any known uncertainties.
  - Governance actions for reuse: establish licensing/usage terms aligned with the provided disclaimer, maintain provenance (model versions, software, data sources), and ensure updates align with new emission inventories and SSP updates.

- References and documentation
  - Key methodological and data references supporting model components, emissions inventories, and evaluation studies (e.g., NAEI, CEIP, and multiple treatment and evaluation papers) to support traceability and validation efforts.

- Implications for data custodians
  - The dataset is a comprehensive, long-term deposition dataset integrating UK-specific emissions, historical trends, and future SSP-based projections, suitable for atmospheric chemistry research, environmental policy evaluation, and exposure assessment, provided governance and metadata requirements are in place to ensure proper discoverability, reuse, and version control.