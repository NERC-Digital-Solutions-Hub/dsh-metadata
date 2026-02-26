# FADOE_visitation.csv

- Overview
  - Data on Brassica nigra flower visitation frequencies by pollinating insects in 2018 and 2019 from Free-Air Diesel and Ozone Enrichment (FADOE) rings.
  - Experimental settings include four pollution treatments (diesel exhaust [D], ozone [O3], diesel exhaust + ozone [D+O3], and a control [CON]) across multiple rings.
  - Observations captured by trained observers over 5–10 minutes per observation unit.

- Experimental design and collection
  - Observation unit: a patch of 6 adjacent plants; observers recorded insect visits and flower counts.
  - Rings: each year had multiple rings; rings were distributed within a field of wheat and moved to an adjacent field in 2019, yielding two locations per ring.
  - Treatments: within each year, two rings were assigned to each of four treatments (D, O3, D+O3, CON); ring positions remained constant across the year with a one-week spatial rotation in 2019.
  - Rotation: during one week in 2019, plant and treatment assignments were rotated so that control rings became diesel-polluted rings and ozone rings became the combined treatment rings (and vice versa) to quantify spatial variation in pollinator foraging behavior.
  - Observation details: each observation recorded the Field Year, Date, Start time, Finish time, and Duration (5–10 minutes), with a trained recorder identifying insects.

- Location and sampling specifics
  - Rings numbered (Ring) and assigned to locations (Location) with precise latitude/longitude provided for 2018 and 2019.
  - Data include per-ring, per-year geographic placement and tracking of how rings moved between fields.

- Pollinators and metrics collected
  - Insect counts by pollinator group (e.g., honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth, and several other groups including beetles, hemiptera, parasitic wasps, and unknowns).
  - Flower visitation data by pollinator group (the six focal groups: honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth).
  - Total insect counts, total flower visits, and visits per insect were calculated.
  - Flower counts within observation periods were recorded.

- Data processing and derived measures
  - Visitation frequencies scaled by the number of flowers and survey duration to derive rates:
    - Insect counts per flower per hour
    - Flower visits per insect per hour
  - For each pollinator group, the average number of visits to flowers was calculated.
  - Derived metrics include total counts, total visits, and visits per insect, normalized to facilitate comparisons across rings, treatments, and time.

- Temporal and data structure notes
  - Temporal coverage: 2018 and 2019; data organized by Year and Date, with explicit Start/Finish times and observation durations.
  - Data structure captures multiple dimensions: ring, location, treatment, rotation status, year, date, and pollinator category, along with per-observation counts and derived rates.