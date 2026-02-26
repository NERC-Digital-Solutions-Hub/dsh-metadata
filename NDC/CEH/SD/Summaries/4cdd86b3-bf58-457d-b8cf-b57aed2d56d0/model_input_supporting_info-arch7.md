# Supporting information for NE/W002930/1: Digital elevation models of bed rock and land surface topography, river discharge data, and settings files for the CAESAR-Lisflood model following the Chamoli ice-debris flow, India, February 2021

## What are these data?
- Input files for CAESAR-Lisflood (CL), a numerical hydrodynamic-landscape evolution model.
- Contain 10 m DEMs of bed rock and land surface topography, river discharge time-series, and configuration settings files for CL modelling.

## Why were the data collected?
- To support coupled hydrodynamic-landscape evolution modelling within project NE/W002930/1.
- Used CL outputs to evaluate geomorphological response of river channels affected by the 7 February 2021 Chamoli ice-rock avalanche and debris flow.

## Where were the data collected?
- Area described by a rectangular bounding box in WGS 84 / UTM Zone 44:
  - Top left: 352312 m E, 3385209 m N
  - Lower right: 384787 m E, 3358896 m N

## When were the data collected?
- Generated between 1 June 2021 and 31 May 2022.
- Final, calibrated CL input files intended to reproduce the model results.

## How were the data collected?
- The XML configuration file is produced within the CL executable and exported when the project is saved.
- DEMs (.txt) were created in QGIS 3.18, down-sampled from 2 m to 10 m for computational efficiency.
- River discharge (hydro) files (.txt) derived from GEOGloWS reanalysis data, representing discharge at specific river locations (e.g., Ronti Gad–Rishiganga confluence, Rishiganga–Dhauliganga confluence, Dhauliganga–Alaknanda confluence).
- Time zero for hydro data is 6 February 2021.

## Who was responsible for the collection and interpretation of the data?
- Project Principal Investigator (PI) created the data with support from a Co-Investigator.
- PI and Co-Is interpreted CL outputs; interpretation is not included as part of this data resource.

## Completeness of the dataset
- Includes all input files required to run CL and reproduce results.
- The CL executable is not included; available from SourceForge with a wiki for model operation and parameter guidance.

## Model overview
- CL combines CAESAR landscape evolution with LISFLOOD-FP hydrodynamics.
- Supports simulation of floods, erosion/deposition for multiple grain sizes, sediment transport, and slope failure within the model domain.

## Model setup
- Run in “reach mode” and divided into four coupled domains to manage spatial resolution and computational load.
- Coupling points placed between key geomorphological segments (e.g., near major confluences and post-damage downstream of the Tapovan facility).
- Key inputs/parameters include:
  - DEMs for bedrock (pre-event) and surface (post-event) topography
  - River discharge time-series per domain
  - Grain size distributions and sediment transport parameters
  - Numerical and physical parameters controlling hydrological and sediment processes
- Specific assumptions:
  - February 2021 event filled pre-event valley floors with sediment.
  - A traditional spin-up period was not used; instead, a brief wetting of the valley floor (4 days) was applied to maintain numerical stability.
- Grain sizes: nine fractions (0.0001 to 1 m). Initial distribution uniform across most domain; refined in sub-model 2 during calibration.
- External sediment fluxes were not supplied for the first year post-event due to dominance of post-event deposits; external inputs may be needed for longer-term modelling.

## Model calibration
- Calibrated by matching modelled net volumetric change to DEM differencing for 10 Feb 2021 to 25 Dec 2021.
- Domain-scale match: 86.3% (modelled -6.35 Mm3 vs. observed -7.35 Mm3).
- Independent validation with satellite DoD (10 Feb 2021 – 27 Jan 2022): 91.3% match (-6.38 Mm3 modelled vs. -6.98 Mm3).
- Excluded domains 1 and 2 from comparisons due to substantial post-event mass deposition (avalanches) in Aug–Oct 2021 not captured by the model.

## Output data
- Daily mean discharge (Qw) at submodel outlets.
- Daily bulk- and size-specific sediment yields (Qs).
- DoDs (difference of DoDs) generated every seven model days to show vertical topographic change since model start.
- Data structure and outputs are designed to support analysis described above.

## Collection / generation / transformation methods
- See sections 1.5 (data collection specifics) and 2 (model setup/calibration) for details on data processing and modelling workflow.

## Nature and units of recorded values
- XML: text-based CL configuration files (editable with standard text editors).
- DEMs: ASCII grid rasters; values in metres.
- Hydro files: river discharge in cubic metres per second (m3/s); time zero defined as 6 February 2021.
- DoD rasters: net elevation change; negative values indicate erosion, positive values indicate deposition.

## Quality control
- DoD gaps reflect holes from photogrammetric reconstruction (due to cloud cover, occlusions, etc.).
- Statistical significance thresholds calculated using 16 stable hillside areas via Pléiades imagery; two-sigma uncertainty per period:
  - Sept 2015 – 10 Feb 2021: ±1.11 m
  - 10 Feb 2021 – 06 Jun 2021: ±0.91 m
  - 06 Jun 2021 – 25 Dec 2021: ±0.61 m
  - 10 Feb 2021 – 25 Dec 2021: ±1.14 m
  - 10 Feb 2021 – 27 Jan 2022: ±1.06 m
- DoD values exceeding thresholds are deemed statistically significant.
- Stable area polygons are provided as part of the dataset.

## Dataset structure
- domain_1
  - chamoli_domain1.xml
  - domain1_bedr_DEM.txt
  - domain1_surf_DEM.txt
  - rontigad_hydro_input.txt
  - chamoli_domain2.xml
  - domain2_bedr_DEM.txt
  - domain2_surf_DEM.txt
  - rishiganga_hydro_input.txt
  - domain1_hydro_output.dat
  - chamoli_domain3.xml
  - domain3_bedr_DEM.txt
  - domain3_surf_DEM.txt
  - dhauliganga_hydro_input.txt
  - domain2_hydro_output.dat
- domain_2
  - (contents described similarly per domain)
- domain_3
  - (contents described similarly per domain)
- domain_4
  - chamoli_domain4.xml
  - domain4_bedr_DEM.txt
  - domain4_surf_DEM.txt
  - alaknanda_hydro_input.txt
  - domain3_hydro_output.dat
- Note: XML files are model settings; _DEM files describe bedrock and surface topography; hydro files are flow discharge inputs (input vs output indicating upstream domain data used downstream).

## References
- Key literature and data sources cited (Bates et al., 2010; Beven, 1997; Bhushan & Shean, 2021; Coulthard et al.; Einstein, 1950; Hancock et al.; Shugar et al.; Shugar et al.; Skinner & Coulthard; Wiel et al.; Wilcock & Crowe).