# Silene uniflora Zinc Tolerance Dataset

- Collection/generation methods: Deep water culture experiments conducted between March 2021 and September 2021. Cuttings from wild Silene uniflora plants across 50 populations were propagated under common conditions, then grown for 4 weeks in diluted Hoagland's solution (pH 5.5). Roots were stained with activated charcoal and transferred to fresh Hoagland's with 1000 μM ZnSO4. After 48 hours, root growth was scored.

- Scoring scheme: 0 = no growth; 1 = visible growth; 2 = visible growth with new root growth >30% of original root length. Population tolerance levels are estimated as the mean score per population.

- Nature and units of recorded values: For each population, the record includes the mean root growth score, the standard deviation, and the number of cuttings scored. Geographic positions of scored populations are noted.

- Data structure: The dataset comprises 50 rows, each representing a single population. Columns (in order):
  - Column 1: Population name/code (based on local areas/landmarks)
  - Column 2: Number of cuttings assessed
  - Column 3: Zinc tolerance score (population mean)
  - Column 4: Standard deviation of the zinc tolerance score

- Geolocation and related data: Full population names and geolocations are provided in a connected dataset titled "Site records for Silene uniflora."

- Quality control and provenance: Scoring conducted by a single author (Giles, L.), with 10% of scores verified by the other two authors.

- Notes for data governance and reuse: The dataset provides a structured, comparable measure of zinc tolerance across populations, suitable for cross-population analyses. Limitations include the use of a single primary scorer and a coarse scoring scale (0–2). Geolocation data are housed in a linked dataset, enabling broader context and discoverability.