# Supporting documentation

## Dataset overview
- Contains a single CSV file: Ecolidatafaeces.csv
- Has 38 columns describing sampling, animals, farmlets, cohort, medicating details, E. coli counts (across dilutions), and derived metrics
- Columns cover:
  - Sampling metadata: Sample number, Sample type, Collection method (freshly voided, floor, grab from rectum), Sampling date
  - Animal/group metadata: Animal 1–4 IDs, Farmlet (blue, green, or red), Cohort (1 or 2)
  - Treatments and timing: Date Medicated, Medication, Reason for medication
  - E. coli counts: E.coli at dilutions 10-1 to 10-4; antibiotic-specific counts (Tet, Ceph, Marb, Merop) across dilutions
  - Derived counts/weights: Mean E.coli CFU/g wet weight, Mean Log E.coli CFU/g wet weight, Mean E.coli CFU/g dry weight, Mean Log10 E.coli CFU/dry wt g-1
  - Antibiotic-augmented data: E.coli Tet 10-1..10-3, Ceph 10-1..10-3, Marb 10-1, Merop 10-1 with corresponding means
  - Sample composition metrics: % DM (gravimetric dry matter), TMC (too many colonies to count), NS (not sampled), ND (no data)

## Data structure and key variables
- Pooling and design:
  - Animals pooled at initial sampling to prepare sequence libraries; nine libraries from 30 animals grouped as 3, 3, and 4 per farmlet
  - Animal IDs (1–4) identify the pooled group
- Farmlet classification:
  - Farmlets identified on the North Wyke farm platform with color labels: blue, green, red
- Measurements and transformations:
  - Raw counts at multiple dilutions (10-1 to 10-4)
  - Wet weight CFU/g and dry weight CFU/g
  - Log10 transformations for both wet and dry weight metrics
- Antibiotic conditions:
  - Data includes counts and derived metrics for plates containing Tet (tetracycline), Ceph (cephalexin), Marb (marbofloxacin), and Merop (meropenem)

## Methods
- Sample processing:
  - 1 g faecal material transferred into 9 ml sterile Ringers; serial 10-fold dilutions prepared
  - 0.1 ml aliquots plated in duplicate on Membrane Lactose Glucuronide Agar (MLGA)
  - Antibiotics added to MLGA at specified concentrations after autoclaving and prior to pouring plates:
    - 16 mg/l tetracycline
    - 16 mg/l cephalexin
    - 1.0 mg/l marbofloxacin
    - 8 mg/l meropenem
  - Incubation: plates dried, inverted, incubated at 44.5 ± 0.2°C for 18–24 h
- Moisture and dry matter determination:
  - Gravimetric moisture: ~50 g faecal material dried at 105°C to constant weight
  - % dry matter calculated as 100 - ((fresh wt. - dry wt.) / fresh wt.) × 100
- Licensing:
  - Establishment licence XA11784A2
  - Project licence P592D2677

## Experimental design and provenance
- Sampling strategy:
  - Animals pooled at initial sampling to enable library preparation; nine libraries from 30 animals grouped by farmlet
- Geographic/context note:
  - Farmlets identified as blue, green, or red from the North Wyke farm platform

## Data quality, completeness, and limitations
- Missing data indicators:
  - NS = not sampled
  - ND = no data
- Data characteristics to consider in GIS contexts:
  - Primarily laboratory-derived counts and derived metrics; spatial context is provided only at the farmlet level (no explicit coordinates in the document)
  - Data resolution is at the sample/animal/farmlet level with pooling, which may affect spatial analysis granularity

## GIS relevance and potential use cases
- Suitable for map-based visualization of:
  - Distribution of E. coli counts and antibiotic resistance indicators by farmlet
  - Temporal and treatment-related patterns (medication dates, drug reasons) across cohorts
  - Comparison of wet vs. dry weight CFU/g and corresponding log-transformed values by farmlet
- Join opportunities:
  - Could be joined with spatial boundaries or shapefiles for North Wyke farm platform to produce farmlet-level choropleth or point-based summaries
- Data preparation considerations for GIS:
  - If coordinate data are unavailable, assign centroid or farmlet-level geometry for visualization
  - Acknowledge pooling and sample-level aggregation when interpreting spatial patterns
  - Handle NS/ND fields explicitly to avoid misinterpretation in analyses

## Licensing and access
- Licences referenced:
  - Establishment licence XA11784A2
  - Project licence P592D2677