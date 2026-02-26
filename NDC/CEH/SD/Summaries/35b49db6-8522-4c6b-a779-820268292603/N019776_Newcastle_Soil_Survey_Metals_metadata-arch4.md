# Community antimicrobial resistance genes and concentrations of polycyclic aromatic hydrocarbons and metals in NE England soils

- Purpose and scope
  - Dataset collates the relative abundance of antimicrobial resistance genes found in DNA from soils around Newcastle upon Tyne.
  - Sampling locations were preselected based on metal concentrations and land-use, representing four treatments: low-metal/rural, low-metal/urban, high-metal/rural, and high-metal/urban.
  - Fieldwork aims to link antimicrobial resistance gene presence with soil metal content.

- Fieldwork details
  - Location: soils surrounding Newcastle upon Tyne, NE England.
  - Sampling period: June 2016.
  - Depth and handling: samples collected from the upper horizon (<15 cm) and refrigerated until processing.

- Analytical methods
  - pH measurement: ISO 10390:2005, soil suspension in deionised water (1:5, slurry), shaken 1 hour, equilibrated overnight, measured with a pH meter.
  - Total metal concentrations: determined by ICP-MS after aqua regia digestion (1 g soil in 1:3 nitric acid:HCl).
  - Bioavailable metals (step 1): extracted with 0.11 M acetic acid (Step 1 of the BCR procedure) for 16 hours, followed by ICP-MS analysis.
  - Bioavailable metals (Step 2): residual solids from Step 1 treated with 0.5 M hydroxylammonium chloride at pH 1.5 for 16 hours; extracts analyzed by ICP-MS.
  - Storage: extracts stored at 4°C prior to ICP-MS analysis.

- Nature of recorded units
  - Total metals: mg/kg (milligram per kilogram).
  - Bioavailable metals: ppm (parts per million).

- Data structure and key variables
  - Main location descriptors:
    - Rural/Urban: land-use category
    - Location: common name of location
    - Latitude and Longitude: geographic coordinates
  - Soil characteristics:
    - pH: soil pH value
  - Metals analyzed (Al, As, Be, Cd, Cr, Cu, Fe, Pb, Hg, Ni, P, Zn)
  - Result groups (three sets of columns):
    - Total metals (aqua regia extractions) — columns F to Q
    - Bioavailable metals (Step 1 BCR extractions) — columns R to AD
    - Bioavailable metals (Step 2 BCR extractions) — columns AE to AQ

- References and standards
  - ISO 10390:2005(E) Soil Quality - Determination of pH
  - Mossop KF, Davidson CM (2003) – Modified BCR sequential extraction procedures
  - Quevauviller et al. (1997) – Certification of extractable contents using a three-step extraction
  - Rothwell KA, Cooke MP (2015) – Methods for calculating background concentrations of potentially toxic elements in urban soil

- Data governance and reuse considerations (Data Leaders perspective)
  - Use of standardized measurement methods (ISO, BCR) enhances comparability and reliability across datasets.
  - Comprehensive metadata (location, depth, pH, three metal measurement schemes, units) supports discoverability, interpretation, and reuse.
  - Spatial coordinates enable integration with other geographic or environmental datasets and facilitate user-centered data products.
  - Clear separation of total vs. bioavailable metal data supports analyses of environmental availability and potential exposure pathways.
  - Dataset design aligns with need for data transparency, provenance, and potential cross-project collaboration (e.g., linking AMR gene abundance with environmental metal context).