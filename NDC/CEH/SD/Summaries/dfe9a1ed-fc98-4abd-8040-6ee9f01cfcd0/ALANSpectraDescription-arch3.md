# Effects of artificial light on multi-trophic population dynamics

- This dataset originates from the NERC project NE/N001672/1 and comprises field and laboratory experiments that test how different spectra of artificial light at night affect an insect-plant- parasitoid-hyperparasitoid food web.
- Field component: 47.5 cm cube Bug Dorm mesocosms established in a field near the University of Exeter (Cornwall, UK), observing multispecies aphid-parasitoid communities over 17 weeks (June–October 2017).
- Laboratory component: Controlled-condition experiments (summer 2017–summer 2018) to mechanistically assess parasitoid attack rate over 24 hours and parasitoid flight-to-light behaviour under the same light treatments.

## Study design and treatments

- Biological system:
  - Plants: broad beans (Vicia faba, Sutton variety) as aphid resources.
  - Aphids: Aphis fabae, Acyrthosiphon pisum, Megoura viciae (dominant species considered for competition and parasitism).
  - Parasitoids: Aphidius megourae, Aphidius ervi, Lysiphlebus fabarum.
  - Hyperparasitoids: diverse endophagous and ectophagous groups (e.g., Alloxystini, others noted as Dendrocerus species, Asaphes suspensus, etc.).
- Field setup:
  - 47.5 cm x 47.5 cm x 47.5 cm Bug Dorm mesocosms arranged 1.5 m apart, with 1 m high benches.
  - Treatments: seven monochromatic spectra plus a dark (natural night) control.
  - Spectra wavelengths: 385, 447, 469, 475, 518, 607, 630 nm; plus a dark control; white light (20 lux) used as a reference in some lab experiments.
  - Light delivery: artificial lights on at night via dusk-dawn sensor (on at 70 lux, off at 110 lux); barrier tenting between cages to prevent spillover.
  - Photon flux: about 7.1 μmol m^-2 s^-1 (≈ 20 lux) for all treatments except UV (2.4 μmol m^-2 s^-1) to avoid dangerous energy levels.
  - Replication: initially 7 replicates per treatment; final analyses included 6 replicates for red/green and 5 replicates for UV due to establishment criteria.
- Sampling and measurements (field):
  - Weekly counts of all aphids and parasitoid mummies (parasitoid abundance) on half of all plants per cage; full verification of presence/absence where any species was not detected.
  - Week 12 and 14 sampling of 10% of mummies per mesocosm for hyperparasitoid identification (lab emergence in gelatine capsules).
  - Plant biomass: at week 10, 2-week-old bean plants introduced to each mesocosm for 3 weeks; dry aboveground and belowground biomass measured after exclusion of aphids by netted cages.
  - Light transmission: plant netting allowed 97% light transmission under 20 lux white light for biomass measurements.
- Laboratory experiments (mechanistic):
  - (i) 24-hour attack rate: 150 third-instar Megoura viciae aphids on a single plant with one A. megourae parasitoid in each cage, 20°C, 16:8 L:D, 24 h exposure; mummies counted after 2 weeks.
  - (ii) Parasitoid flight-to-light: 2-week-old bean plants with 150 aphids placed in darkness; 20 mated female A. megourae released; after 1 hour, parasitoid locations recorded (on plant vs. away from plant); replicated six times.
- Light measurements:
  - Light levels verified with a lux meter to ensure comparability across treatments (field: ~20 lux for most, UV at lower flux; lab: 20 lux baseline with additional white-light control).

## Data collected and structure

- Five main data files capturing:
  - Insect population dynamics across field mesocosms, including aphid and parasitoid abundances.
  - Hyperparasitism rates and presence/absence data.
  - Plant biomass measurements (aboveground and belowground).
  - Parasitoid behaviour metrics, including attack rates and distribution (on plant, cage side, or near light).
  - Treatment, spectra, and experimental design metadata.
- Key variables and coding:
  - Time and sampling: Week (week from start), Cage (mesocosm identity 1–48), Block (randomized block design), Date of sampling.
  - Abundance and sampling details: Abundance factor (full count vs. partial count, 1 or 2), M.v, M.v.w, A.p, A.p.w, A.f, A.f.w, L.f (mummies), A.m (A. megourae), and hyperparasitoid indicators (D.c, D.d, A.s, A.v, etc.).
  - Plant biomass: ab.plant ( aboveground), root (belowground) biomass in grams.
  - Hyperparasitoids: presence/absence (no/yes) and counts when present.
  - Parasitoid distribution: parasitoid.on.plant, parasitoid.cage, parasitoid.near.light (counts in each location).
  - Spectra and treatments: treatment (control, colored spectra), spectra (specific wavelength labeling), w (white reference in some experiments).
- Data quality controls:
  - Post-entry checks against hard copies to ensure consistency between explanatory and response variables.

## Relevance for monitoring frameworks

- What is measured:
  - Multi-trophic population dynamics under controlled nocturnal light spectra, including direct counts of aphids, parasitoids, and hyperparasitoids, plus plant biomass as a productivity metric.
  - Mechanistic insights into parasitoid behavior under different light conditions (attack rate and flight toward light).
- Data characteristics for monitoring design:
  - Longitudinal weekly data over a growing season (17 weeks field data) with consistent sampling across multiple species.
  - Replicated experimental design with explicit treatment, spectrum, and replication structure, enabling comparison across light wavelengths.
  - Clear metadata and data structure documentation (files, variables, units, and coding) to support integration into monitoring dashboards or policy evaluation tools.
- Potential data gaps and governance considerations:
  - Metadata completeness and standardization across datasets are addressed within the data structure; however, public sharing of all underlying data and governance around open data are not detailed and may present barriers similar to those encountered in monitoring programs (as highlighted in the archetype’s challenges).
  - The dataset includes both field and laboratory components, offering complementary perspectives on real-world versus controlled-environment responses to nocturnal lighting, which is valuable for informing monitoring frameworks that need to account for context-dependence.
- Practical implications for policy and future monitoring:
  - Identifies specific spectral bands that influence multi-trophic interactions, informing lighting recommendations and environmental health monitoring criteria.
  - Demonstrates a robust approach to data collection, quality control, and transparent metadata practices essential for trustworthy environmental monitoring data streams.
  - Provides a template for combining ecosystem-level field observations with mechanistic lab experiments to understand the drivers behind observed population trends under anthropogenic light pollution.