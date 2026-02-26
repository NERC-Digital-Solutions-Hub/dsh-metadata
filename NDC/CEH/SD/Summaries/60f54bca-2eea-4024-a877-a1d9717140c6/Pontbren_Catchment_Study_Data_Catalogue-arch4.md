# Equipment & Methods

- Overview
  - This document collects field drilling equipment, borehole logs (NP20–NP23), N-probe (neutron probe) manipulation plots, and streamflow gauging data (Appendix D) from multiple sites around the Pontbren/Llanfair Caereinion area.
  - Key components include borehole descriptions, lithology, sampling depths, completion tubing, and date of logging; plus time-stamped flow measurements at numerous streamflow sites.

- Borehole logs (NP20–NP23)
  - NP20 (Easternmost, Site S3)
    - Location: PEN-TAL-Y-CEIN LLANFAIR CAEREINION; Grid SJ 07360 06833; Site S3 (easternmost)
    - Logging details: Hand auger with AQ drill rod/guide tube; pneumatic hammer/blade; BOREHOLE LOG; completion tubing 16 gauge aluminum; depth/mBGL entries up to ~1.60 m; date 14/05/06
    - Lithology notes: sequence of silty/clay soils with color mottling; multiple layers described (thickness and depth per layer)
    - Samples: depths 0.80–1.60 m noted
  - NP21 (Central, Site S3)
    - Location: PEN-TAL-Y-CEIN LLANFAIR CAEREINION; Grid SJ 07341 06821
    - Logging details: Similar drilling approach; BOREHOLE LOG; depth to ~1.60 m; date 14/05/06
    - Lithology notes: multiple silty/clay layers with mottling; descriptions include soft to stiff clay and sandstone intervals
    - Completion: 16 gauge aluminum tubing; samples 0.80–1.60 m
  - NP22 (Westernmost, Site S3)
    - Location: PEN-TAL-Y-CEIN LLANFAIR CAEREINION; Grid SJ 07323 06807
    - Logging details: Similar equipment; BOREHOLE LOG; depth to ~1.55–1.60 m
    - Lithology notes: greyish-brown silty/clay with mottling; inclusion of stiff gravelly clay and sandstone fragments
    - Completion: 16 gauge aluminum tubing; samples 1.38–1.55 m
  - NP23 (Tyn y Fron Trees edge of wood)
    - Location: COED CWM-Y-LLWYNOG LLANFAIR CAEREINION; Grid SJ 07426 06920
    - Logging details: Hand auger/AQ drill; BOREHOLE LOG; depth entries up to ~1.50 m; date 14/05/06
    - Lithology notes: humic soil with roots/leaf litter transitioning to stiffer clays; includes multiple horizons
    - Completion: 16 gauge aluminum tubing; samples 0.85–1.50 m

  - Equipment and methods across NP logs
    - Recurrent use of: hand auger with AQ drill rod/guide tube; pneumatic hammer; Atlas Copco RAB; Leopard rotary/percussive air flush drills
    - Completion tubing: aluminum (16 gauge, 44.5 mm diameter)
    - Data captured: depth, lithology, thickness, ground level, datum, and sample intervals; dated logs (14/05/06 for NP20–NP23)

- N-probe manipulation plots
  - Sites and plots referenced as N-probe (NP) manipulation plots within the S3 area (Eastern, Central, Western) and Tyn y Fron Trees edge
  - Purpose: monitor soil moisture through neutron probe readings at specified depths (e.g., around 0.25–1.60 m inferred from borehole depths and sampling intervals)

- Streamflow gauging (Appendix D)
  - Contains flow metered spot measurements across multiple sites (Site 3, Site 4, Site 6, Site 7, Site 8, Site 9, Site 10, Site 13, etc.)
  - Data fields include:
    - Start time and Finish time
    - Flow metered estimate (units likely liters per second, ls-1)
    - Multiple records per site/date combination
  - Temporal coverage includes 2005–2009 timeframes with various measurement episodes
  - Purpose: provide calibration/validation data for discharge and hydrological modeling across the network

- Metadata and provenance
  - Borehole data include precise grid references, datum levels, depth-to-date, and lithology descriptions
  - Logs reference the field company (Groundwater Monitoring and Drilling Ltd) and specific borehole IDs (NP20–NP23)
  - Documented equipment types and drilling techniques support lineage and reproducibility of borehole records
  - Streamflow appendix provides time-stamped measurements with site identifiers and measurement methods

- Data governance implications for Data Leaders
  - The dataset offers high-resolution, site-specific borehole lithology and moisture context that can underpin cross-site hydrological analyses when harmonized
  - Key governance needs:
    - Standardized borehole metadata schema (site_id, probe_id, date, grid_ref, datum, depth_m, lithology, thickness, sample_depths, completion, equipment)
    - Consistent units and depth references across all logs (e.g., depth_mBGL, thickness_m)
    - Clear provenance trails linking NP boreholes to N-probe readings and to streamflow measurements
    - Documentation of data quality flags or QA notes for borehole logs and streamflow measurements
  - Opportunities:
    - Integrate borehole lithology with neutron-probe moisture data to produce ground truth soil moisture profiles
    - Create cross-site groundwater/soil-moisture time-series products and compare with streamflow measurements for hydrological modeling
    - Develop a unified data catalog with the NP logs and Appendix D flow measurements for reuse across networks

- Suggested actions for data management
  - Define a BoreholeLog schema capturing site_id, n_probe_id, borehole_id, location (grid_ref), datum_level, depth_mBGL, thickness_m, lithology_description, completion_tubing, sampling_depths, date_logged, logger
  - Create a StreamflowMeasurement schema capturing site_id, start_time, end_time, flow_ls_per_s, measurement_method, notes
  - Link borehole logs to N-probe readings and to streamflow data with provenance metadata
  - Implement standardized geospatial references and a single date format across all records
  - Tag records with data quality indicators and maintain calibration/observer notes to support auditability and reproducibility