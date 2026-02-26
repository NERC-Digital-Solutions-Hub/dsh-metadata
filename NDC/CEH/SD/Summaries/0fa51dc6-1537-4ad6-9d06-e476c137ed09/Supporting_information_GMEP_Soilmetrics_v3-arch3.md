# Glastir Monitoring & Evaluation Programme

- Purpose and scope
  - Welsh Government’s Glastir monitoring programme (GMEP) collects evidence on the effectiveness of management bundles to improve soil quality and to quantify status and trends in soil health.
  - Aims to link soil-related outcomes to drivers of change (land use, climate, pollution) beyond Glastir interventions.
  - Supports policy appraisal and future decision-making for environmental health outcomes (climate change, biodiversity, soil and water quality, woodland expansion).

- Monitoring design and approach
  - Ecosystem-based, multi-scale data captured in a single snapshot when possible.
  - 4-year rolling survey cycle (first cycle 2013–2016) to maximise site coverage while enabling year-on-year trend analysis.
  - Two integrated components:
    - Wider Wales Component: baseline estimation, national trends, and national reporting for Glastir.
    - Targeted Component: focus on Glastir priority areas.
  - Common spatial unit: 1 km2 squares to facilitate national and sub-national indicators and future integration with other surveys (e.g., Countryside Survey).
  - Sample frame: 300 1 km2 squares over four years
    - Half randomly sampled within strata defined by the Land Classification of Great Britain (to maximise environmental representativeness).
    - Half targeted at Glastir priority areas.
  - Exclusion criteria: remove squares with >75% urban land or >90% sea coverage.
  - Spatial mapping: distribution of squares plotted at 10 km resolution to protect data confidentiality.

- Field sampling and laboratory methods
  - Within each square: 5 soil samples collected from randomly dispersed locations using a 15 cm black plastic core, aligned with vegetation surveys.
  - Sample handling: cores refrigerated and shipped promptly to CEH Bangor and CEH Lancaster laboratories.
  - Key soil metrics and analyses:
    - Soil organic matter and carbon
      - Loss on Ignition (LOI) measured on 10 g sub-sample; 105°C drying, 375°C combustion.
      - Carbon concentration derived as C = LOI (%) × 5.5 for compatibility with legacy Countryside Survey data.
      - Quality control via internal soil standards; repeat if deviations exceed historical tolerances.
    - Total soil organic carbon (SOC) and nitrogen (TN)
      - Inorganic carbon removal followed by analysis with Elementar Vario-EL elemental analyser.
      - Quality control with in-house reference materials.
    - Total phosphorus and Olsen phosphorus
      - P-total: acid digestion (H2O2 and H2SO4) with colorimetric SEAL AQ2 analysis.
      - Olsen-P: extraction with Olsen reagent (0.5 M NaHCO3, pH 8.5) and measurement by molybdenum blue chemistry.
      - QC: duplicate samples, blanks, and matrix-matched references.
    - pH (in DIW and in CaCl2)
      - Standard slurry method (soil-to-water or soil-to-CaCl2 ratios) per established reference.
      - QC with internal standards.
    - Electrical conductivity (EC) of soil slurry
      - Measured with a conductivity meter after soil-slurry preparation.
      - QC as above.
    - Soil bulk density (fine earth) and volumetric water content (VWC)
      - Calculated from chemical core measurements; VWC derived from bulk density and gravimetric water content.
      - QC through standardized sampling sleeves and trained surveyors.
    - Soil water repellency (WDPT)
      - Water drop penetration time on air-dried soil surface; results captured on video for accuracy.
      - QC via standardized droplet volume and timing.
  - Data product and metadata
    - Central dataset: GMEP_SOIL_METRICS_2013_16.csv
      - Includes spatial identifiers, plot type, year, and all measured metrics with units and descriptions.
      - Provides derived fields (e.g., C_FE_CTOTAL, C_FE_LOI, C_FE_PTOTAL, Olsen-P, pH, EC, BD, VWC, SWR).
    - Metadata captures sample locations, sampling plots, and easting/northing coordinates to enable national-scale aggregation and trend analysis.

- Data governance, quality assurance, and openness
  - Emphasis on data quality assurance through standardized protocols, calibration, and QA/QC checks (internal standards, duplicates, blanks).
  - Data management and sharing considerations aligned with openness and governance standards; underlying data intended for public sharing where appropriate.
  - Integration with legacy datasets (e.g., Countryside Survey) to enable long-term comparability and broader synthesis.

- Stakeholders and organisational roles
  - Lead responsibility within CEH (Centre for Ecology & Hydrology) with a dedicated GMEP team:
    - Lead scientist, QA/data management, field coordination, laboratory analysis, and data processing.
  - Bangor University and field survey teams contribute to biodiversity oversight, field execution, and data collection.
  - Field teams and laboratory staff collaborate to ensure timely sample processing and data integrity.
  - Output supports Welsh Government policy decisions regarding Glastir and broader environmental health outcomes.

- Policy relevance and intended use
  - The monitoring framework is designed to generate robust national and sub-national indicators of soil quality and to trace changes driven by land use, climate, and pollution beyond Glastir interventions.
  - Data and analyses feed into reporting for Glastir outcomes, inform adjustments to management practices, and support evidence-based policymaking related to soil health, climate resilience, and ecosystem services.