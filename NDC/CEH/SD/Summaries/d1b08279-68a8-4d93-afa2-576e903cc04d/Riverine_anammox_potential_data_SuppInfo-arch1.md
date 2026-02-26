# General information: This dataset contains results from slurry incubations with 15N-labelled substrates.

## Overview
- Results from slurry incubations using 15N-labelled substrates to study nitrogen cycling, including anammox and denitrification, in river sediments.
- Two slurry types: anoxic (3 mL vials) and oxic (12 mL vials), prepared from August 2013 sediments; mass spectrometry measurements conducted in September 2013.
- Slurries amended with 14N or 15N tracers; “potentials” rather than in-situ rates, with incubation in the dark at room temperature.
- Data support analysis of nitrogen transformations through 15N-N2 production and linking nitrification to N2 production.

## Experimental setup
- Anoxic slurries: 1 mL wet sediment, 1 mL synthetic river water, N2 headspace; pre-incubation overnight to remove ambient 14N nitrate.
- Oxic slurries: 2.5 mL wet sediment, 3 mL synthetic river water, air headspace.
- Treatments:
  - Reference samples: no 15N-labelled substrate.
  - Control samples: biological activity stopped with zinc chloride before adding 15N-labelled substrate.
  - Time-series samples: zinc chloride injected at predetermined times after 15N-labelled substrate addition.
- Incubations: conducted in the dark at room temperature; results interpreted as potential activity.

## Data structure and columns
- Data organized in a table with 42 columns and 46 rows (including headers); missing values indicated as BDL (below detection limit).
- Time-series columns include 15NOxT0, 15NOxT1, 15NOxT2, 15NOxT3, 15NOxT4, 15NOxT5 (N-15-labelled nitrate+nitrite concentrations over time in oxic slurries).
- Key column groups and examples:
  - P29-15A, P30-15A: production rates of 29N2 and 30N2 after adding 15N-labelled ammonium to anoxic slurries (nmol N2 g-1 dry sediment h-1; 6 h incubation vs control).
  - P29-15A14N, P30-15A14N: production rates after adding 15N-labelled ammonium and 14N-nitrate (anoxic).
  - P29-15N, P30-15N: production rates after adding 15N-labelled nitrate (slope from time series; nmol N2 g-1 dry sediment h-1).
  - Atotal: total anammox activity under anoxic, 15N-nitrate conditions (nmol N2 g-1 dry sediment h-1); calculated using specified equations.
  - ra: relative contribution of anammox to N2 production (%); derived from Atotal and Dtotal.
  - Dtotal: total denitrification; derived from P30-15N and isotope factors.
  - FN-NH4+, FN-NOx, FN-N2: proportions of 15N in ammonium, NOx, and N2 pools; used in mixing models; included when 15N-labelling is detectable.
  - AmmoniumRef, NOxRef: concentrations in oxic reference slurries; units μM; measured by colorimetric methods.
  - 15NOxT0–T5: concentrations of 15N-labelled NOx in oxic time-series samples (μM); derived from a reduction and gas-phase measurement.
  - Oxicp15N-T0–T4, Oxicp15Nrpt-T0–T5: 15N-labelled N2 produced in oxic slurries with ammonium; controls and replicates across occasions to test nitrification-N2 relationships.
  - Oxicp15NATU-T0–T5: similar measurements with allylthiourea (ATU) to inhibit nitrification.
  - O2Conc-T0–T3: dissolved oxygen concentrations in oxic slurries at multiple timepoints (μM); measured with a microelectrode.
  - Replicate: discrete sediment samples collected from each river with five replicates per river.
  - Site labels: Clay, Sand, Chalk categories representing different river sub-catchments; detailed site coordinates provided.

## Calculations and metrics
- 15N2 production metrics:
  - P29, P30: production rates for 29N2 and 30N2 (nmol g-1 dry sediment h-1).
  - P29-15N, P30-15N: production rates after 15N-nitrate addition.
  - P29-15A, P30-15A: production after 15N-ammonium addition in anoxic slurries.
  - p15N: 15N-labelled N2 production, calculated as P29 + 2×P30.
- Atotal and ra:
  - Atotal = FN^-1 × [P29-15N + 2 × (1 − FN^-1) × P30-15N].
  - ra = Atotal / Dtotal × 100, where Dtotal = P30-15N × FN^-2.
  - Detection limits: ~0.03 nmol 29N2 g-1 dsed h-1 for 29N2, ~0.4 nmol 30N2 g-1 dsed h-1 for 30N2, ~1.6 nmol 15N-N2 g-1 dsed h-1.
- Mixing-model proportions:
  - FN-NH4+, FN-NOx, FN-N2 represent 15N fractions in ammonium, NOx, and N2 pools; used to partition nitrogen pools in mixing models; included only when 15N-labelling is above detection.
- 15NOx measurements:
  - 15NOxT0–T5: 15N-labelled NOx concentrations in oxic slurries; detection limit ~0.02 μM.
- Reference measurements:
  - AmmoniumRef and NOxRef provide baseline concentrations for oxic slurries.

## Measurements and detection
- Nitrogen isotopic measurements via mass spectrometry; 15N tracers at 98 atom % 15N.
- NOx and ammonium quantified by automated colorimetry (indophenol blue for NH4+, Griess method for NOx) with defined limits of detection and precision.

## Sites and replicates
- Rivers categorized as Clay, Sand, Chalk within the Hampshire Avon catchment.
- Specific sites with geographic coordinates listed; five replicates per river.

## Time series details
- Timepoints for oxic and anoxic experiments include early (0 h) and multiple post-addition intervals (0.5 h, 1 h, 2 h, 3 h, 6 h).
- Oxic time-series include controls with and without nitrification inhibitors (ATU) to parse nitrification-related N2 production.

## References
- Jensen et al. (2011); Nielsen (1992); Smart & Barko (1985); Thamdrup & Dalsgaard (2000, 2002) – methodological and interpretive references for isotope pairing, anammox, and denitrification calculations.