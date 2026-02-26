# Abstract

- The dataset comes from the NERC project NE/N001672/1, examining effects of artificial light at night on a multi-trophic insect-plant food web.
- Data were collected through field and laboratory experiments with varying light intensities at night (0, 0.1, 1, 5, 10, 20, 50, 100 lux).

## Study system and treatments

- Experimental setup:
  - Randomized block design with 6 blocks, 48 mesocosms total.
  - Light treatments applied to plants: control (no light) and white LED light at multiple lux levels.
- Community composition within mesocosms:
  - Plants: broad bean (Vicia faba, var. Sutton) and barley (Hordeum vulgare).
  - Aphids: Aphis fabae, Acyrthosiphon pisum, Megoura viciae (counts include winged and unwinged morphs).
  - Parasitoids: Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae (attacking the aphids).
  - Generalist parasitoid linking aphid-plant communities: Praon dorsale (attacks M. viciae, A. pisum, S. avenae).
  - Predator-prey linkages occur via the parasitoid network.
- Experimental duration:
  - Field mesocosm experiment started 29 July 2016 and ran for nine weeks.
  - Additional experiments conducted summer 2016 to spring 2018.
- Measurements:
  - Weekly counts of all species on all or half of the plants.
  - Plant biomass (dry weight) measured at experiment end (for 48 mesocosms).
  - Separate experiment to test plant biomass response without aphids under certain light treatments.

## Experimental procedures and data collected

- Parasitoid attack rate and behaviour experiments:
  - Various setups to assess attack rates under different light levels (including day vs night and varying intensities).
  - Detailed protocols for exposing aphids to parasitoids and measuring mummy formation.
- Behavioural tests:
  - Parasitoid locations (on plant vs. away) under defined light conditions.
  - Night/day cycle experiments to observe parasitoid activity and decisions.
- Temperature and lighting conditions:
  - Controlled room experiments (Penryn Campus, University of Exeter) in addition to field sites.
- Data collection cadence:
  - Weekly population counts over nine weeks for field components; end-of-experiment biomass measurements; multiple lab-based behavioural assays.

## Data structure and files

- 8 data files in total:
  - Insect population dynamics and plant biomass (field experiments).
  - Plant biomass from experiments without insects.
  - Parasitoid behaviour and attack rates under different light conditions.
- Key variables and coding (examples):
  - ab.factor: counting density adjustment (1 = 100%, 2 = 50% of insects counted).
  - Block: experimental block identifier (1–6).
  - Treat.lux / Light.lux: light treatment coding at plant height (control and various lux levels).
  - M.v, M.v.w: Megoura viciae counts and winged forms.
  - A.p, A.f, A.f.w: Acyrthosiphon pisum and Aphis fabae counts (and winged forms).
  - S.a, S.a.w: Sitobion avenae counts (and winged forms).
  - L.f, A.e, A.m: mummy counts for the parasitoids Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae.
  - P.dor.m, P.dor.a, P.dor.s: Praon dorsale counts attacking different aphids.
  - Plantbiomass.g: dry weight of plants.
  - Hostdensity: initial aphid host density for 24 h attack period.
  - Aphid.mummies: number of successful parasitoid attacks.
  - First, Light.Dark: experimental sequence of 12 h light/dark settings.
  - Parasitoid.on.plant / Parasitoid.on.side.of.cage / Parasitoid.ceiling: parasitoid distribution observations.
- Data provenance:
  - Field site observations and controlled lab experiments, with specific measurement time points and setups.
- Data quality notes:
  - Quality control performed after data entry by comparing against hardcopy records.
  - One notable data gap: missing plant biomass data due to loss of labels in the field dataset.

## Temporal and organizational details

- Field site and controlled-temperature lab facilities used at University of Exeter (Penryn Campus, UK).
- Timeline:
  - Field experiment runs in 2016 for nine weeks starting late July.
  - Additional experiments conducted through 2016–2018.

## Relevance and potential uses for data management

- Rich, multi-trophic dataset suitable for analyses of how artificial night-light intensity affects insect-plant interactions, parasitoid dynamics, and community structure.
- Clear metadata concepts and naming conventions (blocks, treatments, species codes) support discoverability and reuse.
- The dataset highlights practical data governance considerations:
  - Comprehensive documentation of experimental design and variable coding supports reproducibility.
  - Missing data due to labeling issues underscores the importance of robust field data management and data recovery plans.
  - 8-file structure and detailed variable mapping facilitate integration with broader ecological or data-system workflows.

## Contacts

- Dirk Sanders, University of Exeter (d.sanders@exeter.ac.uk)
- Kevin J. Gaston, University of Exeter
- F.J. Frank van Veen, University of Exeter