# Abstract

- This dataset comes from the NERC project NE/N001672/1, assessing the effects of artificial light at night on a multi-trophic insect-plant community. It includes field and laboratory observations of insects and plants under different spectra of near-monochromatic LEDs (wavelengths: 385, 447, 469, 475, 518, 607, 630 nm) plus a dark control.
- Measurements cover insect numbers, plant biomass, parasitoid attacks, and parasitoid behavior, collected from field mesocosms and controlled-lab experiments conducted mainly in 2017–2018 at the Penryn Campus, University of Exeter, UK.
- Field setup: 47.5 cm cube BugDorm mesocosms containing broad beans and three aphid species, plus a specialist parasitoid and hyperparasitoids; light treatments applied at night with barriers to prevent spillover.
- Lab experiments: mechanistic studies on 24-hour attack rate and parasitoid flight to light under the same spectra, at a constant 20 lux.
- Data are organized into five files tracking insect population dynamics, hyperparasitism rates, plant biomass, parasitoid behavior, and attack rates under different light conditions; with a detailed data structure and variable definitions.

## Dataset contents and scope

- Field data (17 weeks, 2017): insect populations (aphids and parasitoids), hyperparasitoids, and plant biomass within each mesocosm; weekly counts on selected plants; 70–110 lux lighting window, with 7 spectra treatments plus dark control; barriers prevent cross-mesocosm light leakage.
- Lab data (2017–2018): controlled 20 lux experiments examining (i) 24-hour aphid-parasitoid attack rates and (ii) parasitoid flight to light across all light treatments.
- Temporal coverage: field from June 3, 2017 to October 4, 2017; supplementary lab experiments conducted in summers 2017–2018.
- Organisms measured: broad beans (Vicia faba), three aphid species (Aphis fabae, Acyrthosiphon pisum, Megoura viciae), parasitoid Aphidius megourae, hyperparasitoids (various taxa), and related community members.

## Experimental design and treatments

- Spectral treatments: seven monochromatic spectra plus a dark control; wavelengths as listed above; UV treatment kept at low flux to protect against energy hazards.
- Field arrangement: 47.5 cm cube mesocosms (BugDorm-44545F) spaced 1.5 m apart on benches; each mesocosm started with 2 broad-bean pots and incrementally added to 8 pots per mesocosm.
- Lighting regime: artificial lights on only at night (70 lux on, 110 lux off); light barriers to prevent spillover; photon flux around 7.1 μmol m^-2 s^-1 (except UV at 2.4 μmol m^-2 s^-1).
- Replication and selection: initially 7 replicates per treatment; final analyses included 6 replicates for red/green spectra and 5 replicates for UV due to establishment criteria.
- Data capture cadence: weekly population counts across half of plants per cage; full mesocosm checks if a species was not detected initially; selective sampling of aphid mummies at weeks 12 and 14.

## Data collection and variables

- Field measurements: counts of aphids (three species) and parasitoid mummies, hyperparasitoid presence, and dry above/belowground plant biomass.
- Sampling specifics: 10% mummy sampling at specified weeks for laboratory emergence and hyperparasitoid identification; sampling avoided in cages with low mummy counts to protect populations.
- Lab measurements: (i) 24-hour attack rate with a single Aphidius megourae per cage; (ii) parasitoid flight location after exposure to light; both conducted at 20 lux with replicate treatments.
- Light measurement: lux values verified with a lux meter to ensure consistent treatment illumination.

## Data structure and files

- five data files capturing:
  - Insect population dynamics
  - Hyperparasitism rates
  - Plant biomass
  - Parasitoid behavior
  - Parasitoid attack rates under different light conditions
- Key fields (as a data dictionary): Week, Cage (mesocosm identity), Abundance.factor (sampling density factor), Block (randomized block design), Treatment (dark control or spectral treatment), Spectra (wavelength category), species abbreviations (M.v, A.p, A.f for aphids; L.f, A.e, A.m for parasitoids), mummies, hyperparasitoids presence, plant biomass (above/ below ground), and behavioral/attack metrics (Parasitoid.on.plant, Parasitoid.cage, Parasitoid.near.light).

## Quality control and provenance

- Post-entry data checks performed to align datasets with hard-copy records; explanatory and response variables validated.
- Original researchers: Dirk Sanders, Kevin J. Gaston, F. J. Frank van Veen, University of Exeter.
- Contact information provided for the corresponding authors.

## Governance and data stewardship considerations

- Data stewardship implications: multi-taxa, multi-environment dataset requiring clear metadata, a comprehensive data dictionary, and consistent units and nomenclature across files.
- Availability and limitations: documented sharing limitations and update procedures should be in place; note that field replication was reduced for some treatments due to establishment.
- Interoperability: dataset uses a structured, field/lab integration approach but spans both in-situ field data and controlled-lab experiments, necessitating careful harmonization for reuse and discovery.