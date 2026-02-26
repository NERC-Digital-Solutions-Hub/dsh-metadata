# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal abundance in mudflat and saltmarsh habitats.

## Overview
- Dataset documenting macrofaunal abundance (individuals per m^2) in mudflat and saltmarsh habitats as part of the CBESS program.
- Study design: 6 sites across 2 locations (Essex and Morecambe Bay), 2 habitat types (mudflat and saltmarsh), sampled in winter and summer 2013.
- Sampling details: 3 cores per quadrat across 22 quadrats, spanning 4 spatial scales.
- staff: Christina Wood and Martin Solan.
- Locations include Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM); Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS). Coordinates provided for each site.
- Habitat context: saltmarshes represent contrasting soil types (clay in Essex; sandy in Morecambe Bay) with differing inundation, creek structure, and vegetation; mudflats differ in sediment type (cohesive clays vs coarse mobile sediments).
- Data quality and interoperability: linked with CBESS_macrofauna_biomass.csv; species names checked against WoRMS; data are stored as CSV files.

## Study design and sampling methods
- Sampling campaign: CBESS field campaign conducted in winter and summer 2013; no planned repeats.
- Field procedure: at each quadrat, 3 cylindrical cores (10 cm depth and diameter) collected, fixed in 4% buffered formalin in seawater, sieved (0.5 mm), preserved in 70% IMS.
- species identification and abundance: organisms identified to species level where possible; counts recorded as abundance per taxa; for damaged specimens, head presence used to determine abundance; non-target debris recorded as YES/NO.
- Data processing: counts converted to per m^2 using a factor of 127.323955 and rounded to the nearest whole individual.
- Data quality checks: observations entered by two people and cross-checked; abundance data validated against biomass data in CBESS_macrofauna_biomass.csv; species names validated against WoRMS.

## Data structure and fields
- File format: CSV.
- Core dataset fields (examples): Season (Winter W, Summer S); Location (Morecambe M, Essex E); Site (CS, WS, WP; AH, FW, TM); Habitat (Mudflat MF, Saltmarsh SM); Quadrat Number (1–22); Scale (A: 1 m, B: 1–10 m, Replicate codes C/D; etc.); Measurement Type (Maf; Taxa abundances).
- Taxa coverage: numerous macrofaunal species listed with abundance counts (e.g., Arenicola marina, Ampharete lindstroemi, Capitella sp., Hediste diversicolor, Molluscs, Crustaceans, Crustacea/debris, Nematoda, Nemertea, etc.).
- Data entries include: both explicit abundances for listed taxa and presence/absence indicators for debris categories (Annelid, Mollusc, Crustacea debris) and other groups.
- Metadata: Row Number for sorting; cell formats and descriptive coding for Season, Location, Site, Habitat, Replicate, and Measurement Type.

## Data quality, provenance, and standards
- Multi-operator data entry with double-checking to minimize errors.
- Cross-validation with an independent biomass dataset to ensure consistency between abundance and biomass records.
- Taxonomic names reconciled with an authoritative source (WoRMS).
- Clear documentation of sampling gear, preservation, and processing steps to support reproducibility.
- Dataset clearly links to a larger CBESS framework for ecosystem service and biodiversity analyses.

## Limitations and considerations for analysis
- Temporal coverage is limited to two seasons within a single year (2013); longitudinal or trend analyses over time are not supported by this dataset alone.
- Spatial scope includes six sites across two regions, which may limit broad generalizations to other geographic contexts.
- Core-based sampling and the conversion to per m^2 rely on a fixed scaling factor; potential propagation of any misestimation in the conversion.
- Identification to species level depends on sample preservation and taxonomic expertise; misidentifications could affect certain taxa counts.
- Data integration challenges may arise when combining across habitats, sites, seasons due to differences in sediment type and inundation regimes.
- Some fields in the dataset are densely coded (e.g., many taxa with numerous columns); careful data handling needed for analyses to ensure correct mapping of taxa to columns.

## Potential uses for analysts
- Examine spatial patterns in macrofaunal abundance across mudflat and saltmarsh habitats and between Essex and Morecambe Bay.
- Explore seasonal differences (winter vs. summer) in community composition and abundance.
- Model relationships between sediment type (clay vs sand) and macrofaunal assemblages.
- Develop predictive models of abundance by habitat type, site, and scale; quantify correlations between taxa and environmental/contextual variables.
- Integrate with biomass data to study biomass-abundance relationships and energy flow within these coastal ecosystems.
- Contribute to broader CBESS analyses on coastal biodiversity and ecosystem service sustainability by providing high-resolution, site-specific abundance data.