# Chemical composition of anaerobic digestate and biomass ash blends as a result of storage

## Overview
- Describes a dataset and supporting study examining how adding biomass ash affects nutrient stability in anaerobic digestate (digestate) over time.
- Focuses on ammonium content and other labile agronomic components (nitrogen and sulfur), comparing ash-amended and un-amended digestates.
- Based on time-series experiments using digestates from UK industrial plants and biomass ashes, with and without acidification, monitored for several months.

## Data access and citation
- Data access: https://doi.org/10.5285/e91e8c28-0176-4c5b-9b20-611eb505ab39
- Suggested data citation: Lag-Brotons, A.J.; Thompkins, D.; Burguess, A.; Marshall, R.; Herbert, B.; Hurst, L.; Semple, K.T. (2020). Chemical composition of anaerobic digestate and biomass ash blends as a result of storage. NERC Environmental Information Data Centre. Dataset. https://doi.org/10.5285/e91e8c28-01764c5b-9b20-611eb505ab39

## Datasets and measurements
- Primary data file: WP1B.csv (key for dataset).
- Measurements include:
  - Dry solids (DS) and pH
  - Total Kjeldahl Nitrogen (TKN) on fresh and dry basis (TKNf, TKNd)
  - Total sulfur (TS) on fresh and dry basis (TSf, TSd)
  - Additional elemental nutrients documented for digestates and ash fractions (e.g., P, K, Ca, Mg, Fe, Zn, Cu, Mn, S, Cl, B, Mo, etc.)
- Units and methods are specified (e.g., DS as a percentage; TKN, TS, and other elements in mg/kg or g/kg depending on the parameter; methods referenced such as APHA standards).

## Materials and treatments
- Digestates (examples include D1, D2, D1A1, D2A1) sourced from different feedstocks and life stages of anaerobic digestion plants.
- Biomass ashes (fractions A1, A2; e.g., fly ash) as waste from biomass combustion.
- Treatments involve:
  - Digestate only (D1, D2)
  - Digestate plus ash (D1A1, D2A1)
  - Acidified variants (AD1, AD2; and AD1A1, AD2A1) where 98% sulfuric acid is added to achieve target pH of 5.5
- Table 4 summarizes treatment configurations and the volume of 98% H2SO4 added per litre to reach pH 5.5 (or not added).
- Nine litres of each substrate/treatment are prepared and divided into three replicates per treatment.
- Treatments are stored indoors at ~20°C.

## Experimental design and procedure
- Time-course sampling at days: 0, 1, 2, 4, 8, 16, 32, 64, 128.
- Substrates tested:
  - Digestates alone (D1, D2)
  - Digestates with ash (D1A1, D2A1)
  - Acidified digestates (AD1, AD2)
  - Acidified digestates with ash (AD1A1, AD2A1)
- Acidification foaming observed:
  - Addition of concentrated sulfuric acid caused foaming; required vigorous agitation to reach pH 5.5.
  - Foaming and agitation requirements raise practical considerations for commercial scale digestate acidification.
- Analyses conducted as per the listed analytical suite (see Table 5).

## Analytical methods
- Analytical suite includes:
  - Dry solids (DS) by standard methods (e.g., oven/drying protocols)
  - pH (acid-base measurements)
  - Total Kjeldahl Nitrogen (TKN) on fresh and dry bases
  - Total Sulphur (TS) on fresh and dry bases
  - Additional elemental analyses (as listed in Tables 2 and 3 for digestates and ash fractions)
- Methods referenced include standard APHA methods and related soil/digestate analysis procedures (e.g., JAS and 2540 B3 for DS; 4500-H+ for pH; 48 TKN for TKNf).

## Dataset metadata and structure
- WP1B.csv provides:
  - Treatment (material and acidification status)
  - Material (D1, D2, D1A1, D2A1, AD1, AD2, AD1A1, AD2A1)
  - Acid (Yes/No) and Volume of 98% H2SO4 added (ml per litre)
  - Days (time since start, in days)
  - Replicate (a, b, c)
  - Measured variables: pH, DS (%), TKNf (mg N/kg fresh), TKNd (mg N/kg dry), TSf (mg S/kg fresh), TSd (mg S/kg dry), plus related concentrations for other elements (e.g., P, K, Ca, Mg, Fe, Zn, Cu, Mn, S, Cl, B, Mo) as per the supplementary tables.
- Key definitions and units are provided to ensure correct interpretation of the data (e.g., fresh vs dry basis, units for each parameter).

## Practical use for data support
- Potential products for end users:
  - Dashboards comparing nutrient stability (N, S, trace elements) across digestate treatments and ash amendments over time.
  - Self-serve data views showing effects of ash addition and acidification on ammonium retention, pH trajectories, and dry solids changes.
  - Comparative analyses integrating feedstock type with nutrient outcomes to inform waste-to-resource strategies.
- Data integration opportunities:
  - Link WP1B.csv measurements with the accompanying digestate/ash metadata (Tables 1–3) to build a full picture of composition and treatment effects.
  - Combine with time-series visualization to observe trends in TKNf, TKNd, TSf, TSd, and DS across days and treatments.

## Limitations and caveats
- Foaming during acidification is a notable practical challenge that may affect scaling and process control.
- Data are from controlled experimental conditions with 9 L samples; extrapolation to commercial-scale operations should consider scale effects.
- The study focuses on specific digestate/ash combinations and time points; broader applicability should consider additional feedstocks and ash sources.

## Authors and contact
- Dr. Alfonso Jose Lag Brotons
- Dr. David Thompkins
- Andy Burgess
- Dr. Rachel Marshall
- Ben Herbert
- Dr. Lois Hurst
- Prof. Kirk T. Semple

- For correspondence: respective emails listed in the metadata.