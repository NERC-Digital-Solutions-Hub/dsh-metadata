# Digestate_HF_and_NW_NH3_v2.csv

## Overview
- Supplement to the supporting documentation for data series in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Data from the digestate wheat trial (2017) conducted at Henfaes Research Center (HF) and North Wyke (NW) with NH3 emissions measured from plots amended with different digestate treatments.
- Emissions measured using wind tunnels and acid traps; dataset comprises 8 columns and 304 rows.

## Data content and scope
- Sites: HF (Henfaes) and NW (North Wyke).
- Measurements span a 7-day period after digestate application, with site-specific time points.
- Treatments include: D (digestate), AD (acidified digestate), DNI (digestate with DMPP), ADNI (acidified digestate with DMPP).

## Columns and definitions
- Site: HF or NW.
- Midpoint_time: midpoint of the period during which NH3 was measured.
- Hours_since_digestate_app: hours since digestate application.
- Block: blocking factor in the randomized block design (values 1–4).
- Plot: experimental plot identifier.
- Treatment: D, AD, DNI, or ADNI (definitions as above).
- NH3_qa1: NH3-N emissions over the 7-day measurement period (units: kg NH3-N ha^-1).
- NH3_qa2: same as NH3_qa1, but negative NH3 fluxes replaced with 0.

## Measurement methods
- Gas traps containing phosphoric acid were used to trap NH3; NH4 is measured since NH3 converts to NH4 in acid.
- NH4 traps were changed multiple times per day on the first day at HF/NW due to expected high volatilization.
- Air was circulated from wind tunnels to the traps via two pipes positioned at the beginning and middle of the plot.
- Detection limit: 0.01 mg NH4-N L^-1.

## Experimental context
- Digestate sources: HF uses digestate from anaerobic digestion of food waste (Fre-energy, Wrexham); NW uses digestate from anaerobic digestion of food waste (Holsworthy).
- The dataset forms part of the CINAg experiments, focusing on ammonia emissions from different digestate treatments.

## Data usage notes
- NH3_qa2 applies a data-handling rule by replacing negative NH3 flux values with zero, aligning with the measurement and reporting approach.
- Structure and metadata are provided to support data discovery, interpretation, and cross-dataset integration.