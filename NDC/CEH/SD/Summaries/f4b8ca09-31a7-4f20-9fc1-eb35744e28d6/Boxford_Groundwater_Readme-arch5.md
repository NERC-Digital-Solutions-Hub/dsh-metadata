# This dataset contains logged and manual observations of groundwater levels for piezometers at the Centre for Ecology & Hydrology (CEH) River Lambourn Observatory wetlands at Boxford, Berkshire, for the period 01/02/2012 to 16/01/2015.

- Overview
  - Groundwater heads recorded at CEH River Lambourn Observatory wetlands, Boxford, Berkshire (UK) from 01 Feb 2012 to 16 Jan 2015.
  - Includes datums and ground levels for each piezometer, with supporting methodological context from related House et al. publications.

- Site and geology context
  - Riverside wetland (~10 ha) within the River Lambourn floodplain; part of SSSI and SAC due to Desmoulin's whorl snail and MG8 vegetation.
  - Subsurface: Chalk bedrock, overlain by weathered putty chalk, gravels, and peat.

- Instrumentation network and data collection
  - Piezometer array 115 initially installed Feb 2012; supplemental piezometers added May 2013 (locations 16–21) for temperature anomaly studies.
  - Piezometer types: peat (P) and gravel (G); some locations include chalk (C) boreholes (sites 3, 22, 23).
  - Gravel piezometers screened 2.5–3.5 m bgl; peat screens across peat thickness; varied installation details (some screens above ground level; bentonite seals on new peat installations).
  - Continuous groundwater head monitoring at selected piezometers every 15 minutes using In-Situ Level Troll 500s or SWS Divers, at 3 m bgl for gravel and base of peat for peat piezometers.
  - Manual water level checks performed to quality-control logged data prone to drift.

- Data management and quality control
  - Data periods summarized per piezometer (start/end dates; some entries NA where data not recorded or instruments absent).
  - Quality control included manual dipping for verification of automated readings.

- Piezometer movement and datum considerations
  - Piezometers not anchored to bedrock; potential for vertical datum shifts due to peat expansion/contraction.
  - Datum surveys conducted Nov 2013 (low water table) and Apr 2014 (high water table) using Trimble 5600 DR total station and Trimble R8 dGPS.
  - Systematic differences between survey setups indicate minor, predictable errors (mean differences 0.019 m, 0.000 m, 0.006 m for setups 1–3); overall absolute differences around 0.02 m, within instrument accuracy.
  - Conclusion: movement of piezometer datum due to peat saturation was discounted.

- Data availability, structure, and documentation
  - Tables detail continuous data periods for each piezometer (e.g., 1G, 1P, 2G, 2P, etc.) with NA entries where data are missing.
  - Piezometer naming conventions (numbers, G/P/C suffixes) and corresponding elevations provided for several instrument setups.
  - References to related studies and methodology (House et al. 2015a, 2015b, 2016; Price & Schlotzhauer 1999; Sorensen & Butcher 2011; Trimble guides).

- Metadata and governance implications for Data Stewards
  - Clear provenance: instrument types, locations, installation dates, and data collection protocols documented.
  - Metadata richness: piezometer type, depth, and screen intervals; datum survey results; QA processes; connection to published analyses.
  - Data curation needs: ongoing quality checks, handling of NA periods, consistent timestamping, and updating with new observations or reprocessing.
  - Sharing considerations: data likely intended for portal/catalog integration; must respect limitations and embargoes noted in accompanying text.
  - Documentation should link to primary references for traceability and to enable reuse in groundwater-surface water interaction studies and climate-change projections.

- Key limitations and considerations for reuse
  - Gaps and NA entries in the time series require careful gap handling.
  - Datum movements were found negligible under peat conditions, but ongoing monitoring could be required where peat dynamics change.
  - Complex multi-technology instrumentation (Level Trolls, SWS Divers) necessitates attention to sensor-specific quirks during integration.

- References and linkage
  - House et al. (2015a, 2015b), House et al. (2016) on groundwater-surface water interactions and modeling in the Boxford wetland.
  - Price & Schlotzhauer (1999) on peat shrinkage/compression effects.
  - Sorensen & Butcher (2011), Trimble guides (2003, 2005) for monitoring standards and equipment.