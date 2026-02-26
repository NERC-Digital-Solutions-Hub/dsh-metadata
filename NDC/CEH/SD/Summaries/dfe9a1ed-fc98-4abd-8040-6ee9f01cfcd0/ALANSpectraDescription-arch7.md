# Effects of artificial light on multi-trophic population dynamics

## Overview
- NERC project NE/N001672/1 investigates how different spectra of artificial light at night affect an insect-plant food web.
- Uses direct field and laboratory observations of insects and plants to test monochromatic LED treatments across the visible and near-UV spectrum.
- Light treatments: wavelengths 385, 447, 469, 475, 518, 607, 630 nm plus a dark control; compared to natural night light conditions.
- Photon flux is kept around 7.1 μmol m^-2 s^-1 (≈20 lux) for all treatments except UV (2.4 μmol m^-2 s^-1) due to safety limits.
- Data cover insect numbers, plant biomass, parasitoid attack outcomes, and parasitoid/parasitoid-behavior responses.
- Field site: near University of Exeter, Penryn Campus, Cornwall, UK; lab components at Penryn and Exeter facilities; field experiment ran 3 June 2017 to 4 October 2017; related experiments conducted 2017–2018.

## Field experiment design
- Mesocosms: 47.5 cm (per side) Bug Dorm cages arranged on benches; 1.5 m spacing; barriers prevent light spillover.
- Community assembly: broad beans (Vicia faba, Sutton) as host plants for three aphid species (Aphis fabae, Acyrthosiphon pisum, Megoura viciae); a specialist parasitoid Aphidius megourae; hyperparasitoids present in the system.
- Treatments: seven monochromatic spectra plus a dark control (8 total treatments).
- Replication: initially 7 replicates per treatment; after establishment criteria, analyses used 6 replicates for red/green and 5 replicates for UV.
- Light control: artificial lights on at night via dusk-dawn sensor (72–110 lux range); field cages prevent light spillover; night-time light exposure only.

## Data collection and measures
- Population monitoring: weekly counts of aphids and parasitoid mummies across half of the plants per cage; presence/absence checks across all plants if a species is detected.
- Hyperparasitoid sampling: weeks 12 and 14, 10% of aphid mummies per mesocosm collected, lab-identified; hyperparasitoid dynamics documented.
- Plant biomass: week 10 introduction of a 2-week-old bean plant in each mesocosm, measured after 3 weeks; plants enclosed in netted cages during the biomass assessment (netting transmits ~97% of 20 lux white light).
- Light measurements: lux-based verification with a lux meter to confirm per-treatment light levels.

## Laboratory experiments (mechanistic underpinnings)
- (i) 24-hour attack rate: 150 third-instar M. viciae aphids on single 2-week-old plants; 1 female A. megourae per cage for 24 hours; 20°C, 16:8 L:D; mummy counts after 2 weeks.
- (ii) Parasitoid flight-to-light behavior: 2-week-old bean plants with 150 aphids placed in darkness; 20 mated female A. megourae released; parasitoid locations recorded after 1 hour; conducted across all light treatments; 6 replicates per treatment.
- Light level standardization maintained at 20 lux for comparability with the white light control.

## Quality control and data structure
- Post-entry quality checks: validation against hard copies to identify errors in explanatory and response variables.
- Data files: five files cover insect population dynamics, field with hyperparasitism rates, plant biomass, parasitoid behavior, and attack rates under different light conditions.
- Key variables and structure:
  - Temporal and spatial identifiers: Week, Cage, Block, Treatment, Spectra.
  - Abundance and species: Megoura viciae (M.v, M.v.w), Acyrthosiphon pisum (A.p, A.p.w), Aphis fabae (A.f, A.f.w); parasitoids Lysiphlebus fabarum (L.fab), Aphidius ervi (A.e), Aphidius megourae (A.m); hyperparasitoids (e.g., Dendrocerus spp., Asaphes suspensus, Alloxysta victrix).
  - System metrics: aphid counts, mummies (parasitoid success), hyperparasitoid presence, plant biomass (ab.plant, root), parasitoid locations (on plant, cage side, near light).
  - Experimental design terms: Abundance.factor, Spectra, and treatment group labels (including dark control and colored spectra).
- Documentation and provenance: field data collected 2017–2018; principal investigators listed as Dirk Sanders, Kevin J. Gaston, and F.J. Frank van Veen (University of Exeter).

## Relevance to GIS Specialists
- Spatially explicit design: fixed mesocosm layout with precise positions, distances, and containment, enabling georeferenced mapping of treatment effects.
- Temporal dimension: 17-week field period with weekly sampling supports time-series mapping of multi-trophic responses.
- Multivariate, multi-layer data: link between light spectra, species abundances, and plant biomass suitable for layered GIS analyses (e.g., choropleth maps of abundance, time-enabled visitor/behavior layers).
- Potential for data products: creation of interactive map-based dashboards to explore how spectral lighting affects aphid–parasitoid–hyperparasitoid dynamics and plant biomass across space and time.
- Data standards and quality: explicit QA steps and detailed data structure facilitate integration with other spatial datasets and reproducibility of GIS analyses.