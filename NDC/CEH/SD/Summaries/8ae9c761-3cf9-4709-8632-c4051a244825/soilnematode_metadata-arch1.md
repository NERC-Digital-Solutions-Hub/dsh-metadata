# Soil nematode communities from peri urban watersheds

## Overview
- Study of soil nematode communities across a peri-urban watershed in Ningbo, China.
- Sampling conducted in four periods: April 2017, July 2017, October 2017, January 2018.
- For each site, two land uses were sampled (farmland and forest); 250 g of soil collected as five random cores per site.
- Samples stored at 4 °C before shipping to the UK and kept in quarantine at 8 °C per biosecurity policy.
- Data are organized to be compatible with other CZO catchment datasets.

## Experimental Design
- At each watershed site, two land-use types (farmland and forest) were sampled.
- Each sampling event used 250 g of soil collected from five random cores across the site.

## Collection Methods and Laboratory Instrumentation
- Nematodes extracted from soil using a density centrifugation method:
  - 100 g soil in 250 mL bottles with 150 mL water; shake and centrifuge at 1800 g for 4 minutes.
  - Add 150 mL MgSO4 (final density 1.18); shake and centrifuge again at 1800 g for 4 minutes.
  - Pass supernatant through a 20 µm sieve; wash into a clean tube; freeze-dry.
  - Re-suspend in 2 mL sterile ddH2O; extract nematode DNA with PureLink Genomic DNA Mini Kit.
- Nematode community structure assessed by directed T-RFLP:
  - Primers: Nem_SSU_F74 and FAM-labeled Nem_18S_R.
  - PCR: 95 °C 3 min; 35 cycles (94 °C 30 s, 55 °C 30 s, 68 °C 1 min); final extension at 68 °C for 10 min.
  - Restriction digests: Ple I and BtscI, with specified buffers, temperatures, and times.
  - Digests diluted, mixed with formamide and LIZ 1200 marker, then sequenced on an ABI 3730 capillary sequencer.
  - T-RF peaks identified in Genemapper; baseline fluorescence set at 50 fluorescence units.
  - Relative fluorescence for each peak calculated; peaks <1% of total fluorescence removed.
  - Data transformed using the Hellinger transformation.

## Data Structure & Values
- File: CZOperiurban_watershed_Nematodedata.csv
- Variables:
  - Sample_ID: CZO watershed sample ID; matches identifiers in other CZO datasets.
  - Season: season when the sample was collected.
  - Peak_<number>: Hellinger-transformed relative fluorescence for each T-RF peak (e.g., Peak_54.86 corresponds to peak 54.86).

## Data Processing & Reuse
- Data are Hellinger-transformed for downstream statistical analyses.
- Dataset is prepared to be discoverable and usable, with metadata; datasets created may be uploaded to portals for integration with other CZO data.

## References
- Hallmann and Viaene (2013) Nematode extraction. EPPO Bulletin, 43: 471-495.
- Donn, S., Neilson, R., Griffiths, B.S., Daniell, T.J (2012) A novel molecular approach for rapid assessment of soil nematode assemblages - variation, validation and potential applications. Methods in Ecology and Evolution, 3:12-23.