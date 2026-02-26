# Supporting documentation for European Monitoring and Evaluation Program Model for the UK (EMEP4UK) daily atmospheric composition and fluxes for UK-SCAPE (1960 - 2020)

- Overview
  - Provides daily averaged atmospheric composition for the UK (1960–2020) focusing on main nitrogen, sulphur, particulate organic matter, and ozone.
  - Produced with EMEP4UK model rv5.0 and WRF model v4.4.2; UK-domain results are included from a EU-wide domain.
  - Data are intended to support UK-SCAPE analyses and atmospheric composition studies.

- Data provenance and modeling context
  - Modelchain: EMEP4UK rv5.0 (ACTM) derived from EMEP MSC-W rv5.0; 3D meteorology from WRF v4.4.2.
  - Domain setup: EU domain at 27 × 27 km2 with nested UK domain at 3 × 3 km2; only the UK domain outputs are stored.
  - Data assimilation: ERA5 reanalysis using Newtonian nudging every 6 hours in WRF.
  - Emissions: UK NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, and non-methane VOC from NAEI (year-specific); CEIP data for non-UK emissions; UK total used for 1960–2020.
  - Computational details: FORTRAN Intel compiler (19.1.3.304); calculations performed on UKCEH POLAR cluster.

- Data products and structure
  - NetCDF files containing daily averaged atmospheric composition and fluxes.
  - Variables include surface concentrations and related metrics such as:
    - PM components: PM2.5, PMcoarse, PM10, and PM25 water (rh50), including various fine/coarse fractions and dust/sea-salt/bio/OC/EC components.
    - Gases and oxidants: ozone (O3), CO, NO, NO2, NOx, HNO3, NH3, HCHO, isoprene, and related species.
    - Meteorological and depositional fields: mixing layer height (HMIX), deposition fluxes (WDEP_OXN, WDEP_RDN, etc.), rainfall/deposition terms.
    - Near-surface and particulate matter concentrations with specified NetCDF names (e.g., SURF_ug_PM25_rh50, SURF_ppb_CO, SURF_MAXO3, SURF_NO2, SURF_DUST, etc.).
  - Units and naming conventions: detailed in the documentation; NetCDF variable names and corresponding physical units are specified within the file descriptions.
  - Projection and geography: data projected on a polar stereographic grid; Proj4 string provided for reproducibility.

- Data formats, access and usage guidance
  - Primary format: NetCDF; requires a NetCDF library compatible with R, Python, or FORTRAN.
  - Spatial reference: polar stereographic projection; exact Proj4 string provided to ensure correct usage in applications.
  - Documentation included: guidance for using the data is provided, along with a bibliography of model evaluations and related studies.
  - Reproducibility notes: model versions (EMEP4UK rv5.0, WRF 4.4.2) and compilation details are documented to support replication.

- Quality assurance, limitations, and governance
  - QA/QC: conducted for 1960–2020; QA/QC reports available on request (not included in the primary document).
  - Limitations and caveats: dataset usage is at the user’s risk; no warranty or guarantee of error-freeness or fitness for a specific purpose.
  - Metadata and traceability: extensive metadata on variable definitions, units, model versions, and data provenance support data stewardship and auditability.
  - Documentation availability: core guidance for data usage and a robust set of bibliographic references are provided to support interpretation and integration into workflows.

- Data stewardship, maintenance, and uptake
  - Stewardship notes: dataset is historical (1960–2020) with explicit model provenance and emission data sources; update mechanisms and future revisions would follow model development cycles.
  - Practical steps for data users: review NetCDF variable mappings (SURF_* names), ensure alignment with the Proj4 projection, verify units via NetCDF metadata, and consult QA reports for documented quality considerations.
  - References for context and evaluation are provided to support benchmarking and interpretation of model outputs.

- Bibliography and references
  - Key methodological and evaluation references related to EMEP4UK, WRF, and UK emissions and PM2.5 mitigation studies are listed to aid understanding and validation of dataset outputs.