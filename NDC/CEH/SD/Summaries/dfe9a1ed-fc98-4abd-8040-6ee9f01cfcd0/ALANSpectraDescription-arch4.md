# Effects of artificial light on multi-trophic population dynamics (NERC project NE/N001672/1)

## Overview
- Field and laboratory study to test how different spectra of artificial light at night affect an insect-plant-parasitoid-hyperparasitoid food web.
- System includes broad beans (Vicia faba) and three aphid species (Aphis fabae, Acyrthosiphon pisum, Megoura viciae) with parasitoids (Aphidius megourae, Aphidius ervi, Lysiphlebus fabarum) and hyperparasitoids.
- Monochromatic near-UV to visible LEDs at specific peak wavelengths (385, 447, 469, 475, 518, 607, 630 nm) plus a dark control, plus a white-light reference in certain lab tests.
- Photon flux ~7.1 μmol m-2 s-1 (20 lux) for all light treatments except UV; UV at 2.4 μmol m-2 s-1 for safety. Field lights on at night via dusk-dawn sensor.

## Experimental design and data sources
- Field component: 47.5 cm cube Bug Dorm mesocosms arranged 1.5 m apart in a field near University of Exeter, Cornwall, UK. Displayed 7 spectra treatments plus a dark control; 2 pots/beginning, increasing to 8 total pots per mesocosm. Replication: initially 7 per treatment; analyses used 6 replicates for red/green and 5 for UV due to establishment.
- Plant and insect setup: 2 broad-bean pots per mesocosm initially; 8 pots per mesocosm by setup end. Aphids (A. fabae, A. pisum, M. viciae) supplied biomass for parasitoids; exclusion of spillover via physical barriers.
- Field monitoring: weekly counts of aphids and parasitoid mummies on half the plants per cage; checks to confirm presence/absence when counts were zero; sampling weeks 12 and 14 involved 10% of mummies for hyperparasitoid identification.
- Plant biomass: dry aboveground and belowground biomass measured at week 10 after introducing a 2-week-old bean plant for 3 weeks.
- Lab components: controlled-condition experiments to examine (i) 24-hour attack rate and (ii) parasitoid flight-to-light behavior under the same spectral treatments, conducted at 20 lux with a white-light reference.

## Data content and structure
- Data organized across 5 files capturing insect population dynamics, hyperparasitism rates, plant biomass, parasitoid behavior, and attack rates under different light conditions.
- Key data fields and structure include:
  - Week, Cage (mesocosm identity), Block (randomized block design), Treatment (artificial night light treatment, including dark control), Spectra (specific wavelength set; w = white in some experiments).
  - Population counts by species and life stage:
    - Megoura viciae (M.v, M.v.w for winged morphs)
    - Acyrthosiphon pisum (A.p, A.p.w)
    - Aphis fabae (A.f, A.f.w)
    - Parasitoids: Lysiphlebus fabarum (L.f), Aphidius ervi (A.e), Aphidius megourae (A.m)
    - Hyperparasitoids: Dendrocerus carpenteri (D.c), D. dubium (D.d), Asaphes suspensus (A.s), Alloxysta victrix (A.v)
  - Plant biomass: ab.plant (aboveground), root (belowground)
  - Attack and parasitism indicators: mummies (parasitoid success), no/yes hyperparasitoids present
  - Parasitoid distribution: Parasitoid.on.plant (on plant), Parasitoid.cage (on cage side), Parasitoid.near.light (near light source)
- Data are designed to allow analysis of species interactions, light-treatment effects on population trajectories, parasitoid attack rates, and behavioral responses under different spectral conditions.

## Measurements and variables
- In-field population dynamics: weekly abundances of aphids, parasitoids, and hyperparasitoids; mummification rates.
- Behavioral data: parasitoid attack rates over 24 hours; flight-to-light behavior under various spectra.
- Plant metrics: dry biomass (aboveground and belowground) per mesocosm.
- Light and environmental controls: spectral treatment identifiers, photon flux levels, and light-on/off timing to isolate nocturnal effects.
- Functional notes on sampling: initial establishment requirements, replication adjustments due to establishment success, and exclusion of sampling to avoid extinctions when mummy counts are low.

## Quality control and metadata
- Post-entry quality checks comparing data entries to hard-copy records to ensure accuracy of explanatory and response variables.
- Comprehensive data dictionary embedded in the data structure section detailing variable names, units, and coding (e.g., treatment and spectra codes, biomass units, presence flags).
- Experimental metadata includes field site location, mesocosm dimensions, barrier configurations, light-switching protocol, and replication design (randomized block design).

## Potential uses and insights for data leadership
- System-wide data management: demonstrates end-to-end data capture from field experiments to lab validations, with explicit metadata and structured schemas.
- Data discoverability and reuse: clearly defined files and a detailed data-structure description support cross-study comparison and meta-analyses on light-manipulated multi-trophic interactions.
- Data quality and governance: documented quality checks and replication decisions provide a model for maintaining data integrity in complex ecological experiments.
- Practical applications: enables evaluation of how specific light spectra influence insect-plant interactions, parasitoid efficiency, and higher-level ecosystem dynamics under nocturnal illumination.
- Collaboration considerations: dataset arises from a multi-partner project; metadata and variable definitions facilitate integration with other datasets in the broader data ecosystem.

## Provenance and contacts
- Project and data contributors: Dirk Sanders, Kevin J. Gaston, F. J. Frank van Veen, University of Exeter.
- Contact: d.sanders@exeter.ac.uk (primary data originator).