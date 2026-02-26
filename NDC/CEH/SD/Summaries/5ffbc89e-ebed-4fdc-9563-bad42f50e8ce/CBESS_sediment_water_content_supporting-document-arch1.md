# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment water content in saltmarsh and mudflat habitats

## Overview
- Dataset measuring percentage water content in surface sediment (top 2 mm) for saltmarsh and mudflat habitats.
- Measurements taken as part of the CBESS field campaign in winter and summer 2013.
- Each quadrat yields five replicates; sampling conducted across multiple sites with 22 quadrats per site.
- Sampling staff: Jack Maunder.

## Study Sites and Habitat Context
- Essex region: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay region: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat differences:
  - Saltmarsh sites represent two contrasting soil types: clay soils (Essex) and sandy soils (Morecambe Bay).
  - Inundation frequency, creek structure, and dominant vegetation differ between Essex and Morecambe Bay saltmarshes.
  - Mudflat sites: Essex dominated by cohesive clays, mud, and silt; Morecambe Bay mudflats dominated by coarse, mobile sediments.

## Data Collection and Processing
- Sampling design:
  - Randomly allocated quadrats: 22 per mudflat and 22 per saltmarsh site.
  - Observations collected in winter (W) and summer (S) of 2013.
  - No planned repetition beyond the two-season campaign.
- Field and lab procedures:
  - Surface sediment sampled with a contact corer; flash-frozen with liquid nitrogen; stored below -80°C.
  - Wet and dry weights measured after drying to calculate percent water content.
  - Quadrats were sampled to four spatial scales (A–D) using R to specify scales: A = 1 quadrat; B = 3 quadrats at 1 m to 10 m; C = 6 quadrats at 10 m to 100 m; D = 12 quadrats at 100 m to 1000 m (site maximums).
  - Calibration and scale application followed laboratory protocols.
- Data handling:
  - Readings from scales entered into spreadsheets.
  - File format for final data: comma-separated values (.csv).

## Data Variables and Structure
- Core observational variable: Percentage Water Content (average per quadrat).
- Supporting statistics: StDev (standard deviation of percentage water content values for quadrats).
- Key fields (per observation): Season (Winter or Summer), Location (Morecambe or Essex), Site (CS, WS, WP; AH, FW, TM), Habitat (Mudflat or Saltmarsh), Quadrat Number (1–22), Scale (A–D), Percentage Water Content, StDev, and Other information (e.g., NA for missing data).
- Data organization emphasizes cross-site comparability and explicit documentation of spatial scale and habitat context.

## Quality Assurance and Provenance
- Sampling and analysis followed standardized CBESS field campaign protocols.
- Data entry efforts captured scale readings; NA indicates missing data due to inaccessibility of a quadrat.
- Dataset includes detailed site coordinates and descriptive context to support reproducibility and cross-study synthesis.

## Potential Analyses and Use Cases for Analysts
- Compare water content across habitat types (saltmarsh vs. mudflat) and sediment types (clay vs. sand) within and between Essex and Morecambe Bay.
- Assess seasonal variation (winter vs. summer 2013) in surface sediment moisture.
- Investigate relationships between water content and environmental drivers (inundation frequency, vegetation type, creek structure).
- Develop correlations or predictive models of sediment moisture using spatial scale (A–D) and coordinates.
- Integrate with other CBESS datasets to evaluate ecosystem services related to sediment moisture and biodiversity.
- Consider data limitations: two-season snapshot in 2013, 22 quadrats per site (not a large temporal depth), and NA entries for some missing data.