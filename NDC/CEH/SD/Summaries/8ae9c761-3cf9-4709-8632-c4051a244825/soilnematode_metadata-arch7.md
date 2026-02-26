# Soil nematode communities from peri urban watersheds

## Overview
- Study of soil nematode communities within a peri-urban watershed in Ningbo, China, with the goal of producing data suitable for GIS-based visualization and analysis.
- Data designed to be integrated with other CZO catchment datasets via a common Sample_ID.

## Study design and sampling
- Sampling conducted across a watershed in Ningbo’s peri-urban area during four periods: April 9–12, 2017; July 15–18, 2017; October 14–17, 2017; January 11–14, 2018.
- At each site, two land uses were sampled: farmland and forest.
- At each site: 250 g of soil collected as five randomly distributed cores.
- Samples stored at 4 °C before shipment to the UK and then kept at 8 °C in quarantine per policy.

## Laboratory methods
- Nematodes extracted from soil using a density centrifugation method.
- DNA extraction performed on freeze-dried nematodes.
- Nematode community structure assessed by directed T-RFLP with Nem_SSU_F74 and Nem_18S_R primers.
- PCR and restriction enzyme digestion performed using Ple I and BtscI, followed by capillary sequencing (ABI 3730).
- T-RF peaks identified with Genemapper; baseline fluorescence set at 50 fluorescence units.
- Relative fluorescence per peak calculated; peaks < 1% of total fluorescence discarded.
- Data underwent a Hellinger transformation.

## Data structure and units
- Data file: CZOperiurban_watershed_Nematodedata.csv.
- Key fields:
  - Sample_ID: CZO watershed sample ID (links to other CZO datasets).
  - Season: Season when samples were collected.
  - Peak_...: Hellinger-transformed relative fluorescence for each T-RF peak (e.g., Peak_54.86 corresponds to peak 54.86).
- The dataset provides a per-sample profile of nematode community structure via T-RFLP peaks, enabling comparative GIS analyses across space and time.

## GIS visualization and usage implications
- Enables mapping of sampling locations and land-use types alongside nematode community indicators (T-RF peak abundances).
- Facilitates temporal comparisons (across the four collection periods) and spatial analyses within the peri-urban watershed.
- Suitable for integration with environmental layers and other CZO catchment data using the common Sample_ID.

## Data quality and notes
- Data quality steps include removal of low-abundance peaks (<1% of total fluorescence) and data transformation (Hellinger).
- Sampling and preservation protocols follow standard biogeochemical and biosecurity practices, with explicit storage/shipping conditions.
- References for methods provided (Hallmann & Viaene 2013; Donn et al. 2012) support the extraction, T-RFLP, and analysis approaches.

## References
- Hallmann and Viaene (2013). Nematode extraction. EPPO Bulletin.
- Donn, S., Neilson, R., Griffiths, B.S., Daniell, T.J (2012). A novel molecular approach for rapid assessment of soil nematode assemblages. Methods in Ecology and Evolution.