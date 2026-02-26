# DOMAINE_Tier2_growthresponse_nutrients.csv

## Overview
- Purpose: Bioassay experiments to investigate the growth response of river phytoplankton to different inorganic and organic nutrient additions and to compare these responses with in situ nutrient concentrations, aiming to identify water-chemistry drivers of organic nutrient growth responses.
- Data products: Calculated growth responses to nutrient additions, expressed as natural log response ratios (for inorganic N/P, organic N/P, and their combinations). Includes primary growth metrics and derived averages.
- Dataset format and accessibility: CSV file named DOMAINE_Tier2_growthresponse_nutrients.csv; missing values denoted as NA.
- Experimental design: 12 nutrient treatments (control, inorganic N only, inorganic P only, inorganic N and P, four organic N additions, four organic P additions) applied in triplicate to assess growth responses.
- Linking data: Growth response metrics paired with corresponding background water chemistry data collected concurrently at each site.

## Spatial and Temporal Coverage
- Temporal scope: 01 September 2017 to 31 October 2017; one sampling date per site.
- Spatial scope: Multiple sampling sites across UK rivers (site names include Ashop, Black Burn, Brocky Burn, Coln, Cottage Hill, Deepford Brook, Dickler, Dove, East Dart, Enbourne, Frome, Goredale Beck, Lambourne, N. Teign, Newby Beck, Piddle, Pow Beck, Sherbourne, Tarn Beck, Taw, Tippets Brook, Upper Chew, Windrush, Yeo; coordinates provided in OSGB 1936).
- Spatial references: Site coordinates (Northings/Eastings and National Grid references) included in Table 2; coordinate reference system is OSGB 1936.

## Methods
- Bioassay preparation: Raw water collected, kept at 4°C, transported within 48 hours, acclimated to 20°C; samples filtered through 100 µm to remove zooplankton/large detritus.
- Incubation: 12 nutrient treatments in triplicate, at approximately Redfield ratios (N: ~90 µmol L⁻¹; P: ~6 µmol L⁻¹) with 14-day incubations at 20°C under 18 h light / 6 h dark cycle.
- Growth measurement: Chlorophyll a extracted from filters after incubation and measured spectrophotometrically; growth response calculated as natural log of treatment concentration relative to the appropriate control, following Elser et al. (2007).
- Water-chemistry analyses: Inorganic nutrients analyzed with a Skalar autoanalyzer after persulphate digestion for total and dissolved N/P; DIN and SRP measured on filtered samples; DON and DOP inferred by difference (TDN-DIN, TDP-SRP).
- Quality control: Missing values represented as NA.

## Variables and Data Structure
- Growth-response variables (natural log response ratio):
  - RP: inorganic phosphate (sodium phosphate)
  - RN: inorganic nitrate/nitrogen (ammonium nitrate)
  - RNP: inorganic N and P
  - RON1–RON4: growth responses to organic N compounds (urea, glycine, glutamic acid, acetyl glucosamine)
  - ROP1–ROP4: growth responses to organic P compounds (glucose-6-phosphate, phytic acid, methylumbelliferyl-phosphate, methylphosphonate)
  - RONav: average growth response for all organic N compounds
  - ROPav: average growth response for all organic P compounds
- Water-chemistry variables (concentrations in mg N/L or mg P/L as specified):
  - TON..mg.N.l.1.; Ammonia..mg.N.l.1.; DON..mg.N.l.1.; TN..mg.N.l.1.
  - SRP..mg.P.l.1.; DOP..mg.P.l.1.; TP..mg.P.l.1.; DOC..mg.C.l.1.; DIN.mg.N.L.1
  - DONTNratio: ratio of DON to TN (0–1)
  - DOPTPratio: ratio of DOP to TP (0–1)
- Data structure notes:
  - Each row corresponds to a site replicate (site, rep, date) with associated growth-response and water-chemistry measurements.
  - Units for growth responses are natural log response ratios; nutrient concentrations are in mg N/L or mg P/L as indicated.
- Documentation references: Methods tied to Mackay et al. (unpublished), Maberly et al. (2002), Elser et al. (2007), Ritchie (2008), Talling (1974), and Yates et al. (2019, 2022).

## Data Quality and Governance
- Metadata and quality: Missing values are denoted as NA; methods and references provided to support reproducibility.
- Governance considerations for framework authors: Data are tied to explicit metadata fields (site, date, treatments, replicates, and measured variables) and include both growth responses and in situ chemistry, enabling assessment of nutrient limitation and drivers of organic nutrient uptake. Sharing of underlying data is noted as a possible governance barrier in some contexts, though not explicitly restricted here.
- Reproducibility: Clear description of experimental design, incubation conditions, analytical methods, and data processing (natural log response ratios) to support independent verification and integration into monitoring frameworks.