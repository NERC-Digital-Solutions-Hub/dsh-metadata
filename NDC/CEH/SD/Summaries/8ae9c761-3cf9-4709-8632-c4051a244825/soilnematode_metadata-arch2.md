# Soil nematode communities from peri urban watersheds

## Overview
- A study of soil nematode communities across a peri-urban watershed in Ningbo, China, linking soil biota to land use and seasonal variation.
- Sampling conducted across four time points: April 2017, July 2017, October 2017, January 2018.
- Two land-use types sampled per watershed: farmland and forest.
- Goal aligned with environmental monitoring: produce standardized data to assess soil health via nematode community structure.

## Experimental Design
- At each site, 250 g soil collected by randomly taking 5 cores.
- Each season/site combination provides replicated sampling across land uses.

## Collection methods and laboratory instrumentation
- Nematodes extracted via density centrifugation from 100 g soil, followed by MgSO4 density separation.
- DNA extraction performed on freeze-dried nematodes using PureLink Genomic DNA Mini Kit.
- Nematode community structure determined by directed T-RFLP (terminal restriction fragment length polymorphism).
  - Primers: Nem_SSU_F74 and FAM-labeled Nem_18S_R.
  - PCR conditions: initial denaturation, 35 cycles, final extension.
  - Enzymatic digestion: Ple I and BtscI, with specified digestion/denaturation steps.
  - Capillary sequencing on ABI 3730; peaks identified with Genemapper.
- Data processing: baseline fluorescence set at 50 units; peaks <1% of total fluorescence removed; data transformed using Hellinger transformation.
- Sample metadata and peak data recorded in a CSV data file.

## Data structure and units
- File: CZOperiurban_watershed_Nematodedata.csv
- Key fields:
  - Sample_ID: CZO watershed sample ID (matches other CZO datasets).
  - Season: season of collection.
  - Peak_...: Hellinger-transformed relative fluorescence for each T-RF peak (e.g., Peak_54.86).

## Quality assurance and data handling
- Field samples kept at 4 °C prior to shipping; shipping complies with relevant import licenses.
- Samples stored at 8 °C in quarantine facilities per institutional biosecurity policy.
- Data prepared in a standardized format suitable for uploading to monitoring data portals.
- Method references used for validation and replication of protocols:
  - Hallmann and Viaene (2013) for nematode extraction.
  - Donn et al. (2012) for the T-RFLP approach.

## Outputs and potential use for monitoring
- Standardized nematode community data across time and land-use types enabling comparison and trend analysis.
- Transformed peak data (T-RFLP) used to assess community composition relative to environmental standards or policy targets.
- Datasets can be combined with other environmental datasets to enhance monitoring value (aligned with data-sharing and interoperability goals).

## Reuse and accessibility
- Data structure supports integration with other CZO datasets due to consistent sample IDs and metadata.
- References provided for methodological replication; data file name indicates availability for downstream analysis and public portals.