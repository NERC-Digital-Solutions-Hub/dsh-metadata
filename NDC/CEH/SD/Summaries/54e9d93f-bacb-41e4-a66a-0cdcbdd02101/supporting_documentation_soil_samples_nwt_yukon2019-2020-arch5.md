# Environmental context and metadata for permafrost soil samples, NWT & YT, Canada, 2020

- Purpose and scope
  - Dataset reports carbon (C) and nitrogen (N) content of permafrost soil samples from Northwest Territories (NWT) and Yukon Territory (YT), Canada, collected in 2019 and 2020.
  - Samples collected by Murton, Opel, Kokelj; CN analysis conducted by Friggens with support from Zaragoza-Castells; samples processed and stored for analysis.

- Data structure and contents
  - One CSV file: Soil_samples_NWT_Yukon2019-2020.csv with 14 columns describing CN content and metadata for each soil sample.
  - A Word document accompanying the dataset provides detailed site descriptions, sampling environments, and procedural context.
  - Sample identifiers and coding scheme
    - Sample numbers encoded as 19XX-xxx (year 2019), location codes EC/T/K/HUS/CRB_S, profile numbers (P1–P6), and short sample identifiers.
    - 14 soil profiles (#1–#14) spanning three regions with multiple sampling depths and sites.
  - Geographic and temporal metadata
    - Latitude and longitude for each site; sampling dates in August 2019 or August 2020.
  - Depth and stratigraphy
    - Depth below ground surface for each sample; active-layer (AL) vs permafrost (Pnc, Pc, ALc) classifications; ALT values; descriptions of organic and mineral soil layers.
  - Content descriptors
    - Short descriptions for each sample, sampling methods, storage notes, total sample mass, and CN measurements.

- Sampling design and collection methods
  - 14 soil profiles across three regions: East Channel (EC), Tuktoyaktuk (T), and Klondike (K).
  - Four soil profile types represented: non-lake orthels, drained thermokarst-lake sediments, turbels, and yedoma deposits.
  - Sampling approaches included soil pits, coring, and horizontal drill holes into thaw slumps.
  - Detailed site-level context per profile (geomorphic setting, vegetation, organic/mineral soils, ALT, ground ice observations, sampling positions) with multiple depth samples per profile.

- Data provenance and personnel
  - Field collection by Julian Murton, Thomas Opel, Steve Kokelj (and others noted in profiles).
  - Post-collection processing and CN analysis conducted at the University of Exeter in 2021 by Nina L. Friggens; instrument used: Thermo Scientific Flash 2000 Elemental Analyser.
  - Quality control and calibration performed using EDTA standards (N and C reference values provided).

- Analytical methods and quality control
  - CN analysis performed on defrosted, homogenised soil samples; ~10 g sub-samples oven-dried and analysed.
  - EDTA standards used at start and as check standards every ten samples; reference values: N 9.59% (±3%), C 41.1% (±1%).
  - Frozen storage maintained from field to laboratory; samples shipped frozen and processed under controlled conditions.

- Nature and units of recorded values
  - Data fields include: sample code, soil type, active layer designation, latitude/longitude, depth, date collected, total mass, short description, sampling method, storage during fieldwork, C content (%), N content (%).
  - CN results are reported as percentages and linked to each sample’s depth and classification (AL, Pc, Pnc, etc.).

- Data storage, access, and preservation
  - Field samples stored frozen; transported to the field station and then to the Exeter lab for processing.
  - CN results generated in 2021 and associated with the original sample identifiers.
  - Documentation includes extensive site-level metadata to support reproducibility and re-use.

- Contextual notes and limitations relevant to data stewardship
  - Ground-ice observations are variable by site and depth; some profiles show well-developed ice-rich horizons, while others have limited or no observed ground ice.
  - Cryoturbation and soil-structure interpretations (e.g., lenticular cryostructures) are described for multiple profiles, aiding interpretation of permafrost dynamics but requiring careful handling in downstream analyses.
  - The accompanying Word document provides rich environmental context per site, which is essential for secondary use but increases the need for thorough metadata management to ensure consistent reuse.
  - No explicit licensing or access restrictions are stated in the summary; data stewardship should clearly define data licensing, reuse rights, and citation requirements.

- Recommendations for data stewardship and reuse
  - Ensure the CSV and accompanying metadata document are linked through a stable data portal with clear licensing and citation guidance.
  - Maintain a data dictionary mapping sample codes to full identifiers, site coordinates, depths, and depth-specific classifications to support traceability and reproducibility.
  - Provide versioning and update pathways in case future CN measurements or site re-sampling are added.
  - Consider including data provenance notes and processing workflow (e.g., defrosting, homogenisation, drying, CN analysis steps) in machine-readable form to facilitate reproducibility.
  - Include any embargo or access restrictions, if applicable, and ensure metadata remains aligned with data access policies.