# Digestate_HF_and_NW_N2O_cum.csv

## Overview
- Data supplement from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW), Rothamsted Research.
- Contains 40 rows of plot-level N2O flux data across two sites for multiple treatments.
- Focus on cumulative N2O flux values derived from chamber measurements, with quality-filtered variants.

## Data schema and fields
- Compact schema of seven fields capturing spatial identifiers, treatment, sampling, and three N2O-derived metrics.
- Site: HF or NW.
- Treatment: C (control), D (digestate), AD (acidified digestate), DNI (digestate with nitrification inhibitor DMPP), ADNI (acidified digestate with DMPP).
- Block: 1–5, representing the randomized block design.
- Plot: plot identifier; note some plots were used for monthly samplings at 150 kg N ha-1 (specific plots listed in the dataset notes).
- Date: measurement date.
- N2O_qa1: all N2O flux data for each chamber/plot over the experimental period (used to derive cumulative values).
- N2O_qa2: cumulative N2O flux after removing data with R2 < 0.6 (R2 threshold adjustable).
- N2O_qa3: cumulative N2O flux after removing data with R2 < 0.6 and replacing all negative Flux_N2O values with zero (R2 threshold adjustable).

## Spatial layout and plot sizes
- HF: plot harvest areas vary by treatment, with 1.2 m x 6.5 m harvest areas for nitrogen addition rates and 1.2 m x 14 m for C, D, AD, DNI, ADNI.
- NW: plot harvest areas are 2 m x 4.5 m for nitrogen addition rates and 2 m x 9 m for C, D, AD, DNI, ADNI.

## Data quality and processing
- qa2 and qa3 include quality-filtering steps:
  - Remove cumulative data where R2 < 0.6; threshold is adjustable.
  - In qa3, additionally replace negative flux values with zero.
- Documented to aid consistency when aggregating or comparing across plots and treatments.

## Usage notes for GIS applications
- Ideal for map-based visualization of spatial patterns in N2O flux by site and treatment.
- Can be joined with plot-level spatial layers (plot boundaries, blocks, sampling layouts) to analyze spatial trends.
- Compare cumulative flux across treatments and sites; select whether to use qa2 or qa3 depending on data quality needs.
- Date field enables time-aware mapping or temporal analyses of flux trends.

## Provenance and scope
- Part of supporting documentation for CINAg experiments; supplement to digestate experiment data.
- Two-site study with 40 rows of plot-level N2O data from the 2017 digestate wheat trial.