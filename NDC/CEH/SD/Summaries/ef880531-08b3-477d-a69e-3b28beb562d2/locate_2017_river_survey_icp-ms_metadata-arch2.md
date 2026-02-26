# Summary

- LOCATE is a multidisciplinary NERC project involving the National Oceanography Centre, the British Geological Survey, the UK Centre for Ecology and Hydrology, and the Plymouth Marine Laboratory, with collaboration from several universities and the Environment Agency. Part 2 contains ICP-MS results from river samples; Part 1 covers river water parameters and estuarine data, with DOIs provided for the corresponding datasets. The project aims to improve understanding of carbon flow from land to the ocean, using representative catchments across Great Britain.

- Data scope and purpose
  - Field data collection in 41 rivers across England, Scotland, and Wales, from January to December 2017, with additional sampling in November 2016 (trial). The dataset documents geographical and seasonal variation of cations.
  - Rivers selected to reflect varied land use and to be broadly representative of Great Britain; detailed river sampling information is available in locate_river_info.txt.
  - Part 2 specifically contains ICP-MS analyses (major and trace elements) aligned with the Part 1 river water parameter dataset for integrated interpretation.

- Sampling design and regime
  - Monthly sampling at fixed sites on each river, with most sites sampled in 2–3 days per month; Dorset Stour (DSTO) had a staggered start in April 2017.
  - Coordination led by Andy Tye (BGS).
  - After a pilot (Nov 2016), the program moved to HMS sites to improve data integration.
  - In-field sampling protocol emphasizes contamination control, sample handling, and environmental recording:
    - Field filtering and bottle preparation; POC samples filtered in the lab.
    - Samples kept dark and cooled; salinity, electrical conductivity (SEC), and temperature measured in the field when possible.
    - Mid-channel ~0–30 cm sampling depth, representative of main river body where feasible.
    - Use of gloves, dedicated collection vessels, and cleaning steps to prevent contamination.
    - Photos captured upstream and downstream at sampling sites; weather and river conditions recorded on field forms.

- Sample processing and laboratory workflow
  - Field processing mostly completed on-site; some steps (POC) performed later in the lab.
  - Samples transported on cool boxes or in freezers; chemical preservation by acidification performed at the BGS Keyworth lab.
  - Isotope and ICP-MS samples prepared with appropriate filtration and bottle types; samples preserved with 1% HNO3 for ICP-MS analyses.
  - Blanks prepared from acidified MQ water; standardized QA procedures used to minimize contamination.

- ICP-MS analyses: instrument, method, and units
  - Instrument: Agilent 8900 ICP-QQQ.
  - Analytical method: Ag_2.3.21 Determination of major and trace elements in aqueous samples using ICP-MS.
  - Units: mg/L or μg/L for detected elements.
  - Sample preparation: 0.45 μm filtered water acidified to 1% HNO3; post-receipt, samples may be adjusted with 0.5% v/v HCl for analysis.
  - Laboratory accreditation: UKAS ISO/IEC 17025:2017 (lab number 1816).

- Quality control and data integrity
  - QA/QC performed every ~20 samples with Shewhart plotting; three calibration blocks per run (~125 samples).
  - Use of composite multi-element stock standards and certified single-element standards for calibration.
  - Detection limits specified as two values per element (batch DL and method DL); values below DL reported as below-detection in the dataset.
  - Data handling notes: missing values labeled as n/a; detailed DL information and instrument-specific notes provided to guide data interpretation.

- Data format and content
  - Data file: CSV with 61 columns containing ICP-MS results.
  - Key fields include:
    - LIMS code (lab sample number), River, Month.
    - Element concentrations for a wide suite (Ca, Mg, Na, K, P, S, Si, SiO2, Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, V, Cr, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, La, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Yb, Tm, Lu, Hf, Ta, W, Tl, Pb, Bi, Th, U).
    - Units: mg/L or μg/L as appropriate; detection limits included in the metadata.
  - Data conventions:
    - n/a denotes missing values.
    - Two detection limits per element line: batch DL and method DL; non-detects typically reported as < DL.
  - Supplementary data: river sampling details and site information provided in locate_river_info.txt; dataset references include DOIs for Part 1 estuarine and land-to-river data and the BODC portal for data access.

- Accessibility and related materials
  - Part 1 dataset covers river water parameters (temperature, SEC, salinity, and various chemical constituents) and companion estuary data.
  - Locational and methodological documentation supports cross-dataset integration and comparative analyses.
  - Data management and access align with the LOCATE project’s aim to enable broader data reuse and policy-relevant environmental monitoring.

- Relevance for environmental monitoring analysts
  - Provides standardized, quality-assured, geospatially distributed river chemistry data suitable for monitoring changes in freshwater cation composition over time and space.
  - Supports assessment of environmental health and policy performance through temporal and spatial trends in major and trace elements in UK rivers.
  - Emphasizes data interoperability by coordinating sampling sites, consistent field protocols, and documented QA/QC procedures to facilitate integration with other LOCATE datasets and external data portals.