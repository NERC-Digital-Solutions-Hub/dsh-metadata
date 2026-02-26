# Source apportionment of annual nutrients and sediment loads to rivers in England and Wales modelled with SEPARATE

## Overview
- Provides annual loads of nitrogen, phosphorus, and fine-grained sediment to rivers at Water Framework Directive waterbody scale.
- Modelled with SEPARATE version 2 (SECTOR Pollutant AppoRtionment for the AquaTic Environment).
- Includes diffuse sources (agriculture, urban, river channel banks, atmospheric deposition, groundwater) and point sources (sewage treatment works, septic tanks, combined sewer overflows, storm tanks).
- Emissions summarised by non-coastal WFD Cycle 2 waterbodies, for individual and cumulative waterbodies.
- Baseline data cover 2010–2012 for some sectors; outputs include an agricultural baseline with and without mitigation; STW emissions based on monitored discharges.
- Outputs exclude estuarine/coastal environments; limited data for small waterbodies (<25 km2) should be treated with caution.
- Format suitable for GIS mapping by joining CSVs to WFD Cycle 2 shapefiles; includes instructions to map to EA_WB_ID.

## Data content and structure
- Table 1: Modelled pollution sources (diffuse and point) described (e.g., diffuse agricultural, diffuse urban, diffuse river channel banks, diffuse atmospheric deposition, STWs, septic tanks, CSOs, storm tanks, groundwater).
- Table 2: Modelled pollutants (Total nitrogen, Total phosphorus, Dissolved phosphorus, Sediment) by source.
- Table 3: File column names in descriptions, detailing a wide set of fields for each waterbody, including local and cumulative load values, and multiple pollutant components.
- Pollutant units: tonnes per year for loads; additional percentage columns for mitigated versus unmitigated or local vs cumulative areas.
- Column naming patterns (examples): X_au_L_t (agricultural unmitigated, local), X_be_L_t (bank erosion, local), X_to_L_t (waterbody total, local), X_to_C_t (waterbody total, cumulative); similar patterns for dissolved phosphorus (D), nitrogen (N), total phosphorus (P), and sediment (S).
- Data are stored in CSV format and can be linked to WFD waterbody shapefiles via EA_WB_ID.

## SEPARATE framework and inputs
- SEPARATE aggregates emissions from:
  - Diffuse agricultural sources using the ADAS Agricultural Pollutant Transfer (APT) framework, built on PSYCHIC and NIPPER models for phosphorus, sediment, and nitrogen losses.
  - Diffuse urban sources using annual runoff from urban areas combined with representative event mean concentrations.
  - River channel banks using a national-scale bank erosion index based on river regime, shear stress, and channel network characteristics.
  - Direct atmospheric deposition using NEAP-N for nitrogen and ECN rainfall data for phosphorus.
  - Sewage treatment works (STWs) using a national register of consented discharges with measured flows and concentrations.
  - Septic tanks based on Environment Agency studies.
  - Combined sewer overflows (CSOs) and storm tanks using rainfall-driven discharge assumptions.
  - Groundwater contributions for nitrogen and phosphorus, with specific treatment for dissolved phosphorus.
- Supporting documentation and references provided for methodology and data sources.

## Data format, mapping, and usage
- Data are designed to be mapped in GIS by joining CSVs to WFD River Waterbody Cycle 2 shapefiles (EA_WB_ID).
- Key columns include area descriptors (loc_area, cum_area) and per-waterbody pollutant loads for local and cumulative views.
- The dataset provides both unmitigated and mitigated agricultural loads, bank erosion, urban diffuse loads, STW discharges, septic tank contributions, CSOs, storm tanks, direct deposition, groundwater, and the total for each waterbody.
- CSV includes descriptive fields such as region, catchment, waterbody name, and waterbody ID to facilitate data joins and labeling.

## Uncertainty and limitations
- National-scale integration with local decision-making considerations; results for small waterbodies may be less reliable.
- Approximately 43% of waterbodies have areas <25 km2 and should be treated with caution due to data accuracy limitations.
- Agricultural emissions reflect a 2010–2012 baseline with a mitigated scenario; some data (e.g., STWs) reflect tightened permits and planned nutrient removal measures over time.
- STW data limitations: flow and concentration data gaps for smaller plants; outfalls/permits may require resolution with Environment Agency experts.
- STW emissions to estuarine/coastal environments are not included.
- Channel bank contributions do not account for bank protection works.
- Temporal coverage across sectors is not fully uniform (e.g., 2010 vs. 2010–2012).

## Practical implications for data use
- Suitable for policy support and high-level national-to-local assessments, with caution for small waterbodies.
- Enables comparative analyses of source contributions and the potential impact of mitigation measures.
- Can underpin dashboards or reports that show sectoral, regional, and waterbody-level pollutant load distributions and changes over time when combined with other datasets.
- Requires careful data cleaning and documentation alignment when integrating with other data sources or using at a finer local scale.

## References and documentation
- Core dataset and methodology documentation, including SEPARATE framework details and supporting sources.
- Links to supporting documentation and key references for the input datasets and models used (e.g., PSYCHIC, NIPPER, ADAS-APT, WALLINGFORD method, SAGIS framework, ECN monitoring data, and UKWIR UKWIR WW02 reports).