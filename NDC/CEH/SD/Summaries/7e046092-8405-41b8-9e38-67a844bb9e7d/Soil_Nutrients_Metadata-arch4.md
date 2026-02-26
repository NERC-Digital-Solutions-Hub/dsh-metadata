## Dataset Description (Soil_Nutrients)

- Purpose and scope
  - Describes soil nutrient availability across three land-use types in Sabah, Malaysia: unlogged tropical forest, logged tropical forest, and oil palm plantation.
  - Data were collected March–April 2016 as part of the NERC-funded BALI project.
  - Provides a nutrient supply rate dataset (µg/10 cm2 /14 days) for multiple elements.

- Dataset structure
  - Primary file: Soil_Nutrients.csv with 21 data columns plus metadata.
  - Core columns include: Identifier, Site, Land_Use, Plot_Name, Subplot, NO3_N, NH4_N, Total_N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd.
  - Metadata fields describe each column (description and unit/format).

- Sampling design and sites
  - 9 one-hectare plots across 3 sites representing the land-use types: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
  - Stratified design: each 1 Ha plot subdivided into 25 subplots (20 m x 20 m); 3 subplots randomly sampled per plot.
  - At 3 locations within each subplot, 4 pairs of PRS ion exchange membranes (one pair for cation and one for anion) buried to ~10 cm depth for 2 weeks.

- Laboratory analysis and measurements
  - Pooled membrane samples from each location are eluted with 0.5 M HCl for 1 hour.
  - NO3-N and NH4-N measured colorimetrically via flow injection analysis (FIA).
  - All other elements measured by inductively coupled plasma–optical emission spectroscopy (ICP-OES).
  - Results reported as supply rates per 10 cm2 area over the burial period (µg/10 cm2 /14 days).

- Data quality and detection limits
  - MDL (Method Detection Limits) provided for each element.
  - Data are reported as measured even if below the MDL; zeros indicate non-detectable concentrations.
  - MDL values listed for NO3-N, NH4-N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd (in µg/10 cm2 /14 days).

- Units and definitions
  - All elemental concentrations expressed as µg/10 cm2 /14 days.
  - Key descriptors: Site (geographical area), Land_Use (Unlogged forest, Logged forest, Oil palm), Plot_Name, Subplot.

- Provenance and references
  - Method references: Qian & Schoenau (2002) on ion exchange resins; Riutta et al. (2018) on disturbance effects in Bornean tropical forests.
  - Data collection linked to the Western Ag PRS resin system (www.westernag.ca).

- Potential uses for data leaders
  - Assess nutrient availability and flux differences across land-use types for policy framing or resource management.
  - Support data-driven decisions on land-use planning, conservation priorities, and restoration strategies.
  - Provide a structured, metadata-rich dataset suitable for integration into broader soil- nutrient datasets, enabling cross-site comparisons and supporting governance of data assets.
  - Enable verification and reproducibility of nutrient assessments through detailed sampling design and MDL documentation.

- Access considerations and limitations
  - Dataset reflects measurements from 2016 soil samples, with depth limited to ~10 cm and pooling across locations within subplots.
  - Availability of complete metadata improves discoverability and reuse but users should account for the pooling approach and site-specific context when applying results.
  - References and methodology provide guidance for potential replication or methodological alignment in future studies.