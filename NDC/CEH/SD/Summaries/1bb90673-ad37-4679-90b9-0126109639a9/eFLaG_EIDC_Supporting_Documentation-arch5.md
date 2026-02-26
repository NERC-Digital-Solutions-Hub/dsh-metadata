# OVERVIEW Enhanced Future Flows and Groundwater (eFLaG)

- eFLaG is a nationally consistent hydrological dataset of projections for the UK, covering river flow, groundwater levels, and groundwater recharge from 1981 to 2080, with an observation-driven dataset for 1962–2018.
- Project funded by the Met Office as part of the Strategic Priorities Fund Climate Resilience Programme (contract P107493); partners are UKCEH, BGS, and HR Wallingford.
- Driven by UKCP18 Regional 12km projections, bias-corrected, and applied to models to produce outputs for 200 catchments, 54 boreholes, and 558 groundwater bodies.
- Workflow and site coverage are illustrated in the project materials (Figure 1 and Figure 2 in the doc).

## Data generation and processing

- UKCP18 regional data provide 12 high-resolution projections (1980/1981–2080) for precipitation and potential evaporation (PE); these are used to drive hydrological and groundwater models.
- Outputs include 1km gridded climate time-series and catchment-averaged time-series, derived with standard NRFA methods.
- Ensemble modeling uses three hydrological models (GR4J, GR6J, PDM), one groundwater level model (AquiMod), and one groundwater recharge model (ZOODRM).
- Model outputs cover river flows (m3/s), groundwater levels (mAOD), and groundwater recharge (mm/day); outputs are produced at site- and catchment-scale.

## Catchment and groundwater body selection

- River flows: metadata compiled from NRFA gauging stations, prioritizing data quality, longer records, representativeness, and stakeholder input; network membership (e.g., UKBN2) informs selection.
- Groundwater levels: 54 boreholes from the BGS National Groundwater Level Archive (NGLA) chosen for high-quality, long-term records, regular monthly monitoring, and minimal abstraction effects.
- Groundwater recharge: spatially aggregated over 588 groundwater bodies across England, Wales, and Scotland to reflect hydrogeological characteristics and support Water Framework Directive implementation.

## Model descriptions and outputs

- G2G (Grid-to-Grid): distributed hydrological model producing flows at gauged/ungauged sites and gridded outputs (m3/s).
- GR4J/GR6J: daily lumped hydrological models; GR6J improves low-flow simulations; outputs in m3/s; parameter sets provided.
- PDM: flexible lumped rainfall–runoff model; parameter sets provided; outputs in m3/s.
- AquiMod: lumped groundwater model producing borehole groundwater levels (mAOD).
- ZOODRM: distributed recharge model (2km × 2km grid) using FAO guidelines; outputs in mm/day.
- All outputs are in standard units (m3/s for flows, mAOD for levels, mm/day for recharge).

## Data structure and access

- Data packaged as eFLaG_Dataset.zip containing 27 directories and 3,304 CSV files.
- Two main data groups:
  - simobs: observation-driven simulations for meteorology, river flow, groundwater levels, and recharge; includes observed data where available.
  - simrcm: RCM-driven simulations for meteorology, river flow, groundwater levels, and recharge.
- File naming conventions indicate model (G2G, PDM, GR4J, GR6J), site type (NRFA station, borehole, groundwater body), and data type (simobs/simrcm); examples include ukcp18_simobs_nrfa-station-number.csv and GR4J_simrcm_nrfa-station-number.csv.
- Years covered:
  - simobs: meteorology (1961–2018), river flows and groundwater levels (1963–2018) and recharge (1962–2018).
  - simrcm: meteorology (Dec 1980–Nov 2080), river flows/groundwater levels/recharge (Dec 1982–Nov 2080; Jan 1981–Nov 2080 for recharge).
- Metadata file eFLaG_Station_Metadata.xlsx provides station borehole mappings and related metadata.

## Quality control and validation

- Quality-controlled data sourced from established repositories:
  - River flows: UK National River Flow Archive (NRFA)
  - Groundwater levels: UK National Groundwater Level Archive (NGLA)
- Model evaluation is two-stage:
  - Step 1 (simobs): assess how well simulations driven by observed climate reproduce observations using a suite of metrics, including Nash-Sutcliffe Efficiency (and variants focusing on high/low flows), Absolute Percent Bias, MAPE, Q95APE, and Low-Flow Volume measures.
  - Step 2 (simobs vs simrcm baseline): compare over a common baseline using flow duration curves and low-flow frequency curves rather than day-to-day timing, acknowledging climate model sequencing differences.
- Comprehensive validation details and supplementary metrics are documented in associated references.

## Data governance, stewardship, and usage considerations

- Data provenance and documentation are embedded in the dataset, with links to supporting methodologies and references.
- The data are intended to support climate change impact assessment and hydrological studies at national to local scales, with explicit consideration of representativeness, key hydrometric quality, and stakeholder relevance.
- For data stewards, important considerations include metadata completeness (station and borehole metadata), reproducibility (model parameter files provided for PDM and GR6J), update workflows, and handling of model ensemble outputs and biases.
- Potential challenges noted include handling large, multi-format datasets and ensuring interoperability across diverse model outputs and site types.

## References and underlying sources

- The eFLaG dataset builds on UKCP18 science and regional projections, NRFA catchment methods, NGLA data, and multiple hydrological modeling studies and manuals, including FFGWL and AquiMod/G2G/PDM/GR4J/GR6J/ZOODRM model documentation and prior drought and climate resilience research.