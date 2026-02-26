# General information: This dataset contains results from slurry incubations with 15N-labelled substrates.

## Overview
- Contains results from slurry incubations using 15N-labelled substrates to study nitrogen transformations.
- Slurries prepared as:
  - Anoxic: 3 mL total volume in gas-tight vials (1 mL sediment, 1 mL synthetic river water, N2 headspace).
  - Oxic: 12 mL total volume in gas-tight vials (2.5 mL sediment, 3 mL synthetic river water, air headspace).
- Sediments collected August 2013; Mass Spectrometry analysis performed September 2013.
- Amendments included 14N (natural abundance) and 15N-labelled substrates; nitrate amendments targeted at 100 µM (clay), 300 µM (sand), and 500 µM (chalk); ammonium amendments targeted at 500 µM across all sediments.
- Anoxic slurries pre-incubated overnight to remove ambient 14N-nitrate.
- Incubations conducted in the dark at room temperature; results are poten­tials rather than in situ rates.
- Outputs organized as time-series, reference, and control samples; outputs may be promoted or iterated based on feedback.

## Experimental design
- Slurry types and volumes:
  - Anoxic: 3 mL vials with 1 mL sediment + 1 mL synthetic river water.
  - Oxic: 12 mL vials with 2.5 mL sediment + 3 mL synthetic river water.
- Substrates and tracers:
  - 14N and 15N-labelled substrates; 15N tracers ~98 atom % 15N.
  - N-amendments injected as 100 µL per vial.
- Incubation protocol:
  - Reference samples (no 15N substrate), control samples (inactivated by zinc chloride prior to 15N addition), and time-series samples (inactivated at set times after 15N addition).
- Time-series sampling (oxic slurries) includes: 0, 0.5, 1, 2, 3, and 6 hours post 15N addition.
- Replication:
  - Replicates: five discrete sediment samples per river (Clay, Sand, Chalk sub-sites), representing different sites within the Hampshire Avon catchment.
- Measurements:
  - 15N-labelled NOx and N2 production measured by mass spectrometry.
  - Ammonium and NOx concentrations measured by automated colorimetry with appropriate standards and detection limits.
- Output types:
  - N2 production rates (P29, P30) under various amendments (e.g., 15N-nitrate, 15N-ammonium).
  - Total anammox activity (Atotal) and its share (ra) of total denitrification (Dtotal).
  - Proportions of 15N-label in NH4+, NOx, and N2 pools (FN-NH4+, FN-NOx, FN-N2) used in a mixing model.
  - Aromatically structured time-series data for 15NOx (T0–T5) and related Oxic/Oxidation-specific measurements (Oxicp15N*, O2 concentration, etc.).

## Measurements and calculations
- Key metrics:
  - P29-15A, P30-15A: 29N2 and 30N2 production rates after 15N-labelled ammonium in anoxic slurry (6 h comparison to control).
  - P29-15A14N, P30-15A14N: Rates with 15N ammonium and 14N-nitrate.
  - P29-15N, P30-15N: Rates after 15N-nitrate addition (time-series slopes).
  - Atotal: Total anammox activity (nmol N2 g-1 dry sediment h-1) calculated per Thamdrup & Dalsgaard (2002).
  - ra: Proportion of N2 production from anammox (percent of total denitrification).
- Calculations and methods:
  - Headspace N2 isotopologues (29, 30) used to infer N2 production; equations normalize to total N2 pool and convert to nmol per g sediment.
  - Aqueous N2 calculated from headspace data via the Bunsen solubility coefficient and vial total nmoles.
  - Rates derived from time-series trends (linear fits) of N2 isotopologue concentrations vs. time.
- Detection limits:
  - LODs defined for 29N2, 30N2, and 15N-N2 (specific approximate values provided in the description).
- Additional measurements:
  - Ammonium Ref and NOx Ref: reference concentrations in oxic slurries (colorimetric methods with specified LODs and precision).
  - 15NOxT0–T5: 15N-labelled NOx concentrations in oxic time-series samples.
  - FN-NH4+, FN-NOx, FN-N2: isotopic fractions used in mixing models; included only when 15N tracers are detectable.
  - Oxicp15N-T0...T4 and Oxicp15Nrpt-T0...T5: measurements of 15N-labelled N2 under different conditions (including replicated runs to test nitrification-N2 relationships and allylthiourea inhibition effects).
  - Oxicp15NATU-T0...T5: measurements with allylthiourea to inhibit nitrification in oxic series.
  - O2Conc-T0...T3: dissolved oxygen in oxic slurries at various incubation times.

## Data structure and column headers
- Data structure:
  - 42 columns and 46 rows (including headings); values marked BDL when below detection limit.
  - Time-series columns include: 15NOxT0, 15NOxT1, 15NOxT2, 15NOxT3, 15NOxT4, 15NOxT5 (nitrate+nitrite over time in oxic slurries).
- Representative column families:
  - Sample identifiers: Site, Replicate, Substrate type (Clay/Sand/Chalk), and site coordinates.
  - P29-15A, P30-15A, P29-15A14N, P30-15A14N, P29-15N, P30-15N.
  - Atotal and ra (anammox contribution) with Dtotal (denitrification) implied in calculations.
  - 15NOxT0–T5: time-series NOx concentrations in oxic slurries.
  - FN-NH4+, FN-NOx, FN-N2: isotopic fractions used in mixing models.
  - Oxicp15N pT0–pT5 and Oxicp15Nrpt pT0–pT5: N2 production after ammonium addition under various conditions (including replicates).
  - Oxicp15NATU pT0–pT5: N2 production with ammonium plus allylthiourea.
  - O2Conc-T0–T3: dissolved oxygen measurements over time.
  - AmmoniumRef and NOxRef: reference concentrations for oxic slurries.

## Site and replication details
- Sites grouped by river sub-catchment:
  - Clay (River Sem and tributaries 1–3) with defined coordinates.
  - Sand (River Nadder and Avon sub-sites 1–3) with defined coordinates.
  - Chalk (River Ebble, Wylye, and Avon sub-sites) with defined coordinates.
- Replicates:
  - Five discrete sediment samples per river replicate.

## References and methodological context
- Nielsen, L. P. 1992. Denitrification in sediment determined from nitrogen isotope pairing.
- Jensen, M. M. et al. 2011. intensive nitrogen loss over the Omani Shelf due to anammox with dissimilatory nitrite reduction to ammonium.
- Smart, R. M. & Barko, J. W. 1985. Laboratory culture methods for freshwater sediments.
- Thamdrup, B. & Dalsgaard, T. 2000, 2002. Thamdrup & Dalsgaard methods for N2 production via anammox and denitrification.

## Usage notes and data quality considerations
- Outputs are potential rates (not necessarily in situ rates) due to incubation conditions and time-point controls.
- Time-series nature of many columns requires careful alignment of time points for rate calculations.
- Data include measurements with non-detects (BDL) and require handling of detection limits in analyses.
- Multiple measurement methods (mass spectrometry, colorimetry) and controls (reference and killed-abiotic controls) enable separation of biological activities from abiotic processes.
- Data are suited for: quantifying anammox versus denitrification contributions, comparing across sediment types and river sites, and exploring nitrification-denitrification interactions under oxic vs. anoxic conditions.