# European Monitoring and Evaluation Program Model for the UK (EMEP4UK) monthly atmospheric deposition of oxidised sulphur, oxidised nitrogen, and reduced nitrogen for 2002-2021

- Purpose and scope
  - Provides monthly averaged atmospheric deposition and related surface concentrations for oxidised sulphur, oxidised nitrogen, and reduced nitrogen across the UK, covering 2002–2021.
  - Based on the EMEP4UK rv4.36 atmospheric chemistry transport model (ACTM) coupled with WRF meteorology.

- Experimental design and data sources
  - ACTM: EMEP4UK rv4.36 derived from EMEP MSC-W rv4.36; simulates hourly to annual deposition and surface concentrations of pollutants.
  - Meteorology: Weather Research and Forecasting Model (WRF) v4.2.2 with data assimilation (Newtonian nudging) of NCEP/NCAR GFS reanalysis at 1°x1° every 6 hours.
  - Domain and resolution: EU domain at 27 × 27 km², nested UK domain at 3 × 3 km²; UK results extracted from the nested domain.
  - Emissions inputs: UK NOx, NH3, SO2, primary PM2.5, primary PM coarse, CO, and NMVOC from 2019 National Atmospheric Emission Inventory (NAEI), rescaled to 2002–2019; non-UK emissions from CEIP 0.1° × 0.1° data; 2020–2021 emissions set to 2019 values.

- Data products and contents
  - Variables include:
    - Surface concentrations (as applicable) and deposition components for oxidised sulphur (SOx), oxidised nitrogen (NOx), and reduced nitrogen (RDN).
    - Deposition components: dry deposition (area-weighted) and wet deposition, with units described in NetCDF files.
    - Additional metadata such as rainfall (mm), grid area (km²), and corresponding NetCDF variable names.
  - Grid projection: data projected on a polar stereographic grid; proj4 string provided for use in applications.

- Technical implementation
  - Software and hardware: FORTRAN Intel compiler (19.1.3.304) used; computations run on the UKCEH POLAR cluster (CentOS Linux 7).
  - Data format: monthly averaged outputs stored in NetCDF files; structure illustrated with an example variable DDEP_SOX_m2Grid.

- Data quality and governance
  - QA/QC conducted for 2002–2021; QA/QC reports available on request (not included in the document).
  - Data usage disclaimer: content is at the user’s risk; no warranty of error-free content or fitness for a particular use.
  - Metadata and data management: robust metadata is essential; limitations include potential data gaps or discrepancies in upstream emissions inputs for certain years.

- Guidance for use
  - Projections and compatibility: use the provided polar stereographic projection and the associated proj4 string; ensure NetCDF libraries compatible with R, Python, or FORTRAN are available.
  - Data provenance and reproducibility: trace emissions inputs (NAEI CEIP) and meteorology (WRF with GFS reanalysis nudging) to reproduce or validate outputs.

- Bibliography and references
  - Key technical and supporting references related to the EMEPMSC-W model, WRF, and emissions inventories are provided for methodological context.