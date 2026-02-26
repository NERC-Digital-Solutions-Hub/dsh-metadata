# Stalybridge Water Table 2019-2022

## Overview
- Dataset of depth to water table measurements from ten experimental microcatchments on Stalybridge Moor, an upland peatland in the UK.
- Microcatchments are labeled A–J (west to east); two dipwell clusters per catchment (near gully edge and far from gully edge), with five dipwells per cluster.
- Time span: 2019–2022, covering pre- and post-gully-blocking periods to evaluate restoration impacts.
- Experimental design uses a Before-After-Control-Intervention (BACI) framework to assess the effects of gully blocking and dam configurations.

## Experimental design / sampling regime
- Controls: microcatchments A, D, G, and J remained unrestored throughout the study.
- Treatments (dam configurations varies by catchment):
  - B: 22 standard cobblestone dams
  - C: 7 cobblestone dams (lower gully) + 13 peat dams (middle/upper reach)
  - E: 10 piped-peat dams
  - F: 6 standard peat dams
  - H: 6 standard peat dams
  - I: 20 timber dams
- Pre-intervention period: May 2019 to March 2020.
- Gully blocking undertaken: 16–25 March 2020.
- Post-intervention: records from April 2020 onwards; some design changes to dams during the post-restoration period (see below).

## Field interventions and post-restoration changes
- Microcatchment E: piped-peat dams operated with an open pipe (150 mm diameter) during 25/03/2020–22/02/2021; on 22/02/2021, all piped-peat dams capped to a 64 mm open orifice.
- Microcatchment I: timber dam slots started at 150 × 40 mm; lower most dam slot constricted to 50 × 40 mm on 27/01/2021; by 29/03/2021 all remaining timber dam slots reduced to 50 × 40 mm.

## Data collection methods
- Dipwells: 1 m long PVC tubes with 10 mm holes drilled at ~100 mm intervals; base sealed; 100–150 mm of the tube protruding above the peat surface.
- Dipwell clusters: two per catchment (near gully edge: ~2 m from the edge; far edge: >10 m from edge).
- Depth to water table recorded by blowing air into the dipwell and reading the depth to air bubbles; dipwell protrusion height also measured to convert to depth from peat surface.
- Vertical datum: peat anchors (metal rods) installed to monitor protrusion changes.
- Data gaps: occasional dipwells not locatable due to snow/vegetation; 'nd' used when data are missing; some dipwells removed during decommissioning.
- Locations: UK grid references provided for each dipwell cluster (detailed in the dataset).

## Data structure and units
- Data stored in CSV format.
- Rows: individual dipwells; columns: dates of observations.
- Dipwell naming convention: [site]_[microcatchment]_[cluster type]_[dipwell number]
  - cluster type: 'n' near-gully edge; 'f' far from gully edge.
  - Example: ST_C_N_5 (dipwell 5, near-gully, microcatchment C, site ST).
- Recorded values: depth to water table from the peat surface in millimetres (mm); negative values indicate water table above peat surface.
- Data quality notes: 'nd' denotes no data; measurement variations due to field conditions are acknowledged.

## Calibration and quality control
- Depth to water table converted from dipwell readings using measured dipwell protrusion height.
- Quality controls include the peat anchor and vertical datum to detect changes in dipwell height due to interference or movement.

## Data collection timeline and coverage
- Field campaigns aimed for monthly measurements during winter months (October–February) but were affected by Covid-19 lockdowns, sometimes resulting in opportunistic measurements in summer/autumn.
- Site decommissioning: final 2022-02-25 visit completed prior to full removal of all dipwells.

## Data accessibility and references
- Primary reference for the BACI design: Shuttleworth, E.L. et al. (2019) Restoration of blanket peat moorland delays stormflow from hillslopes and reduces peak discharge. Journal of Hydrology X, 2, 100006. Available at the provided DOI.
- Project context: Protect-NFM, NERC grant NE/R004560/1 (Optimising NFM in headwater catchments to protect downstream communities).
- Author: Adam Johnston.