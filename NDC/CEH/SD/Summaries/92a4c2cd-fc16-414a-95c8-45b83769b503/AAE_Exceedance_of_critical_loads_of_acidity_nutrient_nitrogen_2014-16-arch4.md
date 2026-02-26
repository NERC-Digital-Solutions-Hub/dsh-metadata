# AAE data for acidity and nutrient nitrogen critical loads 2014-16

- Purpose and scope
  - 1x1 km data sets of Average Accumulated Exceedance (AAE) for acidity and nutrient nitrogen critical loads due to acid and nitrogen deposition for 2014–2016.
  - AAE summarises exceedances across multiple habitats within each grid square, facilitating assessment of potential long-term ecological effects.

- How AAE is calculated
  - For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - AE summed across all habitats within a 1x1 km grid square.
  - AAE (keq ha-1 year-1) = total AE / total habitat area (ha) in the grid square.

- Habitats included
  - Acidity (AAE): acid grassland; calcareous grassland; dwarf shrub heath; bog; montane; managed productive coniferous woodland; managed productive broadleaved woodland; unmanaged coniferous and broadleaved woodland.
  - Nutrient nitrogen (AAE): acid grassland; calcareous grassland; dwarf shrub heath; bog; montane; managed productive coniferous woodland; managed productive broadleaved woodland; unmanaged beech woodland; unmanaged oak woodland; unmanaged Scots pine woodland; other unmanaged woodland; dune grassland; saltmarsh.

- Data files and structure
  - Two CSV files: acidhab_AAE_2014-16.csv (acidity) and nutnhab_AAE_2014-16.csv (nutrient nitrogen).
  - Coverage varies between files due to habitat distributions.
  - Each row includes: East_m and North_m (OSGB grid centre coordinates), Unique1km (grid square identifier), AAE_keq (AAE value), CountryID (1=England, 2=Wales, 3=Scotland, 4=Northern Ireland).
  - A Unique1km link allows combining acidity and nitrogen data where both exist for the same square.

- Units and conversions
  - AAE is expressed in keq ha-1 year-1.
  - If deposition is below the critical load, AAE is set to zero.
  - For nutrient nitrogen, AAE can be converted to kg N ha-1 year by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year).
  - Acidity AAE represents a combination of sulfur and nitrogen compounds and cannot be converted into kg of S or N separately.

- Data quality, methods, and provenance
  - Based on methods agreed at the UNECE CLRTAP; detailed transparency provided in Hall et al. (2015).
  - Critical loads and CBED deposition data available from the EIDC.
  - Summary exceedance statistics and trends published annually (e.g., Hall et al. 2019; Trends Report 2018) and as a UK Biodiversity Indicator (B5a).
  - Not included in the AAE calculation: freshwater data derived from catchment areas (not 1x1 km grids).

- Interpretation and caveats for use
  - National critical load maps are based on empirical or steady-state mass-balance methods; exceedances indicate potential long-term harm rather than immediate damage.
  - Habitat distribution maps used for critical loads/exceedances may differ from other habitat maps, affecting total habitat areas in acidity and nitrogen analyses.
  - Reducing deposition below the critical load does not guarantee immediate ecological or chemical recovery; both chemical and biological recovery can exhibit long time lags.
  - Uncertainties exist in habitat mapping and critical-load derivation; refer to Hall et al. 2015 and associated metadata for the data uncertainties.

- Use considerations for data governance and strategy
  - The data are linked via a unique 1 km square identifier to enable integration with other 1x1 km datasets.
  - Metadata and documentation are maintained (references to the CEH metadata and related reports).
  - Data are suitable for cross-habitat, grid-level analyses of exceedances and for informing policy-relevant assessments of deposition impacts across the UK.

- References and sources
  - Hall, J.; Rowe, E.; Smith, R.; Dore, T.; Banin, L.F.; Levy, P.; Sawicka, K. 2019. Trends Report 2018: Trends in critical load and critical level exceedances in the UK.
  - Hall, J.; Curtis, C.; Dore, T.; Smith, R. 2015. Methods for the calculation of critical loads and their exceedances in the UK.
  - Data provenance: EIDC (deposition data) and CEH metadata.