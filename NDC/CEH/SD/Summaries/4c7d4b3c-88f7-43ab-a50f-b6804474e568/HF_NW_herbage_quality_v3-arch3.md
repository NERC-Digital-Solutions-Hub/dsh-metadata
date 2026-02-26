# Details of data structure to HF_NW_herbage_quality.csv

- This document is a supplement to the supporting documentation for data series detailed in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Focuses on the data structure for HF_NW_herbage_quality.csv, a dataset of herbage quality.

## Overview and dataset scope

- Contains 13 columns and 96 rows.
- Dataset from grassland fertiliser trials conducted in 2016 at:
  - Henfaes Research Station (Bangor University)
  - North Wyke Research Station (Rothamsted Research)
- Henfaes samples were pre-dried and sent to Sciantec Analytical (Stockbridge Technology Centre, UK).
- North Wyke samples were fresh and sent to Trouw Nutrition GB (Blenheim House, Ashbourne, UK).
- Analyses performed using near-infrared spectrometry (NIR).

## Measured variables and units

- Date: Date of grass cut.
- Site: HF | NW (HF = Henfaes, NW = North Wyke) — location of trial.
- N_app: 1 | 2 | 3 denotes fertiliser application; 1st & 2nd applications at 90 kg ha-1, 3rd application at 60 kg ha-1.
- Block: 1 | 2 | 3 | 4 (blocking factor of randomized block design).
- Plot: 1 - 16 (plot harvested; plot size 2 × 6 m).
- Treatment: AN | U | IU | C (N fertiliser type; AN = ammonium nitrate, U = urea, IU = inhibited urea (agrotain), C = 0N control).
- Dry_matter: g kg-1 (dry matter content).
- ADF: g kg-1 (Acid Detergent Fibre; measures lignin, cellulose, lignified N).
- Ash: g kg-1 (Total mineral content).
- Crude_Protein: g kg-1 (Protein content).
- ME: MJ kg-1 (Metabolisable energy).
- NDF: Neutral Detergent Fibre (cellulose, lignin, hemi-cellulose). Unit as listed in dataset (document shows MJ kg-1, though typical NDF unit is g kg-1).
- D: Digestibility metric, % (D = ME / 0.16).

## Calculation used in the dataset

- Digestibility (D) is calculated as D = ME / 0.16.

## Data provenance and processing

- Data originate from field trials and are processed for reporting.
- Samples and analytical workflow indicate separation by site (Henfaes vs. North Wyke) and by sample type (pre-dried vs. fresh) prior to laboratory analysis.

## Purpose for monitoring and governance context

- The dataset provides measurable indicators of herbage quality relevant to evaluating fertiliser treatments and management practices.
- Structured with clear metadata (date, site, plot, block, treatment) to support monitoring, comparison across sites, and communication of findings.
- Data structure supports transparency and potential data sharing, in line with monitoring framework aims (data provenance, metadata, and clear presentation of results).