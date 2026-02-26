# MealwormPredationRates

## Context and Purpose
- Study location: three oil palm estates in Riau Province, Sumatra, Indonesia (Ujung Tanjung, Kandista, Libo) owned by Pt Ivo Mas Tunggal.
- Experimental aims: quantify predation pressure on mealworms as a proxy for environmental predation risk across mature and replanted oil palm stands; part of the Biodiversity and Ecosystem Function in Tropical Agriculture project and BEFTA/NERC initiatives.
- Design purpose within monitoring: provides a structured dataset to evaluate predation dynamics by vertical stratum (crown vs ground) and management treatments, informing monitoring frameworks for ecosystem function and biodiversity responses.

## Experimental Design
- Plots and timing:
  - 18 plots established in 2013 (Biodiversity and Ecosystem Function in Tropical Agriculture project); estates include mature (Ujung Tanjung, Kandista) and replanted (Libo) stands.
  - Predation measured in 2014 (mature) and 2016–2017 (both mature and replanted).
- Treatments and sampling:
  - Factorial design with exclusion (caged) vs non-exclusion (uncaged) and canopy vs ground exposure.
  - Each plot contains three test palms per randomization; six mealworms per test.
  - Exposure duration ~24 hours per sampling event.
- Measurement unit:
  - Response is the total number of mealworms remaining (out of six) after exposure; half-worms counted as applicable.
- Sampling structure:
  - Palm-level sampling with precise palm numbers and plot coordinates; trials conducted at three compass-based positions per plot.

## Data Collected and Units
- Primary variable:
  - worms_remaining: number of mealworms still present after ~24 hours (0–6).
- Experimental treatments:
  - wormtreat: categories indicating cage presence and position (Remain_top_nocage, Remain_top_cage, Remain_base_nocage, Remain_base_cage).
- Sampling metadata:
  - Date_set, Time_set: when larvae were placed.
  - Date_coll, Time_coll: when remaining larvae were counted.
  - Period: discrete sampling interval within the experiment.
  - Plot and estate identifiers: Plot_no (e.g., C01), Estate_abbrev (KNDE, UTNE, LIBE), Triplet grouping.
  - Palm: palm identifier on each plot.
- Environmental and ancillary data:
  - dayrain: rainfall over the 24-hour period (8 am–8 am) at nearest weather station.
  - Ants characteristic and Ants Quantity: qualitative/quantitative ant presence where observed.
  - distance: distance to palm center for ant-exclosure analyses (2016–2017).
  - All_notes: field observations and data-entry notes; includes data-check updates (e.g., 2018 data verification).
- Data management signals:
  - 50% of data entry cross-checked against original field sheets; error rate <1%; changes recorded with provenance.

## Data Format and Files
- Three CSV files (thin format; one observation per line):
  - MealwormPredationRates_2013_2014.csv
  - MealwormPredationRates_2016_2017.csv
  - MealwormPredationRates_replants.csv
- Key fields include:
  - Estate_abbrev, Plot_no, Triplet, Treatment, Palm, Period, Date_set, Time_set, Date_coll, Time_coll, wormtreat, worms_remaining, Ants characteristic/Ants Quantity, All_notes, dayrain, distance (where applicable).

## Quality Control and Provenance
- Basic data validity checks performed (e.g., impossible values, date ranges, formatting).
- 50% of data entries re-checked against original field sheets; error rate <1%.
- All changes documented; provenance retained with the dataset.

## Miscellaneous and Funding
- BEFTA core plots data (KNDE and UTNE) from 2013–2014.
- BEFTA core plots data funded by NERC (2016–2017).
- Replanted plots (LIBE) data funded by NERC.
- Randomisation for palm selection was generated via Excel; data coordinates and plotting details provided to support traceability and reproducibility.

## Relevance for Monitoring Frameworks
- Demonstrates a structured approach to selecting and recording environmental health indicators (predation pressure) across management regimes and stand types.
- Supports data governance needs: explicit variable definitions, metadata-rich fields, and traceable data lineage.
- Illustrates handling of data gaps and barriers common in monitoring datasets (e.g., data sharing considerations, need for consistent metadata, and open data readiness).
- Provides a model for integrating ecological response measurements with temporal (2013–2017) and spatial (estates, plots, palms) scales to inform policy and decision-making in environmental health monitoring.