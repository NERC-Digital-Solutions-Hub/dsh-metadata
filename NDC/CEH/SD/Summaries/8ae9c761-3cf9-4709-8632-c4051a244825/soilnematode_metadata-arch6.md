# Soil nematode communities from peri urban watersheds

## Overview
- Study of soil nematode communities across a peri-urban watershed in Ningbo, China, examining seasonal variation and land-use effects (farmland vs forest).
- Sampling conducted over four periods: Apr 9–12, 2017; Jul 15–18, 2017; Oct 14–17, 2017; Jan 11–14, 2018.
- At each site, 250 g of soil collected via 5 random cores; samples stored at 4 °C before shipping to the UK under compliance with the Scottish import licence and stored at 8 °C in quarantine facilities.

## Experimental Design
- Each watershed included two land-use types: farmland and forest.
- Sampling protocol used 5 soil cores per site to obtain representative soil for nematode analysis.
- Aimed to enable integration with other Catchment-Scale Observatories (CZO) data via consistent Sample_IDs.

## Methods and Laboratory Procedures
- Nematode extraction: density centrifugation from 100 g soil, using MgSO4 solution (final density ~1.18) and successive centrifugation steps; material freeze-dried and re-suspended for DNA extraction.
- DNA extraction: PureLink Genomic DNA Mini Kit (ThermoFisher).
- Community structure profiling: directed T-RFLP (terminal restriction fragments) using Nem_SSU_F74 and Nem_18S_R (FAM-labeled).
- PCR conditions: 95 °C 3 min; 35 cycles of 94 °C 30 s, 55 °C 30 s, 68 °C 1 min; final extension at 68 °C 10 min.
- Restriction digest: Ple I and BtscI enzymes, with specified buffers and temperatures; products denatured and prepared with formamide and LIZ 1200 for capillary sequencing (ABI 3730).
- Data processing: T-RF peaks identified in GeneMapper; baseline fluorescence set at 50 units; relative fluorescence calculated for each peak; peaks <1% of total fluorescence removed; data transformed with Hellinger transformation.

## Data Structure, Nature, and Units
- Data file: CZOperiurban_watershed_Nematodedata.csv
- Sample_ID: CZO watershed sample identifier that can be matched to other CZO datasets.
- Season: season of sample collection.
- Peak_...: Hellinger-transformed relative fluorescence for each T-RF peak (e.g., Peak_54.86 corresponds to peak 54.86).

## Data Quality and Usability Notes
- Data are pre-processed to remove noise (peaks <1% of total fluorescence) and transformed, enabling comparative analyses of nematode community structure across samples.
- Interoperable with other CZO datasets via Sample_ID.

## Potential Data Uses (Data Support Perspective)
- Build dashboards or pivot-table style views to compare nematode community composition across seasons and land uses.
- Combine with environmental covariates or other biological datasets for cross-disciplinary insights.
- Share early prototypes with stakeholders and iteratively refine data products; promote broader data reuse.

## References
- Hallmann and Viaene (2013) on nematode extraction.
- Donn, Neilson, Griffiths, Daniell (2012) on molecular approaches for soil nematode assemblages.