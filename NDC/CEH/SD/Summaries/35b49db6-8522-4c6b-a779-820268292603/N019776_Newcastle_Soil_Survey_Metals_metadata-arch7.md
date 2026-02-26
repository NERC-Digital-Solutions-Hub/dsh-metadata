# Community antimicrobial resistance genes and concentrations of polycyclic aromatic hydrocarbons and metals in NE England soils

## Overview
- A dataset describing the relative abundance of antimicrobial resistance genes in DNA extracted from soils around Newcastle upon Tyne.
- Sampling locations were preselected based on metal concentrations and land-use to represent four treatments: low-metal/rural, low-metal/urban, high-metal/rural, high-metal/urban.
- Fieldwork conducted in June 2016 on the soil horizon less than 15 cm from the surface; samples refrigerated after collection.

## Fieldwork design
- Preselection criteria: metal concentration patterns from prior sampling and land-use classification.
- Four treatment categories to capture variability in metal exposure and urbanization.
- Sampling depth: upper soil horizon (<15 cm).
- Sample handling: immediate refrigeration for preservation prior to analysis.

## Analytical methods
- Soil pH: ISO 10390:2005; slurry at 1:5 (soil:deionised water), mixed 1 h, equilibrated overnight, measured with a Jenway 3020 pH meter.
- Metal concentrations:
  - Total metals: determined by ICP-MS after aqua regia digestion (1 g soil in 1:3 HNO3:HCl).
  - Bioavailable metals:
    - Step 1 (exchangeable fraction): 0.11 M acetic acid extraction, 40 mL acid with 1 g soil for 16 h, centrifuged, extracts stored at 4°C for ICP-MS.
    - Step 2 (residual fraction): solids from Step 1 extracted with 40 mL 0.5 M hydroxylammonium chloride at pH 1.5 for 16 h, centrifuged, extracts stored at 4°C for ICP-MS.
- Units:
  - Total metals: mg/kg
  - Bioavailable metals: ppm

## Data structure and fields
- Key data columns:
  - Rural/Urban: land-use category for sampling site
  - Location: common name of the location
  - Latitude: geographic latitude
  - Longitude: geographic longitude
  - pH: soil pH value
  - Metals/elements measured: Al, As, Be, Cd, Cr, Cu, Fe, Pb, Hg, Ni, P, Zn
  - Results grouped into:
    - Total metals (aqua regia extractions) – columns F–Q
    - Bioavailable metals (Step 1 BCR extractions) – columns R–AD
    - Bioavailable metals (Step 2 BCR extractions) – columns AE–AQ

## Data handling and context
- Data are compiled from chemical analyses of soil samples across predefined field sites, enabling spatial visualization and mapping of metal contamination and bioavailability, alongside microbial resistance gene context when integrated with DNA results.
- Data processing aligns with standard sequential extraction and QA practices to ensure comparability across samples and treatments.

## References
- ISO (2005) ISO 10390:2005(E) Soil Quality - Determination of pH
- Mossop KF, Davidson CM (2003) Comparison of original and modified BCR sequential extraction procedures for the fractionation of copper, iron, lead, manganese and zinc in soils and sediments. Analytical Chimica Acta, 478:111-118
- Quevauviller P, Rauret G, López-Sánchez J-F, Rubio R, Ure A, Muntau (1997) Certification trace metal extractable contents in a sediment reference material (CRM 601) following a three-step sequential extraction procedure. Science of the Total Environment, 205(2-3):223-234
- Rothwell KA, Cooke MP (2015) A comparison of methods used to calculate normal background concentrations of potentially toxic elements for urban soil. Science of the Total Environment, 532:625-634