# DOMAINE_Tier2_growthresponse_nutrients.csv

## Overview
- Bioassay data assessing river phytoplankton growth responses to inorganic and organic nutrient additions in relation to in situ nutrient concentrations.
- Purpose: identify water-chemistry drivers of organic nutrient growth responses and explore correlations between ambient nutrient status and nutrient-induced growth.

## Data scope and structure

- File format: CSV
- File name: DOMAINE_Tier2_growthresponse_nutrients.csv
- Data provenance: Growth responses calculated from controlled incubations with multiple nutrient treatments; background water-chemistry data collected concurrently.
- Growth metrics: Natural log response ratio (lnRR) for various nutrient treatments.

## Variables and measurements (Table 1 description)

- Site and replicate information
  - siteinfo: sampling site name
  - rep: replicate number (integer)
  - date: incubation start date (dd/mm/yyyy)

- Growth response variables (lnRR)
  - RP: growth response to sodium phosphate
  - RN: growth response to ammonium nitrate
  - RNP: growth response to sodium phosphate and ammonium nitrate
  - RON1–RON4: growth responses to organic N additions (1–4 compounds)
  - ROP1–ROP4: growth responses to organic P additions (1–4 compounds)
  - TON..mg.N.l.1.: total oxidised nitrogen concentration (mg N L-1)
  - Ammonia..mg.N.l.1.: ammonia concentration (mg N L-1)
  - DON.. mg.N.l.1.: dissolved organic nitrogen (mg N L-1)
  - TN..mg.N.l.1.: total nitrogen (mg N L-1)
  - SRP..mg.P.l.1.: soluble reactive phosphorus (mg P L-1)
  - DOP..mg.P.l.1.: dissolved organic phosphorus (mg P L-1)
  - TP..mg.P.l.1.: total phosphorus (mg P L-1)
  - DOC..mg.C.l.1.: dissolved organic carbon (mg C L-1)
  - DIN.mg.N.L.1.: dissolved inorganic nitrogen (mg N L-1)
  - DONTNratio: ratio of DON to total nitrogen (0–1)
  - DOPTPratio: ratio of DOP to total phosphorus (0–1)
  - RONav: average growth response for all dissolved organic N compounds
  - ROPav: average growth response for all dissolved organic P compounds
- Methods for growth measurement
  - Growth assessed via chlorophyll a change after 14 days, using spectrophotometric methods (Talling 1974; Ritchie 2008)
  - Incubations: 14 days at 20°C, light 80–120 μmol m−2 s−1, 18 h light/6 h dark
  - Treatments (12 total, in triplicate): control, inorganic N only, inorganic P only, inorganic N+P, four organic N additions, four organic P additions
- In situ water chemistry methods
  - Analyzed with Skalar ++ autoanalyzer after persulphate digestion
  - Measured TN, TP (unfiltered) and TDN, TDP (pre-leached filtered samples)
  - DIN, NH3, SRP, DON, DOP derived by difference where appropriate

## Spatial and temporal coverage

- Sites: multiple UK river sites (e.g., Ashop, Black Burn, Brocky Burn, Coln, Cottage Hill, Deepford Brook, etc.)
- Spatial coordinates: provided as Northings, Eastings, and NGR; coordinate reference system = OSGB 1936
- Temporal coverage: one sampling date per site, 01 September 2017 to 31 October 2017

## Collection, processing, and quality control

- Sample collection: raw water collected on-site, kept at 4°C, transported to lab within 48 hours
- Preparation: filtration to 100 μm to remove zooplankton, 35 mL aliquots used for 12 nutrient treatments
- Replication: triplicate treatments
- Data quality: missing values denoted as NA

## Methods and references

- Experimental design: nutrient additions following Mackay et al. (unpublished) and aligned with Maberly et al. (2002) and Elser et al. (2007) protocols
- Growth measurement: chlorophyll a quantified spectrophotometrically per Talling (1974) and Ritchie (2008)
- Water-chemistry methods: detailed in Yates et al. (2019, 2022)
- Key references for interpretation of growth responses and nutrient analyses:
  - Elser et al. 2007; Maberly et al. 2002; Mackay et al. 2020; Ritchie 2008; Talling 1974
  - Yates et al. 2019, 2022

## Potential analytical applications for the data

- Identify correlations between in situ nutrient status and growth responses to inorganic vs organic nutrients
- Develop predictive models linking ambient TON, TN, DIN, SRP, DOP, etc., with observed lnRRs for different nutrient additions
- Compare growth responses to organic N versus organic P compounds across sites and conditions
- Assess spatial and temporal patterns in nutrient-driven phytoplankton growth within river systems

## Summary of dataset purpose

- Enables examination of how river phytoplankton growth responds to specific nutrient amendments in the context of ambient water chemistry, with a robust, replicated bioassay framework across multiple sites and a well-documented chemical analysis protocol.