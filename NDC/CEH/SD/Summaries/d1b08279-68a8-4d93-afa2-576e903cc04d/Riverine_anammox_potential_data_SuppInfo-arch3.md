# Dataset from Slurry Incubations with 15N-labelled Substrates

## Overview
- Describes results from slurry incubations using 15N-labelled substrates to study nitrogen cycling processes (notably anammox and denitrification) in river sediments.
- Experimental setup includes anoxic and oxic slurries:
  - Anoxic: 3 mL vials with 1 mL wet sediment, 1 mL synthetic river water, nitrogen gas headspace.
  - Oxic: 12 mL vials with 2.5 mL sediment, 3 mL synthetic river water, air headspace.
- Sediments collected in August 2013; mass spectrometry measurements performed September 2013.
- Slurries amended with combinations of natural abundance 14N and 15N-labelled substrates; N-amendments injected through vial septa.
- Target nitrate or ammonium concentrations after tracer addition: 100 µM (clay), 300 µM (sand), 500 µM (ammonium) across sediment types.
- Experiment includes reference samples (no 15N), control samples (biological activity stopped with zinc chloride), and time-series samples (zinc chloride added at set times after tracer addition). Incubations are conducted in the dark at room temperature and are interpreted as potential rather than in-situ rates.
- Data structure comprises 42 columns and 46 rows, with some values below detection marked as BDL.

## Study Sites and Replication
- Location: rivers in the Hampshire Avon catchment.
- Sub-catchment types: Clay, Sand, Chalk representing clay-dominant, greensand-dominant, and chalk-dominant sites.
- Site identifiers and coordinates:
  - Clay: Clay 1 (River Sem), Clay 2 (Sem tributary), Clay 3 (Sem tributary) with respective coordinates provided.
  - Sand: Sand 1 (River Nadder), Sand 2 (west branch of River Avon), Sand 3 (west branch of River Avon) with coordinates.
  - Chalk: Chalk 1 (River Ebble), Chalk 2 (River Wylye), Chalk 3 (east branch of River Avon) with coordinates.
- Replicates: 5 replicates per river.

## Experimental Design and Key Measurements
- Substrates and tracers:
  - 15N-labelled substrates (high isotopic purity ~98 atom % 15N).
  - Additional injections of 14N (natural abundance) used in combination with 15N tracers.
- Time-series sampling:
  - 15NOx time series in oxic slurries: T0, T1 (~0.5 h), T2 (~1 h), T3 (~2 h), T4 (~3 h), T5 (~6 h) after 15N-labelled nitrate addition.
  - Ammonium tracers (15N) with time-series measurements and corresponding controls.
- Measurements and calculations:
  - 15N-N2 production tracked by mass spectrometry; P29 and P30 denote production of N2 with mass-to-charge ratios 29 and 30.
  - p15N denotes production of 15N-N2, calculated as P29 + 2×P30.
  - Headspace N2 and aqueous N2 concentrations calculated via Thamdrup and Dalsgaard methods; conversion to nmol per g dry sediment.
  - Rates derived from time-series with linear trend lines (nmol N2 g−1 d−1 or h−1 depending on data).
  - Atotal: total anammox activity in 15N-nitrate incubations (Anammox + nitrate coupling) calculated using FN (15N-label in nitrate tracer, FN ≈ 0.98) and P29/P30 as per Thamdrup & Dalsgaard (2002).
  - ra: contribution of anammox to total N2 production, expressed as a percentage (Dtotal determined from P30; Atotal from 15N experiments).
  - FN-NH4+, FN-NOx, FN-N2: proportions of 15N-label in ammonium, NOx, and N2 pools, used in isotope-mlabel mixing models; included only when 15N-labelled pools were detectable.
  - NOxRef and AmmoniumRef: reference concentrations for oxic slurries (microM) measured by colorimetry; NOx via Griess method with cadmium reduction; NH4+ via indophenol blue method.
  - 15NOxT0 to 15NOxT5: concentrations of 15N-labelled nitrate+nitrite in oxic time-series samples.
  - O2Conc-T0 to O2Conc-T3: dissolved oxygen in oxic slurries at measurement times.
- Analytical methods:
  - Nitrate/nitrite and ammonium concentrations measured by automated colorimetry; 15N-N2 quantified by mass spectrometry after reduction steps (sulphamic acid treatment for N2 analysis in the headspace).
  - Calibration with standards and standard reference materials; detection limits provided for each measurement type.
- Data structure and headers:
  - Data organized in a table with 42 columns and 46 rows; numerous time-series columns for 15NOx and related metrics.
  - Column headers detailed in a dedicated section describing site, replicate, and measured parameters (e.g., P29-15A, P30-15A, Atotal, ra, 15NOxT0–T5, FN-NH4+, FN-NOx, FN-N2, Oxicp15N-T0..T4, Oxicp15Nrpt-T0..T4, Oxicp15NATU-T0..T5, O2Conc-T0..T3).

## Data Quality, Limitations, and Interpretation
- Outputs represent potential rates from controlled slurry experiments, not in-situ runtime rates in the environment.
- Detection limits are specified for all key measurements.
- Some values are marked as BD(L) where below detection limit.
- The experiment includes replication and reference controls to identify biological activity versus background processes.
- The design includes measures to isolate nitrification effects (e.g., allylthiourea in ATU experiments) to test the relationship between nitrification and N2 production.

## Metadata and Data Handling
- Sediment handling and pre-treatment details:
  - Anoxic slurries pre-incubated overnight before addition of 15N-labelled substrates to remove ambient 14N-nitrate.
  - Water samples filtered through 0.45 µm filters and frozen for later analysis (within 3 months).
- Data processing notes:
  - Headspace and aqueous N2 concentrations computed with gas-phase/isotopic balance equations.
  - Total moles per vial scaled to g dry sediment.
  - Time-series analysis used to derive production rates from isotope-labeled N2 formation.

## References
- Jensen, M. M. et al. Intensive nitrogen loss over the Omani Shelf due to anammox coupled with dissimilatory nitrite reduction to ammonium. ISME J. 5, 1660-1670 (2011).
- Nielsen, L. P. Denitrification in sediment determined from nitrogen isotope pairing. FEMS Microbiol. Ecol. 86, 357-362 (1992).
- Smart, R. M. & Barko, J. W. Laboratory culture of submersed freshwater macrophytes on natural sediments. Aquat. Bot. 21, 251-263 (1985).
- Thamdrup, B. & Dalsgaard, T. The fate of ammonium in anoxic manganese oxide-rich marine sediment. Geochim. Cosmochim. Acta 64, 4157-4164 (2000).
- Thamdrup, B. & Dalsgaard, T. Production of N2 through anaerobic ammonium oxidation coupled to nitrate reduction in marine sediments. Appl. Environ. Microbiol. 68, 1312-1318 (2002).