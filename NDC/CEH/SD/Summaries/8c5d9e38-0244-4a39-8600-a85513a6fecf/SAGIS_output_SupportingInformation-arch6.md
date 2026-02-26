# Source apportionment of nutrient contributions to rivers in England and Wales modelled with SAGIS

## Purpose and scope
- Estimates of loads and in-river concentrations of nitrates and phosphates from multiple sector sources across England and Wales.
- Results are summarized at Water Framework Directive (WFD) waterbody catchment scale.
- Modelling performed with the SAGIS framework to support catchment management decisions.

## SAGIS framework and modelling approach
- SAGIS (Source Apportionment-GIS) was developed to help regulators and stakeholders identify and quantify pollution sources and to predict impacts of mitigation measures.
- Combines input loads from major sector sources (diffuse and point) with a water quality model to predict in-stream nutrient concentrations.
- Uses a Monte Carlo SIMCAT river water quality model to mix loads with flow and predict concentrations along river reaches.
- Outputs are provided at model features and every 1 km of river; flow data derived from low-flow year 2000 and EA WFD river network definitions.

## Data inputs and sources
- Sector sources include: Agriculture (diffuse), Highways (diffuse), Urban runoff (diffuse), Onsite wastewater treatment systems (OsWwTS, diffuse), Atmospheric deposition (diffuse), Wastewater treatment works (WwTW, point), Storm tanks/CSOs (point), Industrial discharge (point).
- Input load estimation methodologies vary by source (see Table 2 in the dataset description), with key datasets such as EA WwTW data (MCERTS), WIMS water quality data, CORINE land use, rainfall data, PSYCHIC model for phosphorus, and MAGPIE framework for nitrate.
- Point-source loads are represented as mean and standard deviation of annual concentrations and flow; diffuse sources as mass per year or per km2.

## Output data structure and format
- For each pollutant, results are delivered as five shapefiles covering England and Wales.
- Shapefile attributes include:
  - Reach identifiers and location (ReachNo, GISCode, ReachName, X/Y coordinates)
  - Spatial context (US_DS_Feat, Description, FeatName)
  - Hydrology and sampling (ObsFlow, ObsQ90Flow, ObsQ95Flow, ObsQ99Flow, ObsConc, NumSamples, ObsConcUCL/LCL)
  - Concentrations and loads (MeanConc_m in mg/L, MeanLdKGd in kg/d; LCLimMnCon/UCLimMnCon and LCLimMnLd/UCLimMnLd)
  - Source-specific concentrations/loads (SWConc/ SWLoad, IMLoad, INLoad, MILoad, LSLoad, ARLoad, HWLoad, URLoad, ATLoad, BGLoad, STLoad, LKLoad, and related concentrations)
  - Distance data (DISHeadKM), sampling details, and geographic coding
- File naming includes pollutant-specific identification; units are specified in the attribute descriptions.

## Uncertainty and applicability
- Uncertainty due to national-scale data; local refinement is limited.
- Confidence in model outputs is considered good for catchments larger than approximately 50 km2.

## Potential data exploration and usage
- Use for visualizing spatial distribution of nutrient loads and concentrations across catchments.
- Facilitates source attribution (diffuse vs. point) and comparison of relative contributions from sectors.
- Supports scenario analysis of mitigation measures and their predicted in-stream nutrient impacts.
- Enables self-serve data exploration via GIS and related data products for policy and management discussions.

## References and provenance
- Environment Agency (2015). WFD Surface Water Management Catchments Cycle 2.
- UKWIR (2012). Chemical Source Apportionment under the WFD.
- PSYCHIC model (Davison et al., 2008) and MAGPIE framework (Lord & Anthony, 2000) used for nutrient modelling components.