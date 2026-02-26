# Soil nematode communities from peri urban watersheds

## Overview
- Objective: characterize soil nematode communities across farmland and forest in a peri-urban watershed in Ningbo, China, over four seasonal windows, using directed T-RFLP to assess community structure.
- Outcome: a structured dataset detailing nematode community signals suitable for cross-site comparison and monitoring.

## Experimental Design
- Study area: peri-urban watershed in Ningbo; two land uses (farmland and forest).
- Temporal scope: sampling during four periods (Apr 9–12, 2017; Jul 15–18, 2017; Oct 14–17, 2017; Jan 11–14, 2018).
- Sampling at each site: 250 g of soil collected via 5 random cores.
- Sample handling: soils stored at 4 °C before shipment; shipped under Scottish government import license and stored at 8 °C in quarantine per James Hutton Institute biosecurity policy.

## Collection Methods and Laboratory Instrumentation
- Nematode extraction: density centrifugation method adapted from Hallmann & Viaene (2013). Process involves processing 100 g soil with water, successive centrifugation steps, sieving, freezing, then freeze-drying.
- DNA extraction: from freeze-dried nematodes using PureLink Genomic DNA Mini Kit.
- Community analysis: directed T-RFLP method adapted from Donn et al. (2012).
  - Primers: Nem_SSU_F74 and Nem_18S_R labeled with FAM.
  - PCR conditions: 95 °C for 3 min; 35 cycles of 94 °C for 30 s, 55 °C for 30 s, 68 °C for 1 min; final extension at 68 °C for 10 min.
  - Restriction digests: PleI and BtsCI with specified buffers and temperatures; denature at 65 °C and 80 °C respectively after digestion.
  - Analysis: digests diluted 1:10, mixed with formamide and LIZ 1200, sequenced on ABI 3730 capillary sequencer.
  - Data processing: T-RF peaks identified with GeneMapper; baseline fluorescence set to 50 RFU; relative peak fluorescence calculated; peaks <1% of total removed; data transformed Hessian (Hellinger).

## Data Structure & Units
- Data file: CZOperiurban_watershed_Nematodedata.csv
- Key fields:
  - Sample_ID: matches the CZO watershed dataset identifiers.
  - Season: season of sample collection.
  - Peak_...: Hellinger-transformed relative fluorescence for each T-RF peak (e.g., Peak_54.86).

## References
- Hallmann, A. & Viaene, N. (2013). Nematode extraction method.
- Donn, S.; Neilson, R.; Griffiths, B.S.; Daniell, T.J. (2012). A molecular approach for rapid assessment of soil nematode assemblages (Methods in Ecology and Evolution).