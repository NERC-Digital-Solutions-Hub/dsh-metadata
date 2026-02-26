European Monitoring and Evaluation Program Model for the UK (EMEP4UK) annual surface resistance based atmospheric deposition for 2018

- Purpose and scope
  - Provides the annual total surface-resistance-based atmospheric deposition for the UK for 2018.
  - Derived from the EMEP4UK rv4.36 atmospheric chemistry transport model, coupled with WRF v4.2.2 meteorology.
  - Focuses on surface deposition of oxidised and reduced nitrogen and sulphur, with area-weighted totals and land-cover specific deposition.

- Experimental design and data sources
  - Model: EMEP4UK rv4.36 (ACTM) based on EMEP MSC-W rv4.36; 3D meteorology from WRF v4.2.2.
  - Domain: EU domain at 27 × 27 km and nested UK domain at 3 × 3 km; only UK domain results shown.
  - Meteorology: NWP reanalysis nudged from NCEP/NCAR GFS at 1° × 1° every 6 hours.
  - Emissions: UK anthropogenic emissions (NOx, NH3, SO2, primary PM2.5, PMcoarse, CO, NMVOC) from 2019 NAEI scaled to 2018; non-UK emissions from CEIP at 0.1° × 0.1°; UK total used for 2018.
  - Data products: Annual total deposition data produced by the model for 2018.

- Model implementation and environment
  - Compiler: FORTRAN Intel compiler 19.1.3.304 (20200925).
  - Computation: Run on the UKCEH POLAR computing cluster (CentOS 7).

- Nature, units, and data structure
  - File format: NetCDF.
  - Grid: Polar stereographic projection (proj4: +proj=stere +ellps=sphere +lat_0=90.0 +lon_0=0.0 ...).
  - Grid area: variable Area_Grid_km2 (km^2).
  - Deposition variables (dry deposition, area-weighted and land-cover specific):
    - Oxidised sulphur: DDEP_SOX_m2Grid (area weighted), DDEP_SOX_m2Conif (conifer), DDEP_SOX_m2Seminat (semi-natural), DDEP_SOX_m2Water_D (water), DDEP_SOX_m2Decid (deciduous), DDEP_SOX_m2Crops (coniferous crops).
    - Oxidised nitrogen: DDEP_OXN_m2Grid (area weighted), DDEP_OXN_m2Conif, DDEP_OXN_m2Seminat, DDEP_OXN_m2Water_D, DDEP_OXN_m2Decid, DDEP_OXN_m2Crops.
    - Reduced nitrogen: DDEP_RDN_m2Grid (area weighted), DDEP_RDN_m2Conif, DDEP_RDN_m2Seminat, DDEP_RDN_m2Water_D, DDEP_RDN_m2Decid, DDEP_RDN_m2Crops.
  - Notes: The document lists additional naming conventions and that the NetCDF files contain the specified deposition metrics; an example snippet is provided but not detailed here.

- Data quality and limitations
  - A QA/QC process was performed for 2018; QA/QC reports are available on request.
  - Content is provided “as is” with no warranty on error-freeness or fitness for purpose.
  - The dataset represents model-simulated annual totals and is subject to uncertainties in emissions, meteorology, chemistry, and deposition processes.
  - Guidance notes indicate limitations related to model scale, domain boundaries, and potential need for local validation.

- Guidance for use
  - Projection and data access: Data are projected on a polar stereographic grid; users should apply the provided proj4 string in their applications.
  - Software requirements: Requires a NetCDF library compatible with R, Python, or FORTRAN to read the data.
  - Documentation and references: Bibliography includes key model descriptions and related atmospheric deposition studies for context and validation.

- Access and provenance
  - The dataset is the 2018 annual surface-resistance-based atmospheric deposition for the UK produced by EMEP4UK rv4.36 with WRF-driven meteorology.
  - QA/QC reports available on request; data usage requires acknowledgment of the cited models and sources.

- Bibliography (selected)
  - Ge et al., 2021; Geosci. Model Dev. on evaluation of EMEP MSCW and WRF against measurements.
  - Gu et al., 2021; Science on ammonia abatement vs NOx for PM2.5 mitigation.
  - Jalkanen et al., 2016; ship traffic emissions inventory.
  - NCEP/NCAR reanalysis contributions from 2000.
  - Simpson et al., 2012; EMEP MSC-W model technical description.
  - Skamarock et al., 2019; ARW Model V4 description.
  - Vieno et al., 2016a,b; UK PM2.5 sensitivities and 2014 dust episode studies.