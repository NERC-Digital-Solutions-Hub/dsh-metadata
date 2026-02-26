# Effects of artificial light on multi-trophic population dynamics

## Overview
- Datasets from the NERC project NE/N001672/1 examining effects of artificial night-time light on multi-trophic interactions.
- Data include direct observations of insects and plants from field and laboratory experiments.
- Experimental focus: varying artificial light intensities (0, 0.1, 1, 5, 10, 20, 50, 100 lux) and their impact on an insect food web.
- Field site and controlled-temperature laboratory at Penryn Campus, University of Exeter, UK.
- Field experiment ran for nine weeks starting 29 July 2016; additional experiments conducted 2016–2018.
- Measured outcomes: insect abundances (including winged/unwinged morphs), plant biomass, parasitoid attack rates, and parasitoid behavioral responses to light.

## Experimental design
- Field experiment: randomized block design with 6 blocks; 8 light treatments (control plus seven lux levels) applied at plant height.
- Replication: six replicates per treatment, total of 48 mesocosms.
- Communities per mesocosm:
  - Plants: broad bean (Vicia faba) and barley (Hordeum vulgare).
  - Aphids: Aphis fabae, Acyrthosiphon pisum, Megoura viciae.
  - Parasitoids (specialists): Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae.
  - Generalist parasitoid linking to measured aphids: Praon dorsale.
- Data collection: weekly counts of all species on all or half of the plants for 9 weeks; plant biomass measured at end after drying.
- Additional experiments:
  - Light treatments without aphids: 30 mesocosms; 2-week-old broad beans; biomass measured after 3 weeks.
  - Parasitoid behavior and attack-rate experiments under different light conditions (including day/night contrasts and varying lux).

## Data collected
- Population dynamics: counts by species, with winged vs. unwinged aphids.
- Behavioral data: parasitoid location (on plant vs. other parts of cage), distance from light source, and position relative to light.
- Attack outcomes: mummy counts after 2 weeks as measure of successful parasitoid attacks; experiments comparing dark vs light periods.
- Plant biomass: dry weight (g) of plants at experiment end; note for field biomass some data are missing due to label loss.
- Experimental metadata: treatment identifiers and hierarchical structure (blocks, mesocosm IDs, initial host densities, etc.).

## Data structure and files
- Eight data files capturing insect dynamics, plant biomass (with and without insects), and parasitoid behavior/attack data.
- Key variables and codes include:
  - ab.factor, Block, Treat.lux, Light.lux
  - M.v (Megoura viciae), M.v.w (winged M.viciae), A.p (Acyrthosiphon pisum), A.f (Aphis fabae), A.f.w (winged A. fabae), S.a (Sitobion avenae), S.a.w
  - L.f, A.e, A.m (parasitoids: Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae)
  - P.dor.m, P.dor.a, P.dor.s (Praon dorsale attacks on respective aphids)
  - Plantbiomass.g, Hostdensity, Aphid.mummies
  - First, Light.Dark, Parasitoid.on.plant, Parasitoid.on.side.of.cage, Parasitoid.ceiling
- Data are organized to enable dose–response and multi-trophic interaction analyses across light treatments.

## Quality control and limitations
- Post-entry validation against hard-copy records performed to ensure accuracy.
- Noted data gaps: missing plant biomass data due to label loss in the field dataset.
- Some counts per cage involve a factor (ab.factor) adjusting for partial counting (100% or 50%).

## How this supports data use
- Enables investigation of how varying artificial night-light intensities influence multi-trophic dynamics among plants, aphids, and parasitoids.
- Facilitates analyses linking light exposure to:
  - Aphid population growth and winged/unwinged morph proportions
  - Parasitoid attack success and behavioral responses to light
  - Overall plant biomass outcomes under different light regimes
- Data are well-documented with explicit experimental design, units, and variable codings, supporting reproducible analysis and creation of data products (dashboards, pivot tables, visualization charts).

## Access and contact
- Researchers: Dirk Sanders, Kevin J. Gaston, F.J. Frank van Veen, University of Exeter.
- Primary contact: d.sanders@exeter.ac.uk
- Data provenance: NE/N001672/1 project on artificial light and multi-trophic population dynamics.