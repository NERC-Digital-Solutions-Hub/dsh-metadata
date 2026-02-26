# Fire emissions data for Southeast Asian fires for 2004, 2006, 2009, 2012, 2014 and 2015

## Scope and purpose
- Provides Southeast Asian fire emissions data for 2004, 2006, 2009, 2012, 2014, and 2015 for a region from 15°S to 15°N and 95°E to 125°W.
- Based on the Fire Inventory from NCAR (FINNv1.5) with added peat-fire emissions (FINNpeatSM).
- Intended for atmospheric modeling and assessment of fire impacts; results are not real-life fire chronicles.

## Data sources and methodology
- Core basis: FINNv1.5 with MOZART4 speciation; daily emissions at 1 km resolution.
- Peat-fire emissions: computed with E_s = BA × BD × ρ × EF_s, using peat density 0.11 g/cm3 and burn depth tied to soil moisture (ESA CCI SMv04.4), with depth limits 5–37 cm and moisture-dependent scaling.
- Burn area and depth assumptions for peatlands:
  - Burn area per peat hotspot: 40 ha (smaller than vegetation-fire assumption in FINNv1.5).
  - Burn depth scaled with soil moisture using pre-dry-season and dry-season moisture bounds.
- Emission factors (EFs) for species drawn from multiple prior studies; example values: CO2 = 1670 g/kg, PM2.5 = 22.3 g/kg, OC = 11.5 g/kg, BC = 0.07 g/kg.
- Peat-fire emissions do not include Malaysian peat fires in this dataset.
- Emissions are assigned on the day of fire detection; no long-term smoldering effects included.

## After-restoration scenario (FINNpeatSM after restoration)
- Hypothetical scenario in which 2.49 million hectares of Indonesian peatland are restored.
- Emissions recalculated by: reducing burned area to reflect average peatland burn-area reductions and increasing soil moisture to reflect observed park-based increases in Kalimantan.
- Scenario described as a model exercise; does not represent actual fires.

## File structure and content
- File format follows FINNv1.5 with MOZART4 specs.
- Each file contains:
  - Header with variable names; one row per fire event.
  - Spatial (LATI, LONGI) and temporal (DAY, TIME) controls.
  - Emission totals for multiple species (CO2, CO, CH4, PM2.5, OC, BC, PM10, and numerous VOCs and related compounds).
  - Area burned (AREA, in m2) and other descriptive fields (GENVEG, etc.).
- Full references accompany the dataset to support the emission factors and methodology.

## Metadata, provenance, and governance
- Methodology and data are linked to Kiely et al. (2019, 2020) and Kiely et al. (2021) for restoration scenarios; extensive supporting references are provided.
- Clear documentation of data origins (FINNv1.5 base, peat-fire extensions) and species coverage to aid reproducibility.
- Public sharing of underlying data is discussed as a governance consideration; the documentation emphasizes data quality, openness, and standardization.

## Data quality, limitations, and caveats
- Malaysian peat fires are not included in these emissions.
- The restoration scenario is hypothetical and should be used for comparative analysis, not as a predictive forecast.
- Emissions are assigned to the detection day only; does not account for smoldering or delayed emissions beyond that day.
- Requires careful attention to metadata quality and consistency for reuse in monitoring frameworks.

## Relevance for monitoring frameworks
- Demonstrates integrating multiple data sources (satellite fire detections, peatland maps, soil moisture, emission factors) into a coherent emissions dataset.
- Provides a detailed, standardized file structure and species-wide emission inventory suitable for atmosphere-ocean/air-quality modeling workflows.
- Highlights practical challenges for monitoring programs: data gaps (partial regional coverage), data accessibility, metadata completeness, and the need for clear governance around data sharing and versioning.
- Illustrates how hypothetical scenario analyses (restoration) can be used to explore policy or management impacts on emissions and air quality.

## References (key sources)
- Kiely et al. 2019; Kiely et al. 2020; Kiely et al. 2021 (emission methodology and restoration scenario)
- Akagi et al. 2011; Christian et al. 2003; Dorigo et al. 2017; Jayarathne et al. 2018; Smith et al. 2018; Stockwell et al. 2016; Wooster et al. 2018 (emission factors and peat-fire measurements)
- Additional supporting sources on soil moisture, peat properties, and related datasets (ESA CCI SM, Driessen & Rochimah, Neuzil, Shimada, Warren et al.)