# DOMAINE_Tier2_growthresponse_nutrients.csv

## Overview
- A CSV dataset from bioassay experiments examining how river phytoplankton growth responds to inorganic and organic nutrient additions, compared with in situ nutrient concentrations.
- Contains calculated growth responses (natural log response ratios) to various nutrient additions, derived from incubation experiments and concurrent water chemistry data.

## Spatial and Temporal Coverage
- Spatial: 24 sampling sites across UK rivers (e.g., Ashop, Black Burn, Brocky Burn, Coln, Cottage Hill, Deepford Brook, etc.).
- Coordinate reference system: OSGB 1936 (British National Grid); coordinates provided as Eastings/Northings and NGR codes.
- Temporal: 01 September 2017 to 31 October 2017; one sampling date per site.

## Data Structure and Key Variables
- File format: CSV named DOMAINE_Tier2_growthresponse_nutrients.csv.
- Core growth-response variables (natural log response ratio):
  - RP, RN, RNP
  - RON1, RON2, RON3, RON4
  - ROP1, ROP2, ROP3, ROP4
  - RONav, ROPav (averages for all dissolved organic N/P compounds)
- Experimental metadata:
  - siteinfo (site name)
  - rep (replicate number)
  - date (incubation start date)
- Water chemistry variables (nutrients and related metrics):
  - TON..mg.N.l.1., Ammonia..mg.N.l.1., DON..mg.N.l.1., TN..mg.N.l.1.
  - SRP..mg.P.l.1., DOP..mg.P.l.1., TP..mg.P.l.1., DIN.mg.N.L.1
  - DOC..mg.C.l.1., DONTNratio (DON/TP ratio), DOPTPratio (DOP/TP ratio)
- Additional notes:
  - Units for growth responses are natural log response ratios.
  - Missing values are denoted as NA.

## Sampling and Analytical Methods
- Experimental design:
  - 12 nutrient treatments (control, inorganic N, inorganic P, inorganic N+P, plus four organic N additions and four organic P additions) applied to 35 mL samples in triplicate, following Redfield ratios.
  - 14-day incubation at 20°C with 18h light/6h dark cycle; chlorophyll a measured post-incubation to quantify growth response.
- Water chemistry methods:
  - Inorganic nutrients measured with a Skalar autoanalyzer after digestion of samples; dissolved inorganic N (DIN) measured on filtered samples.
  - DON and DOP calculated by difference (TDN - DIN, TDP - SRP); quality control notes specify NA for missing values.

## Data Quality and Limitations
- Quality control: missing values are denoted NA.
- Data are from a single sampling date per site (temporal resolution limited to the Sep–Oct 2017 window).
- Experimental data are derived from controlled incubations; in situ relevance depends on context and alignment with ambient conditions.
- Data standardization and integration considerations:
  - Spatial data in OSGB 1936; ensure appropriate reprojection if combining with other CRS.
  - Multiple nutrient treatments create a rich but complex matrix for GIS analysis; careful data shaping needed for per-site summaries or spatial comparisons.

## Potential GIS Applications
- Map spatial patterns of growth responses (e.g., organic N vs organic P) across river sites.
- Link growth-response metrics to site-level water chemistry, land-use attributes, or nutrient loading datasets.
- Create thematic maps (e.g., choropleth or graduated symbols) of key responses such as RNP, RONav, and ROPav.
- Integrate with other DOMAINE datasets to explore drivers of phytoplankton responses along nutrient gradients.
- Support policy and management discussions by visualizing spatial variation in phytoplankton nutrient limitation indicators.

## References
- Elser et al. (2007); Maberly et al. (2002); Mackay et al. (2020); Ritchie (2008); Talling (1974); Yates et al. (2019, 2022).