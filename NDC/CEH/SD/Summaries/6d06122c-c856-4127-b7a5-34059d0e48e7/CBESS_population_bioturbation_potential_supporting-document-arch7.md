# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) population bioturbation potential in mudflat and saltmarsh habitats

## Overview
- Dataset documenting population bioturbation potential (BPp) in mudflat and saltmarsh habitats as part of CBESS.
- Core variable: BPp calculated from field and biomass data across multiple species.

## Data Collection and Scope
- Spatial coverage: 6 sites across 2 locations — Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).
- Habitat types: Mudflats and saltmarshes.
- Temporal coverage: Winter and Summer 2013; no planned repeat sampling.
- Sampling design: 3 replicates per quadrat across 22 quadrats, at 4 spatial scales; data collected from 6 sites over 2 locations, 2 habitats.
- Site characteristics: Saltmarsh sites represent contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differ in inundation frequency, creek structure, and vegetation; mudflats differ in sediment composition between locations.

## Methodology
- Field procedures: Collect 3 cylindrical cores per quadrat (10 cm deep, used for macrofauna extraction).
- Lab processing: Fix in 4% buffered formalin, sieve through 0.5 mm, identify and count organisms to species level, weigh biomass, and record data in 70% IMS.
- BPp calculation: BPp = BPi × Ai, where Ai is species abundance per quadrat, and BPi = (sqrt(Bi)) × Mi × Ri (Bi = biomass per m²; Mi = mobility; Ri = reworking rate).
- Species considered: Includes a wide range of taxa (e.g., Arenicola marina, Caprellids, Crustaceans, Molluscs, Polychaetes, and other invertebrates) with species-specific BPp entries.
- Calibration and data handling: Data entered by two people and cross-checked; biomass validated against abundance; BPp calculations double-checked.

## Data Content and Structure
- File format: CSV.
- Core fields: Row Number (sorting), Season (Winter W, Summer S), Location (Essex E, Morecambe M), Site (e.g., AH, FW, TM, CS, WS), Quadrat Number, Scale (A: 1 m, B: 1–10 m, C: 10–100 m, D: 100+ m), Replicate (1–3), Measurement Type (BPp per sample population).
- Taxa data: For each listed species (e.g., Arenicola marina, Ampharete lindstroemi, Nereididae, Molluscs, Crustaceans, etc.), a BPp value per site/quadrat and related counts/biomass data are provided. Some rows include multiple entries (e.g., BPp for the listed species and counts for individual taxa like Crustaceans, Nematoda, etc.).
- Data notes: “NA” indicates no data in certain cells.

## Data Quality Assurance
- Raw data input by two operators with double-checking.
- Biomass cross-validated against abundance data (CBESS_macrofauna_abundance.csv).
- BPp calculations independently verified.

## Data Formats and Access
- Primary data format: CSV (tabular, suitable for GIS and statistical analysis).
- Dataset includes explicit field descriptions and species-specific BPp values, enabling spatial visualization and multi-scale GIS analyses.

## Dataset Field Descriptions (highlights)
- Row Number: Sorting key.
- Season: Winter (W) or Summer (S).
- Location: Morecambe (M) or Essex (E).
- Site: Specific sampling locations (e.g., AH, FW, TM, CS, WS).
- Quadrat Number: Identifier (text/numeric as provided).
- Scale: A (1 m), B (1–10 m), C (10–100 m), D (100+ m).
- Replicate: 1–3.
- Measurement Type: BPp per sample population.
- Taxa: List of species with corresponding BPp values (e.g., Arenicola marina, Pygospio elegans, Macoma balthica, etc.) and their counts or BPp figures.

## GIS-Relevant Considerations and Uses
- Suitable for map-based visualization of BPp across habitats, sites, seasons, and scales.
- Can support spatial comparisons of bioturbation potential by habitat type (mudflat vs. saltmarsh) and sediment type (clay vs. sand).
- Enables integration with other CBESS datasets for ecosystem service assessments and policy-relevant GIS analyses.
- Useful for identifying data gaps at resolutions or locations with NA entries and planning future sampling if repeats are contemplated.