# Heavy metal, nitrogen, and sulphur atmospheric deposition with the European Monitoring and Evaluation Program Model for the UK (EMEP4UK) for 1750 - 2018

## Overview
- Provides annual total atmospheric deposition (dry and wet) of cadmium, copper, nickel, lead, zinc, sulphur, and nitrogen over the UK for 1750–2018.
- Created with EMEP4UK model rv4.36 and WRF model v4.2.2; UK results are extracted from a domain covering the EU at 27×27 km2 with a nested UK domain at 3×3 km2.
- Meteorology for all runs uses 2018 conditions; 6-hourly assimilated meteorology from NCEP/NCAR GFS.
- Emissions: UK NOx, NH3, SO2, primary PM2.5, primary PMcoarse, CO, and NMVOCs from 2019 NAEI (rescaled to 2018); non-UK emissions from CEIP, UK total used for 2018.
- Historical heavy metal emissions (1750–1960) from literature; 1970–2018 from UK emissions inventory (NAEI 2021); future projections (2040, 2070, 2100) use country-specific SSPs.

## Methods and data production
- ACTM framework: EMEP MSC-W-based model rv4.36 coupled with WRF for 3D meteorology; 1°×1° NCEP/NCAR reanalysis nudging every 6 hours.
- UK-focused outputs derived from a larger EU domain; annual totals produced on a geographic grid with defined projection parameters.
- Unit definitions and target variables are documented in NetCDF files (post-processing limited to variable extraction).
- Model compilation: FORTRAN Intel compiler; run on the UKCEH POLAR computing cluster.

## Data files and structure
- Contains 30 NetCDF files named EMEP4UK_met2018_emisYYYY.nc, where YYYY indicates the year of emissions.
- Temporal coverage: output for one year every decade from 1750 to 1990; every 5 years between 2005 and 2010; and the year 2018.
- Grid: longitude–latitude grid with explicit grid area (km2) variable.
- Key variables (area-weighted deposition):
  - Dry deposition: oxidised sulphur (SOx), oxidised nitrogen (OXN), reduced nitrogen (RDN) per m2, and metals (Cd, Cu, Ni, Pb, Zn) per m2.
  - Wet deposition: oxidised sulphur (SOx), oxidised nitrogen (OXN), reduced nitrogen (RDN) per m2, and metals (Cd, Cu, Ni, Pb, Zn) per m2.
  - Rainfall (WDEP_PREC, mm).
- NetCDF metadata notes: units and variable names are listed in the files; history attribute documents postprocessing steps.

## Quality assurance, limitations, and documentation
- QA/QC: full QA/QC completed for the 2018 dataset; visual checks conducted for other historical and future runs.
- QA/QC reports are available on request; detailed QA/QC documentation is not included in the primary document.
- Usage disclaimer: content is at the user’s own risk; no warranty or guarantee of error-free content or fitness for purpose.

## Provenance and references
- References associated with data production and methodology include:
  - Tomlinson et al. (2023) on heavy metal emissions (UK 1750–2100).
  - Garland et al. (2022) NAEI emissions inventories (2005–2020).
  - Ge et al. (2021), Gu et al. (2021), Jalkanen et al. (2016), NCEP/NCAR/UCAR sources, Simpson et al. (2012), Skamarock et al. (2019), Vieno et al. (2016a, 2016b).
- Bibliography provides methodological and validation context for the EMEP4UK model, WRF, and emissions inventories.

## Relevance for data leadership and governance
- System-level view: covers multiple pollutants (heavy metals, nitrogen, sulphur) across a long historical range, enabling assessment of deposition trends and policy impact over time.
- Data availability and discoverability: structured NetCDF outputs with explicit variable naming and documentation within the history attribute; year-by-year emission-driven files facilitate longitudinal analyses.
- Metadata and provenance: detailed description of model components, emissions sources, and data lineage supports reproducibility and integration with other datasets (emissions inventories, SSP scenarios).
- Data quality and stewardship: robust QA/QC plan exists (2018 verified; other years checked visually); documentation and references provide traceability for methodological choices.
- Collaboration and system integration: dataset is built from international models (EMEP MSC-W, WRF) and inventories (NAEI, CEIP), illustrating cross-network data sharing and the need for coordinated data governance, standards, and metadata harmonization.
- User considerations for policy and research: suitable for evaluating deposition burdens, cross-border transport implications, and scenario analyses; reliance on 2018 meteorology and rescaled UK emissions indicates alignment with contemporary policy baselines while acknowledging uncertainties in historical data and future projections.