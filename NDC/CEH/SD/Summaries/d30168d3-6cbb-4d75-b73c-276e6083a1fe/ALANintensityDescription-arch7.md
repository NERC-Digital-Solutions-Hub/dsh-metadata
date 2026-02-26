# Effects of artificial light on multi-trophic population dynamics

## Overview
- A combined field and laboratory study investigating how artificial light at night affects multi-trophic interactions among plants, aphids, and parasitoids.
- Data encompass insect counts, plant biomass, parasitoid attack rates, and parasitoid behavioral responses under varying light intensities.

## Experimental design and data collected
- Field experiment:
  - Randomized block design with 6 blocks; 8 light treatments: control (no light) and white LED at 0.1, 1, 5, 10, 20, 50, 100 lux.
  - 6 replicates per treatment, totaling 48 mesocosms.
  - Mesocosms host two plant species (broad bean Vicia faba and barley Hordeum vulgare) and associated insect communities (three aphid species: Aphis fabae, Acyrthosiphon pisum, Sitobion avenae) and their parasitoids (Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae), with a generalist parasitoid Praon dorsale linking aphids.
  - Weekly counts of all species over 9 weeks; plant biomass measured at the end after processing.
  - An additional experiment assessed plant biomass under light treatments without aphids (30 mesocosms; 0, 0.1, 5, 20, 100 lux).
- Laboratory/controlled experiments:
  - Tests of parasitoid attack rate and behavior under different light intensities.
  - Protocols include varying light during exposure (dark vs specific lux levels), 12 h light/12 h dark cycles, and measurement of parasitoid locations or mummy counts after exposure.
- Quality control:
  - Post-entry data checks against hard copies.

## Data structure and files
- Data are organized into 8 files covering:
  - Insect population dynamics and plant biomass from field communities.
  - Plant biomass from experiments without insects.
  - Parasitoid behavior and attack rates under different light conditions.
- Key variables and codes (examples):
  - ab.factor: counting rate adjustment (1 = 100%, 2 = 50% of insects counted).
  - Block: experimental block (1–6).
  - Treat.lux: light treatment at plant height (including control and specified lux levels).
  - Light.lux: light treatment at plant height (mirrors Treat.lux).
  - M.v, M.v.w: Megoura viciae counts and winged morphs.
  - A.p, A.p.w: Acyrthosiphon pisum counts and winged morphs.
  - A.f, A.f.w: Aphis fabae counts and winged morphs.
  - S.a, S.a.w: Sitobion avenae counts and winged morphs.
  - L.f, A.e, A.m: mummy counts for parasitoids Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae.
  - P.dor.m, P.dor.a, P.dor.s: Praon dorsale attacking various aphids.
  - Plantbiomass.g: dry plant biomass (g).
  - Hostdensity: initial aphid host density for parasitoids.
  - Aphid.mummies: number of mummy aphids (attack success).
  - Light.Dark: sequence of 12 h dark vs 12 h light periods.
  - Parasitoid.on.plant, Parasitoid.on.side.of.cage, Parasitoid.ceiling: locations of parasitoids during experiments.

## Timeline and location
- Field site: Penryn Campus, University of Exeter, UK.
- Field data collection: 29 July 2016 to 9 weeks thereafter.
- Additional experiments conducted from Summer 2016 to Spring 2018.
- Experiments conducted in both field mesocosms and a controlled-temperature room.

## Relevance for GIS and map-based data products
- Spatial structure is defined by mesocosm identifiers and block layout, enabling spatial visualization of species counts and biomass across light treatments.
- Potential GIS products:
  - Map of mesocosm locations and treatment gradients with associated counts and biomass.
  - Spatial choropleth or dot-density maps of aphid abundances, parasitoid mummies, or plant biomass by treatment and block.
  - Layered visualization combining light intensity, plant types, and trophic interactions.

## How to use the data
- The 8 files provide a comprehensive dataset for multi-trophic interactions under varying artificial light levels.
- Attribute tables can be joined via mesocosm identity, block, and treatment to produce GIS-ready datasets for spatial analyses and visualization.
- Suitable for creating interactive map-based dashboards showing how light pollution may restructure food webs at small spatial scales.