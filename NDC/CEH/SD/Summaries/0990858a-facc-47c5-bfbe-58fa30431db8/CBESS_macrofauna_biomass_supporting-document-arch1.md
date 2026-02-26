# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) macrofaunal biomass in mudflat and saltmarsh habitats.

## Overview
- A dataset documenting macrofaunal biomass (grams per square meter) in mudflat and saltmarsh habitats.
- Scope: 6 sites across 2 locations (Essex and Morecambe Bay), 2 habitats per site (mudflat and saltmarsh).
- Temporal coverage: winter and summer 2013; no planned repeats beyond the campaign.
- Structure: 3 replicates across 22 quadrats, sampled at four spatial scales.

## Study design and scope
- Variables observed: biomass of individual taxa (and major debris) per quadrat.
- Sampling framework: 3 cylindrical cores per quadrat (10 cm depth, 10 cm diameter) processed to yield biomass per taxon.
- Spatial scales: four scales defined for spatial analysis (1 m; 1–10 m; 10–100 m; 100 m to upper limit).
- Data processing: biomass per taxon multiplied by a constant (127.323955) and rounded to 0.0001 g to produce biomass in g/m^2.

## Location and habitats
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), and an additional Morecambe site (WP listed as West Plain in field descriptions).
- Habitat pairs per site: Mudflat (MF) and Saltmarsh (SM).
- Habitat contrasts:
  - Saltmarsh: two soil types—clay soils (Essex) vs sandy soils (Morecambe Bay); differences in inundation frequency, creek structure, and vegetation.
  - Mudflat: Essex dominated by cohesive clays, mud, and silt; Morecambe mudflats dominated by coarser, mobile sediments.

## Data collected and measurement
- Primary measurement: biomass of each listed taxa (grams per square meter).
- Taxa list includes numerous polychaetes, molluscs, crustaceans, and other invertebrates (e.g., Arenicola marina, Hediste diversicolor, Cerastoderma edule, Macoma balthica, Mytilus edulis juvenile, Crangon crangon, etc.), plus major debris.
- Data structure: wide table listing biomass by taxon per replicate, quadrat, habitat, site, location, season, and scale.

## Sampling and processing methods
- Field collection: three 10 cm diameter cores per quadrat, up to 10 cm depth.
- Preservation: cores fixed in 4% buffered formalin in seawater; residues stored in 70% IMS after processing.
- Taxonomic processing: organisms identified to species level where possible; damaged specimens grouped as major debris.
- Biomass determination: individuals weighed to 0.0001 g after blotting; when too light to register, recorded as 0.0001 g.
- Data quality: biomass per quadrat cross-checked against accompanying abundance data; species names validated against the World Register of Marine Species (WoRMS).

## Data quality and validation
- Data entry completed independently by two people with double-checking.
- Cross-validation between biomass and abundance datasets to ensure consistency.
- Taxonomic validation against WoRMS to ensure accepted nomenclature.

## Data structure and fields
- Primary file: CSV with detailed field descriptions.
- Key fields include: Row Number, Season (Winter W, Summer S), Location (Morecambe M, Essex E), Site (e.g., CS, WS, AH, FW, TM), Habitat (Mudflat MF, Saltmarsh SM), Quadrat Number (1–22), Scale (1 m to 100 m+), Replicate (1–3), Measurement Type (Maf = Macrofauna).
- Taxon-specific biomass fields for numerous species and major debris; separate blocks for annelids, molluscs, crustaceans, copepods, etc., plus debris categories.

## How analysts can use the dataset
- Compare biomass across habitats within sites and across sites with different sediment types and inundation regimes.
- Assess seasonal differences in macrofaunal biomass between winter and summer samples.
- Explore relationships between habitat type (mudflat vs saltmarsh), sediment type (clay vs sand), and biomass distribution across spatial scales.
- Build predictive models of biomass using site characteristics (location, habitat, soil type, inundation patterns) and seasonal factors.
- Validate species- or group-level responses to environmental gradients and compare to abundance data.
- Use the explicit spatial scales to examine how biomass patterns vary from fine (1 m) to broad (100 m+) scales.

## Limitations and caveats
- Temporal scope is limited to winter and summer 2013; no repeated sampling beyond this field campaign.
- Only six sites across two locations; spatial generalizability may be limited to similar UK mudflat and saltmarsh systems.
- Some taxonomic groups may be underrepresented due to preservation, identification limits, or biomass measurement thresholds.
- Data processing involves a conversion factor; ensure interpretation aligns with the conversion methodology when comparing to other datasets.