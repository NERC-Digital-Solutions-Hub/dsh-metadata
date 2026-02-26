Introduction These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2018-20.

- What AAE is
  - AAE summarizes exceedances across multiple habitats within a 1x1 km grid square.
  - For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - AAE (keq ha-1 year-1) = total AE across habitats in the grid square ÷ total habitat area in that square.
  - AAE values are provided as two rasters: acidity AAE and nutrient nitrogen AAE.

- Habitats included
  - Acidity (acid_aae_2018-2020.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed coniferous woodland, managed broadleaved woodland, unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen (nutn_aae_2018-2020.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed woodland (coniferous/broadleaved), unmanaged beech/oak/Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

- Methods and sources
  - Based on UK Methods Report (Hall et al, 2015) for calculating critical loads and exceedances; CBED deposition data and UK Land Cover Map 2019 used.
  - Summary exceedance statistics by habitat and country published in the Trends Report (e.g., Rowe et al., 2023) and UK Biodiversity Indicator.
  - Freshwater exceedances are not included in AAE because freshwater data are catchment-based, not grid-based.

- Calculation and interpretation of exceedances
  - Exceedances for acidity: combine sulfur and nitrogen depositions; calculated relative to the acidity critical load function, using CLmaxS, CLminN, CLmaxN values.
  - Shortest-distance exceedance: the exceedance amount is derived from the shortest distance to the relevant critical load function region (Figure 2 in the source).
  - Acidity critical loads: two approaches
    - Empirical approach for non-woodland mineral/organomineral soils.
    - Simple mass-balance (SMB) for woodland habitats and peat soils (Appendix I provides the SMB equation with Ca:Al ratio as criterion for mineral/organomineral soils; peat uses a buffering-based approach).
  - Nutrient nitrogen critical loads: empirical, set under the Convention on Long-Range Transboundary Air Pollution; habitat classes aligned to European Nature Information System (EUNIS); loads are given as ranges (e.g., 10–20 kg N ha^-1 yr^-1) and most recently revised in 2022.
  - Exceedances are computed as: for nitrogen, total N deposition minus the critical load; for acidity, a combination of S and N depositions relative to the critical load function.
  - A grid cell is considered exceeded if its deposition surpasses the applicable critical load range (for nitrogen).

- Inputs and data structure
  - Deposition data: CBED (Concentration-Based Estimated Deposition) methodology.
  - Land cover: UK CEH Land Cover Map 2019 (1 km summary rasters).
  - Data format: two single-band raster files in British National Grid (EPSG: 27700).
  - Units
    - AAE values: keq ha^-1 yr^-1 (acidity or nitrogen as applicable).
    - If deposition is below the critical load, AAE is set to zero.
    - For nitrogen, AAE can be converted to kg N ha^-1 yr^-1 by multiplying by 14 (1 keq ha^-1 yr^-1 = 14 kg N ha^-1 yr^-1).
    - Acidity AAE cannot be expressed as kg of S or N; remains in keq ha^-1 yr^-1.
  - Coverage: differs between acidity and nitrogen datasets due to habitat distributions; both are 1 km grids but may not align perfectly in total habitat areas.

- Quality control and transparency
  - Methods aligned with UNECE CLRTAP processes; detailed validation documented in Hall et al. (2015).
  - Clear notes on limitations: maps reflect data availability and may differ from other national habitat maps; recovery after reducing deposition can be slow; AAE represents potential long-term effects, not immediate damage.

- Use and interpretation for analysts
  - Exceedances indicate potential long-term harm to systems at steady-state; lack of immediate damage does not imply no impact.
  - Habitat distribution maps and habitat areas used in the calculations may differ from other maps; this can affect total habitat area in acidity vs. nitrogen analyses.
  - AAE values are grid-based summaries; interpretation should consider spatial scale, data coverage, and potential lags in chemical and ecological recovery.

- Appendix and equations
  - Appendix I provides the simple mass-balance equation for acidity critical loads in woodland:
    CLA = ANCw - ANCle(crit)
    with definitions for ANCw, ANCle(crit), BC and leaching terms, and other related parameters (Ca:Al ratio, runoff, etc.).

- References and data provenance
  - Hall J et al. 2015; Henriksen & Posch 2001; Sverdrup et al. 1990, 1994; Calver et al. 2003, 2004; Gammack et al. 1995; Skiba & Cresser 1989; Smith et al. 1992; Morton et al. 2022; Rowe et al. 2023.
  - Data sources: CBED deposition data; UK Land Cover Map 2019; related CEH and Defra reports.