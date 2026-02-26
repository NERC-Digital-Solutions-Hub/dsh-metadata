# Abstract

- Data from the NERC project NE/N001672/1 on the effects of artificial light at night on multi-trophic population dynamics.
- Focus: direct observations of insects and plants in field and laboratory experiments using coloured near-monochromatic LEDs with peaks at 385, 447, 469, 475, 518, 607, and 630 nm plus a dark control.
- Light flux: about 7.1 μmol m^-2 s^-1 (roughly 20 lux) for all treatments except UV, which used 2.4 μmol m^-2 s^-1 due to safety limits.
- Datasets cover insect numbers, plant biomass, parasitoid attacks, and parasitoid behavior under different spectra; data collected in field at Penryn Campus and in a controlled laboratory setting.
- Field and lab experiments conducted 2017–2018; authors: Dirk Sanders, Kevin J. Gaston, F.J. Frank van Veen, University of Exeter.

## Experimental design

- Field experiment
  - Setting: 47.5 cm cube Bug Dorm mesocosms arranged 1.5 m apart in a field near the University of Exeter (Cornwall, UK).
  - Communities: broad beans (Vicia faba) hosting three aphid species (Aphis fabae, Acyrthosiphon pisum, Megoura viciae) and a parasitoid (Aphidius megourae) with hyperparasitoids present (endophagous Alloxystini; generalist ectophagous).
  - Procedure: start with 2 pots per mesocosm, increasing to 8 pots; 7 spectra treatments plus dark control; photon flux maintained ~7.1 μmol m^-2 s^-1 (white LED ~20 lux); dark control exposed to natural nightlight; lights on at night by dusk-dawn sensor (70 lux on, 110 lux off); light barriers between cages.
  - Replication and sampling: initial 7 replicates/treatment; analyses used 6 replicates for red/green, 5 for UV due to establishment criteria.
  - Measurements: weekly counts of aphids and parasitoid mummies from half the plants per cage; full cage checks if a species was absent; weeks 12 & 14 included sampling of 10% mummies ( lab rearing to identify hyperparasitoids ); week 10 plant biomass after 2 weeks growth in a netted cage to exclude aphids.
  - Light monitoring: 20 lux white-light reference; UV treatment flux adjusted to safe levels; barriers prevented light spillover.

- Laboratory experiments
  - (i) 24-hour attack rate: 150 third-instar Megoura viciae aphids on single 2-week-old plants; one Aphidius megourae female per cage for 24 hours; 20°C, 16:8 L:D; after 2 weeks, count mummies.
  - (ii) Parasitoid flight to light: 2-week-old bean plants with 150 aphids placed in darkness; release 20 mated female parasitoids; after 1 hour record locations (on plant vs elsewhere); 6 replicates per treatment.
  - Light conditions: all field spectra replicated under laboratory conditions at 20 lux, with an additional white-light control.

## Treatments and conditions

- Spectra: 385, 447, 469, 475, 518, 607, 630 nm plus dark control; in some lab tests, a white LED treatment included.
- Light levels: field treatments around 7.1 μmol m^-2 s^-1 (except UV 2.4 μmol m^-2 s^-1); field experiments used dusk-dawn activated lighting; lab experiments kept at 20 lux for comparability.

## Data collected

- Insect populations: counts of Megoura viciae (M.v.), Acyrthosiphon pisum (A.p.), Aphis fabae (A.f.); winged morphs where recorded.
- Parasitoids and hyperparasitoids: mummies for Aphidius megourae and other parasitoids (Aphidius ervi, Lysiphlebus fabarum), hyperparasitoid taxa (e.g., Alloxystini, Asaphes suspensus, Alloxysta victrix).
- Plant data: aboveground and belowground dry biomass.
- Behavioral data: parasitoid attack rates and parasitoid-flight behavior relative to light source.
- Experimental context: treatment identifiers, replicate/block structure, sampling week, cage/mesocosm IDs, and depth of sampling (abundance factor).

## Data structure and variables

- Five data files capturing:
  - Insect population dynamics in field mesocosms with hyperparasitism data.
  - Plant biomass measurements.
  - Parasitoid behavior data (on-plant counts, cage locations, near-light observations).
  - Parasitoid attack rate data (lab experiments).
  - Hyperparasitoid presence/absence and counts.
- Key fields and codes:
  - Week, Cage (1–48), Abundance.factor (1 or 2), Block (experimental block), Treatment (C; color spectra; w for white; o/p/... codes), Spectra (spectral treatment).
  - Species counts: M.v., M.v.w, A.p, A.p.w, A.f, A.f.w; L.f (mummies of Lysiphlebus fabarum), A.e (Aphidius ervi), A.m (Aphidius megourae), D.c, D.d, A.s, A.v (hyperparasitoids).
  - Plant biomass: ab.plant (aboveground), root (belowground).
  - Aphids and mummies counts, hyperparasitoids present/absent, parasitoid on plant, cage, near light observations.

## Quality control and data management

- Post-entry error checking against hardcopy records.
- Clear documentation of data structure and variable definitions to facilitate reuse and reinterpretation.

## Provisional data use notes

- Enables analysis of how specific light spectra influence multi-trophic interactions among aphids, parasitoids, hyperparasitoids, and host plants.
- Provides field-realistic and controlled-condition contrasts to assess spectral effects on population dynamics and behavior.
- Detailed data dictionary and recording schema support data integration, re-use in dashboards or reports, and reproducible analyses across related datasets.