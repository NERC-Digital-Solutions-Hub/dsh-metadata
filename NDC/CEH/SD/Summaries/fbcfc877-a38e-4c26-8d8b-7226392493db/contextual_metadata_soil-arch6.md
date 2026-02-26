# Discovery metadata- Soil nutrients, soil pyrogenic carbon, soil bulk density and roots dry weight under different intensities of soil management in the Colombian Andes between 2019-2021

- Scope and purpose
  - Provides discovery metadata and four CSV data files for soil nutrients, pyrogenic carbon, bulk density, and roots dry weight.
  - Aims to enable analysis of how soil characteristics change across disturbance gradients and altitudinal zones in Colombian Andean forests.
  - Supports understanding of forest resilience and ecosystem functioning under varying perturbation levels.

- Study design and sampling
  - Permanent monitoring plots: 27 plots of 0.5 hectares each.
  - Altitudinal gradient categories: lowlands (0–1200 m), midlands (1200–2200 m), highlands (2200–3200 m).
  - Disturbance gradient: low, medium, high perturbation; recovery times specified (more than 30 years, 20–30 years, less than 20 years).
  - Plot allocation: three plots per perturbation level within each altitude category (27 plots total).
  - Location details provided for each plot, including coordinates, localities, and land-use context.

- Study area and locations
  - Five locations across the Colombian Andes with various forest types and disturbance histories.
  - Lowlands: Serranía de las Quinchas (Puerto Boyacá, Boyacá) and nearby private properties.
  - Midlands: Pedro Palo (Tena, Cundinamarca) and Encino (Santander).
  - Highlands: Encenillo (Guasca, Cundinamarca) and Martos (Guatavita, Cundinamarca).
  - Environmental context includes climate, topography, and forest successional stages.

- Data collection and parameters
  - Four CSV data files:
    - pyrogeniccarbonbr.csv: pyrogenic carbon and organic carbon data.
    - soilnutrientbr.csv: soil nutrients and texture data.
    - bulkdensitybr.csv: bulk density measurements.
    - dryweigthbr.csv: roots dry weight data.
  - Variables and key fields per file:
    - pyrogeniccarbonbr.csv
      - Plot_code, depth_range_cm, depth_upper_cm, depth_lower_cm, depth_mid_cm, Sample_Id, Project/Collected
      - %C_(Bulk), Lower_D13C_(pyc), Median_D13C_(pyc), Upper_D13C_(pyc)
      - Cpyc_(%), %Cpyc/Cbulk, %OC
      - Data concepts: Total Organic Carbon (TOC) via elemental analysis; Pyrogenic carbon (Cpyc) via hydrogen pyrolysis (HyPy); D13C corrections per Wurster et al. (2012); Cpyc%/CBulk ratio.
    - soilnutrientbr.csv
      - Plot_code, pH, p_available, tot_p, sand, clay, silt, Ca_ex, Mg_ex, K_ex, Na_ex
      - Units vary (pH, mg/kg for P, percentage for texture, cmolc/kg for exchangeable cations).
    - bulkdensitybr.csv
      - Plot_code, Depth, Date_sample_taking, Municipio, Departamento, Farm, Land_use, Ecosystem
      - Bulk_density (g/cm3)
    - dryweigthbr.csv
      - Plot_code, Ecosystem, Land_use, Municipio, Departamento, Depth, Dry_weight
      - Dry weight of roots (g)

- Data structure and units
  - Four CSV files with consistent naming: pyrogeniccarbonbr.csv, soilnutrientbr.csv, bulkdensitybr.csv, dryweigthbr.csv.
  - Columns and measurements standardized to enable cross-file joins by Plot_code and depth where applicable.
  - Example data ranges and units:
    - TOC (%C_bulk), %Cpyc, D13C (per mille), Cpyc (%), Cpyc/Cbulk (%)
    - pH (water), p_available (mg/kg), tot_p (mg/kg or % as context), sand/clay/silt (%), Ca_ex/Mg_ex/K_ex/Na_ex (cmolc/kg)
    - Bulk_density (g/cm3)
    - Dry_weight (g)
  - Metadata includes valid value ranges, detection limits, and measurement units for each variable.

- Data generation, transformation, and quality control
  - Collection/Transformation methods
    - TOC: elemental analysis with Costech ECS-4010 (0 blank autosampler).
    - Pyrogenic carbon (Cpyc): HyPy hydrogen pyrolysis; Cpyc%, Cpyc/Cbulk derived from HyPy results.
    - D13C corrections for pyrogenic carbon following Wurster et al. 2012.
    - Soil nutrients: pH via water extraction; available P via sequential resin/NaHCO3/NaOH/HCl extraction; tot_p via acid digestion (H2SO4/H2O2); texture by Bouyoucos method; exchangeable cations via Ag-TU extraction.
    - Bulk density: pit samples dried to constant weight.
  - Calibration and validation
    - Instrument calibration and reference value checks prior to data collection.
    - Calibration values established from literature review.
  - Quality control
    - Multi-person review of databases and metadata for structure, missing fields, data completeness, typing, and duplicates.
    - Metadata validation for accuracy and consistency.

- Provenance and references
  - Project context: BioResilience project, investigating forest resilience post-conflict in Colombia with cross-institutional collaboration (UNAD, INPA, James Cook University; supported by UK NERC NE/R017980/1).
  - Key references underpinning methods for pyrogenic carbon analysis, soil properties, and related methodologies (HyPy, D13C corrections, soil carbon fractions, and classical soil analysis methods).

- Potential uses and outputs for data support
  - Create self-serve data products (dashboards, pivot tables) enabling exploration of soil nutrients, pyrogenic carbon, bulk density, and root biomass across disturbance and altitude gradients.
  - Cross-dataset analyses to assess drivers of soil variation due to perturbation, altitude, and land-use context.
  - Data products for policymakers and researchers studying forest resilience, soil health, and carbon cycling in Andean ecosystems.
  - Provenance and metadata support to ensure reproducibility and transparency in data use and sharing.