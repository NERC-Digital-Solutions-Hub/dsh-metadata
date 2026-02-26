# Spatial and temporal variations in aquatic organic matter composition in UK surface waters.

## Aim
- Characterize spatial and temporal variation in aquatic organic matter composition in UK surface waters using standardized DOM and water-chemistry measurements, enabling monitoring of environmental health over time.

## Study design and sampling
- Fieldwork conducted 2018–2021 at four locations across England and Scotland.
- Sampling sites encompassed water body types associated with peat or organic soils (pools, headwaters, streams, reservoirs, lakes, outlets) with multiple locations per catchment.
- In situ site measurements: pH, conductivity, dissolved oxygen, water temperature; accompanying air temperature, pressure, and humidity.

## Water chemistry and sample handling
- Grab water samples collected at each site; 50 mL filtered in the field through a 0.45 µm syringe filter; samples kept cold (in a cool bag and cool box) and stored at 4 °C until laboratory analysis.
- Analyses on filtered water included dissolved inorganic and organic carbon, absorbance at eight wavelengths, dissolved nutrients, cations, metals, and anions.

## Organic matter processing
- A larger water sample from each site was filtered to remove particulates, then concentrated from ~large volume to ~100 mL for processing.
- Concentrated sample was evaporated to dryness; the residue represented colloidal and dissolved organic matter (DOM).

## DOM analysis and QA
- DOM samples analyzed for elemental composition (C, N, H, O) using an Elementar Vario MICRO cube after acidification to remove inorganic carbonates.
- A subset of samples analyzed by negative-mode electrospray FT-ICR MS for detailed molecular composition.
- QA procedures:
  - 10% of samples analyzed in replicate.
  - Instrument calibration at run start and with checks throughout.
  - Replicate data compared; if within 95% agreement, averaged; if not, re-analysis performed.
  - CHNO-derived metrics subject to restrictions based on physical properties.

## Datasets and data structure
- UK_Sites: metadata per site and visit (ID, Visit, Month, Year, Group) plus contextual site descriptors (PEAT_AREA, ELEVATION, Type_4, LAND_USE, VEG_COVER, POSITION, CATCHMENT_AREA, HOSTPEAT, DISTANCE_SEA). Locations of sites are not included due to access restrictions granted by water companies.
- UK_DOM: composition metrics derived from DOM CHNO content and FT-ICR MS outputs (e.g., DOM_PROP_C, DOM_COX, DOM_OR, DOM_DBEC, C/N, H/C, O/C, Assigned_formula, Mean_mz, Mean_ai, diversity indices, and fractions of lipid, carbohydrate, amino, peptide, and oxy-aromatic compounds; MS_DBEC).
- UK_Water: environmental variables and water chemistry for each sample (ID, Visit) including pH, conductivity, dissolved oxygen, water temperature, air temperature, humidity, air pressure, bank temperature, DOC, major ions (Cl, SO4, Ca, K, Mg, Na, Al, Mn, Fe, Pb, Cd, Co, Cu, Ni, Zn, Li), and related proxies (e.g., SUVA254, E4E6, DON, DIN, DOP, DIP).

## Analytical methods referenced
- DOM extraction and digestion methodology aligned with Moody (2020) for dissolved organic matter extraction and analysis.
- Techniques combined provide both bulk elemental/chemical composition and high-resolution molecular-level insights.

## Relevance to environmental monitoring and data accessibility
- Demonstrates a standardized, repeatable workflow for monitoring aquatic organic matter and associated water chemistry across multiple UK sites and years.
- Data are organized into dedicated datasets to support temporal and spatial analyses and potential integration with other environmental datasets.
- Anonymization of site locations reflects access and confidentiality considerations common in monitoring programs.

## Key considerations for analysts
- Standardized sampling, filtration, cold-chain handling, and QA are essential for comparability over time and across sites.
- Combining bulk chemistry (DOC, DON, DIN, DOP, DIP, major ions) with DOM composition (CHNO, FT-ICR MS-derived metrics) enables assessment of environmental drivers of organic matter in surface waters.
- Datasets provide a framework for linking organic matter composition to catchment characteristics, peatland influence, and spatial-temporal trends in UK freshwater environments.