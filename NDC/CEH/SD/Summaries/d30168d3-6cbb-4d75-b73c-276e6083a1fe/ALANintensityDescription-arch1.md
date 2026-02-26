# Effects of artificial light on multi-trophic population dynamics

## Overview
- Investigates how artificial light at night (ALAN) across multiple intensities affects a plant–aphid–parasitoid community.
- Experimental setup combines field mesocosms and controlled lab experiments to capture direct and indirect (trophic) effects of ALAN on population dynamics and behavior.
- Data include insect counts, plant biomass, parasitoid attack rates, and parasitoid behavior under varying light levels.

## Experimental Design
- Randomized block design with 6 blocks; 48 mesocosms total.
- Treatments: control (no light) and white LED ALAN at plant height at 0.1, 1, 5, 10, 20, 50, 100 lux.
- Community composition per mesocosm:
  - Plants: broad bean (Vicia faba, var. Sutton) and barley (Hordeum vulgare).
  - Aphids: Aphis fabae, Acyrthosiphon pisum, Megoura viciae (with winged and unwinged morphs counted).
  - Parasitoids: Lysiphlebus fabarum (attacks M. viciae), Aphidius ervi (attacks A. pisum), Aphidius megourae (attacks A. fabae).
  - Generalist parasitoid: Praon dorsale, linking all three aphid species.
- Field component started 29 July 2016; ran for nine weeks, with data collection weekly.
- Additional experiments conducted summer 2016–spring 2018 to explore ALAN effects on plant biomass without aphids and on parasitoid behavior.

## Light Treatments and Experimental Details
- Field mesocosms: 6 blocks × 8 treatments (0, 0.1, 1, 5, 10, 20, 50, 100 lux) × replication; 48 cages total.
- Aphid and parasitoid experiments included variations to test parasitoid attack rates and behavioral responses under different ALAN scenarios (including 0, 1, 5, 20, 100 lux) and day–night settings.
- Lab components examined parasitoid attack success (mummification) and spatial behavior (parasitoids on plant, cage sides, or ceiling).

## Data Collected
- Weekly counts of all species on all plants (including winged and unwinged aphids).
- Plant biomass (dry weight, g) measured at experiment end after drying at 50°C for 48 h; missing labels caused some biomass data gaps.
- Parasitoid attack data: number of mummies after 2 weeks, indicating successful attacks.
- Behavioral observations under light treatments: parasitoid locations (on plant, on cage sides, ceiling/light source).

## Additional Experiments
- ALAN effects on plant biomass without aphids: 30 mesocosms, three-week duration.
- Parasitoid behavior and attack-rate experiments under various ALAN intensities and controlled light conditions.

## Quality Control
- Post-entry data checks against hardcopies to identify and correct errors in explanatory and response variables.

## Data Structure and Variables
- Eight data files covering:
  - Insect population dynamics and plant biomass (field and lab components).
  - Plant biomass without insects.
  - Parasitoid behavior and attack rates under different light conditions.
- Key variables (examples):
  - ab.factor: proportion of insects counted (100% or 50% depending on density).
  - Block, Treat.lux, Light.lux: block and light treatment identifiers.
  - M.v, M.v.w: Megoura viciae counts and winged morphs.
  - A.p, A.f, A.f.w: Acyrthosiphon pisum and Aphis fabae counts and winged morphs; A. f. w refers to winged morphs of A. fabae.
  - S.a, S.a.w: Sitobion avenae counts and winged morphs.
  - L.f, A.e, A.m: Parasitoid counts (Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae) as mummies.
  - P.dor.m, P.dor.a, P.dor.s: Praon dorsale mummies attacking M. viciae, A. pisum, and S. avenae.
  - Plantbiomass.g: Dry weight of plants.
  - Hostdensity: Initial aphid density for parasitoid attacks.
  - Aphid.mummies: Number of mummy aphids after 2 weeks (attack success).
  - First, Light.Dark: Sequence and light regime (12 h dark/light period).
  - Parasitoid.on.plant, Parasitoid.on.side.of.cage, Parasitoid.ceiling: Locations of parasitoids during observations.