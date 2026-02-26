# 1x1 km data sets of Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads by acid and nitrogen deposition for 2019-21

- Purpose and scope
  - Provide 1x1 km raster data for AAE of acidity and AAE of nutrient nitrogen, summarising exceedances of habitat-specific critical loads due to acid and nitrogen deposition for 2019–2021.
  - AAE = total accumulated exceedance (AE) across habitats within a 1x1 km grid square, divided by total habitat area in that grid square.
  - Two separate rasters: acidity AAE (acid_aae_2019-2021.tif) and nutrient nitrogen AAE (nutn_aae_2019-2021.tif).

- What AAE represents and how it is calculated
  - AE for each habitat: AE = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - AAE = AE / total habitat area in the 1x1 km grid square (keq ha-1 year-1).
  - Units: AAE expressed as keq ha-1 year-1 (for acidity, a combination of S and N; for nutrient nitrogen, expresses as keq ha-1 year-1 that can be converted to kg N ha-1 year-1).

- Habitats included (by dataset)
  - Acidity (acid_aae_2019-2021.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, and various woodlands (productive and unmanaged).
  - Nutrient nitrogen (nutn_aae_2019-2021.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, productive woodlands, and various unmanaged woodlands and wetlands, plus dune grassland and saltmarsh.

- Key methods and data sources
  - Based on UK Methods Report (Hall et al., 2015) for calculating acidity and nitrogen critical loads and exceedances.
  - Exceedances derived from critical loads (CL) and CBED deposition data, mapped to habitat distributions.
  - Inputs include:
    - Deposition data: CBED (Concentration-Based Estimated Deposition).
    - UK CEH Land Cover Map 2019 (1 km summary rasters).
  - Freshwaters data (1752 locations) are reported separately and not included in the AAE calculations here because they use catchment areas rather than 1 km grid squares.

- Critical loads and exceedances (conceptual overview)
  - Acidity critical loads (two approaches):
    - Empirical approach for non-woodland mineral/organomineral soils.
    - Simple mass balance (SMB) for woodland and peat soils; uses Ca:Al criteria and related parameters.
    - For peat soils, acidity CLs are set using a target effective rain pH of 4.4 to reflect buffering by organic acids.
  - Freshwaters use the catchment-based FAB model (not used in AAE rasters).
  - Nutrient nitrogen critical loads:
    - Based on empirical evidence under the UNECE CLRTAP framework, linked to habitat classes (EUNIS).
    - Critical loads are given as ranges (e.g., 10–20 kg N ha-1 yr-1) to reflect ecosystem variability; latest revised in 2022.
  - How exceedances are computed:
    - Nitrogen exceedance = total N deposition − CL.
    - Acidity exceedance involves a combination of S and N deposition, using a Critical Load Function that partitions deposition into five regions and calculates a shortest-distance exceedance relative to CLmaxS, CLminN, CLmaxN.

- Data structure, format and coverage
  - Two raster files in British National Grid (EPSG:27700), each with a single band.
  - acid_aae_2019-2021.tif: AAE for acidity (keq ha-1 year-1).
  - nutn_aae_2019-2021.tif: AAE for nutrient nitrogen (keq ha-1 year-1); convert to N kg ha-1 yr-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - Coverage differs between the two layers due to habitat distributions for acidification and eutrophication sensitivities.

- Quality control and interpretation guidance
  - Methods conform to international frameworks and UNECE CLRTAP processes; detailed methodology documented in Hall et al. (2015).
  - Interpretation notes:
    - Exceedances indicate potential for harm under long-term steady-state conditions; exceeding a CL does not imply immediate damage.
    - Habitat maps and CL maps include only areas with data used for calculation and may differ from other habitat distributions.
    - Reducing deposition below the CL does not guarantee immediate ecological or chemical recovery; recovery can be slow and time-lagged.

- Practical notes for users
  - All AAE values are in keq ha-1 year-1; acidity AAE cannot be converted to separate S or N kg values.
  - Visualization and reporting may require attention to data gaps and the potential need for metadata verification due to data provenance and transformations.

- Related documentation and references
  - UK Methods Report (Hall et al., 2015) for critical loads and exceedances calculation.
  - Trends/indicator reports and CEH publications for context on UK acidity and nitrogen exceedances.
  - Appendix I provides the terrain-specific simple mass balance equation for woodland acidity critical loads (Ca:Al, ANC, BC, Hle, etc.), illustrating the complexity of the SMB approach.