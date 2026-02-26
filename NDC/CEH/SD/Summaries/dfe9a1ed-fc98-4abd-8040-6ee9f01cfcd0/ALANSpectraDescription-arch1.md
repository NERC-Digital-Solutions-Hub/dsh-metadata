# Abstract

- This dataset arises from the NERC project on the effects of artificial light on multi-trophic population dynamics and includes field and lab observations of insects and plants under different light spectra.
- Experimental system: aphid–parasitoid–hyperparasitoid interactions using broad beans (Vicia faba) and aphids (Aphis fabae, Acyrthosiphon pisum, Megoura viciae) with a specialist parasitoid (Aphidius megourae) and hyperparasitoids.
- Field setup: 47.5 cm cube Bug Dorm mesocosms deployed in a Cornwall field site near the University of Exeter; 17 weeks of population monitoring (June–October 2017) with 2 pots of beans per week, expanding to 8 pots per mesocosm.
- Light treatments: seven monochromatic spectra with a single peak in the visible/near-UV (385, 447, 469, 475, 518, 607, 630 nm) plus a dark control; photon flux near 7.1 μmol m^-2 s^-1 (20 lux) for all spectra except UV (2.4 μmol m^-2 s^-1 due to energy constraints). Artificial lights on at night via dusk-dawn sensor (70 lux to 110 lux) with light barriers to prevent spillover.
- Replication and design: initial 7 replicates per treatment; analyses include 6 replicates for red/green and 5 for UV after excluding non-established runs; complete caging to prevent cross-treatment light leakage.
- Data collected in the field: weekly counts of aphids and parasitoid mummies (parasitoids), hyperparasitoid presence, and plant biomass measurements; sampling of aphid mummies for hyperparasitoid identification (weeks 12 and 14); in-cage netting allowed 97% light transmission for plant measurements.
- Mechanistic lab experiments: (i) 24-hour parasitoid attack rate and (ii) parasitoid flight-to-light behaviour under all light treatments, conducted at 20 lux with a white-light control; experiments used standardized aphid and parasitoid densities and temperatures (20°C, 16:8 L:D).
- Data quality and structure: post-entry error checks against hard copies; dataset comprises five files detailing insect population dynamics, hyperparasitism rates, plant biomass, and parasitoid behaviour/attack rates under different light conditions.
- Key variables and data structure:
  - Temporal and experimental identifiers: Week, Cage (mesocosm), Block, Treatment, Spectra
  - Biological counts: Megoura viciae, Acyrthosiphon pisum, Aphis fabae; winged morphs where recorded; parasitoids (Aphidius megourae and others); mummy counts; hyperparasitoids (e.g., Alloxystini)
  - Plant metrics: above- and below-ground dry biomass
  - Behavioral measures: parasitoid on-plant presence, cage-side presence, proximity to light (near-light)
- Authors and contact: Dirk Sanders, Kevin J. Gaston, F. J. Frank van Veen, University of Exeter (emails provided in the dataset summary)

- Implications for analysts: enables identification of wavelength-specific impacts on multi-trophic population dynamics, estimation of spectral effects on attack rates and parasitoid behaviour, and assessment of how artificial light spectra may alter predator–prey–hyperparasitoid interactions and plant biomass under nocturnal illumination.