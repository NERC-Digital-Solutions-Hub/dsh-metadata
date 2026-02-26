# DOMAINE_Tier2_growthresponse_nutrients.csv

## Overview
- Dataset from bioassay experiments assessing growth responses of river phytoplankton to inorganic and organic nutrient additions, compared with in situ nutrient concentrations.
- Purpose: identify water-chemistry drivers of organic-nutrient growth responses.
- Includes calculated growth responses (natural log response ratios) to various nutrient additions derived from incubations and concurrent background nutrient data.

## Data description

- File format: CSV
- Spatial coverage: multiple sampling sites (e.g., Ashop, Black Burn, Brocky Burn, Coln, Cottage Hill, Deepford Brook, Frome, Yeo, and others) across UK rivers; coordinates provided in OSGB 1936 with Northings/Eastings and grid references.
- Temporal coverage: 01 September 2017 to 31 October 2017; one sampling date per site.
- Collection and derivation:
  - Raw water collected at each site, filtered (100 µm to remove zooplankton/large detritus), acclimatised, and subjected to 12 nutrient treatments in triplicate (control, inorganic N only, inorganic P only, inorganic N+P, plus four organic N additions and four organic P additions).
  - Incubations: 14 days at 20°C with 18 h light/6 h dark; phytoplankton growth assessed via chlorophyll a after incubation.
  - Growth response calculated as the natural log response ratio of treatment growth relative to the relevant control.
  - Water chemistry analyzed using Skalar autoanalyzer after persulfate digestion; inorganic/organic N and P fractions derived (e.g., DIN, SRP, DON, DOP) by measurement and difference calculations.
- Quality control: missing values denoted NA.

## Variables and units

- Site and replicate info:
  - siteinfo: sampling site name
  - rep: replicate number (integer)
  - date: incubation start date (dd/mm/yyyy)
- Growth response variables (natural log response ratio, LN RR):
  - RP: growth response to sodium phosphate
  - RN: growth response to ammonium nitrate
  - RNP: growth response to sodium phosphate and ammonium nitrate
  - RON1: growth response to urea
  - RON2: growth response to glycine
  - RON3: growth response to glutamic acid
  - RON4: growth response to acetyl glucosamine
  - ROP1: growth response to glucose-6-phosphate
  - ROP2: growth response to phytic acid
  - ROP3: growth response to methylumbelliferyl-phosphate
  - ROP4: growth response to methylphosphonate
- Water chemistry (concentrations in mg N or P L-1 where noted):
  - TON..mg.N.l.1.; ammonia..mg.N.l.1.; DON..mg.N.l.1.; TN..mg.N.l.1.
  - SRP..mg.P.l.1.; DOP..mg.P.l.1.; TP..mg.P.l.1.; DOC..mg.C.l.1.
  - DIN.mg.N.L.1
  - DONTNratio: ratio of DON to TN (0 to 1)
  - DOPTPratio: ratio of DOP to TP (0 to 1)
- Averages:
  - RONav: average growth response for all dissolved organic N compounds
  - ROPav: average growth response for all dissolved organic P compounds
- Units: all growth-response variables are natural log response ratios.

## Methods and processing

- Experimental design and references:
  - Based on Mackay et al. and Maberly et al.; nutrient-growth bioassays conducted as described.
- Incubation and measurements:
  - Raw water collected and processed as described; chlorophyll a quantified spectrophotometrically after extraction, to derive growth responses.
- Data processing:
  - Growth response calculated as ln(treatment growth) minus ln(control growth) for each nutrient treatment.
  - DON and DOP derived by difference between TDN and DIN, and TDP and SRP, respectively.
- Analytical methods:
  - Inorganic nutrients measured with Skalar autoanalyzer after persulfate digestion of unfiltered and pre-leached filtered samples.
  - DON and DOP inferred by subtraction from total N/P pools.

## Spatial and temporal details

- Sites: diverse river sites listed (e.g., Ashop, Black Burn, Brocky Burn, Coln, Cottage Hill, Deepford Brook, Frome, Yeo, and others).
- Coordinate reference: OSGB 1936; includes precise northings/eastings and grid references.

## Usage notes and caveats

- Outputs are suitable for exploring phytoplankton responses to specific inorganic vs. organic nutrient sources and their relation to water-chemistry parameters.
- Incubation conditions (14 days at 20°C with specified light regime) are controlled and may differ from in situ conditions; results reflect experimental growth under those conditions.
- Data include multiple replicates and a comprehensive suite of organic and inorganic nutrient treatments, enabling analysis of nutrient limitation patterns.
- Missing values are indicated as NA.

## References

- Elser et al. (2007)
- Maberly et al. (2002)
- Mackay et al. (2020)
- Ritchie (2008)
- Talling (1974)
- Yates et al. (2019)
- Yates et al. (2022)