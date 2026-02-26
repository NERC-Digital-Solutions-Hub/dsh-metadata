# FADOE_yield.csv

## Overview
- Dataset of post-flowering yield characteristics for Brassica nigra plants grown under Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Collected over two years (2018 and 2019) across two field locations with four pollution treatments (D, O3, D+O3, CON) and two rings per treatment.

## Experimental design
- Treatment structure: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON).
- Replication: 2 rings per treatment (8 rings total).
- Plant density and sampling: 24 plants per ring.
- Spatial/temporal replication: rings moved from one field (2018) to an adjacent field (2019); field coordinates provided for each year.

## Data collected and derived measurements
- Plant- and pod-level metrics:
  - Year, Ring, Treatment, Plant no.
  - No. developed pods; No. undeveloped pods; % pod development (derived)
  - No. pods bagged (ten random pods); Mass of pods; Pod mass (per pod)
  - No. seeds (pods); Mass of seeds in bagged pods
  - No. seeds total (including seeds in pods); Seed mass total (including seeds in pods)
  - Plant dry mass
  - No. seeds (plant); Seed mass (plant)
- Derived analyses enabled:
  - Pod development efficiency per plant
  - Seeds per pod; total seed output per plant
  - Relationships between vegetative mass, pod development, and seed yield

## Data collection and processing notes
- Harvest protocol: plants harvested after flowering ended, matured in insect mesh-covered polytunnel to prevent additional insect damage, then harvested.
- Pod and seed processing: ten random pods per plant or per ring collected, oven-dried at 70 °C, weighed; pod and seed counts/masses recorded.
- Data organization: variables are linked by Year, Ring, and Treatment to enable analysis of treatment effects, year effects, and spatial replication.

## Analytics opportunities for an Analyst
- Assess effects of D, O3, and D+O3 versus CON on pod development, seed production, and seed mass.
- Compare year-to-year differences and the impact of moving rings between fields.
- Explore correlations between plant dry mass and seed yield, as well as seed yield components (pods produced, seeds per pod, total seeds).
- Develop predictive models linking treatment, year, and plant-level metrics to yield outcomes; quantify uncertainty with replication at the ring level.
- Integrate data across metrics to inform practical decisions about pollutant exposure and crop yield under environmental stress.