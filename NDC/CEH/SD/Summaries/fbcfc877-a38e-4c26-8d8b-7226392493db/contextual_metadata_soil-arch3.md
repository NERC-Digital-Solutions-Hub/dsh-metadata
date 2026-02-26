Discovery metadata- Soil nutrients, soil pyrogenic carbon, soil bulk density and roots dry weight under different intensities of soil management in the Colombian Andes between 2019-2021

## Summary

- Objective and scope
  - Provides discovery metadata for a dataset aimed at understanding how soil characteristics change across disturbance gradients to inform forest resilience and ecosystem functioning in Colombian Andean forests.
  - Part of the BioResilience project; data collection occurred from 2019 to 2022 across 27 permanent monitoring plots (0.5 ha each) along an altitudinal gradient (lowlands, midlands, highlands) and a disturbance gradient (low, medium, high perturbation).

- What is included
  - Four CSV datasets:
    - pyrogeniccarbonbr.csv: soil pyrogenic carbon (TOC, Cpyc, D13C for pyrogenic carbon, Cpyc%), %Cpyc/Cbulk, %OC, plot and depth metadata.
    - soilnutrientbr.csv: soil nutrients and texture (pH, available P, total P, sand, clay, silt) and exchangeable cations (Ca, Mg, K, Na).
    - bulkdensitybr.csv: bulk density with location and land-use context (Depth, Date, Municipality, Department, Farm, Land_use, Ecosystem, Bulk_density).
    - dryweigthbr.csv: roots dry weight with ecosystem, land-use, and location context (Depth, Dry_weight).
  - Detailed metadata fields and units, enabling traceability from plot to measurements and practical interpretation.

- Study design and location
  - 27 plots (0.5 ha each) distributed across:
    - Altitude: lowlands, midlands, highlands.
    - Disturbance gradient: low, medium, high perturbation with recovery time categories.
  - Geographic context includes multiple local reserves and private properties across the Eastern Cordillera and surrounding areas of Colombia.
  - Coordinates and site descriptors (municipio, departamento, ecosystem, land use) are provided for each plot.

- Methods and analytes
  - Pyrogenic carbon (PHYC) quantified via hydrogen pyrolysis (HyPy); TOC determined by elemental analysis (Costech ECS-4010); Cpyc and Cpyc%/Cbulk derived as described; D13C values reported for pyrogenic carbon with uncertainty bounds.
  - Soil nutrients measured using standard soil chemistry procedures:
    - pH in water; available P via sequential resin/chemical extractants; total P by acid digestion with H2O2.
    - Particle size analysis by Bouyoucos method (sand, silt, clay).
    - Exchangeable Ca, Mg, K, Na by Ag-TU extraction.
  - Physical properties:
    - Bulk density measured from pit samples; roots dry weight recorded for biomass assessment.
  - Calibration and quality control steps confirm instrument accuracy and data integrity (external review of databases and metadata for completeness, consistency, and structure).

- Data structure and content
  - Four CSV files with explicit column lists and units:
    - pyrogeniccarbonbr.csv: Plot_code, depth_range_cm, depth_upper_cm, depth_lower_cm, depth_mid_cm, Sample_Id, Project/Collected, %C_(Bulk), Lower_D13C_(pyc), Median_D13C_(pyc), Upper_D13C_(pyc), Cpyc_(%), %Cpyc/Cbulk, %OC, etc.
    - soilnutrientbr.csv: Plot_code, pH, p_available, tot_p, sand, clay, silt, Ca_ex, Mg_ex, K_ex, Na_ex.
    - bulkdensitybr.csv: Plot_code, Depth, Date_sample_taking, Municipio, Departamento, Farm, Land_use, Ecosystem, Bulk_density.
    - dryweigthbr.csv: Plot_code, Ecosystem, Land_use, Municipio, Departamento, Depth, Dry_weight.
  - Clear documentation of measurement ranges, units, and data validation notes per variable.

- Data quality, provenance, and governance
  - Systematic calibration and validation procedures documented; data reviewed by individuals outside the soil team for structure, completeness, typing, and lack of duplicates.
  - Metadata validation ensures accuracy, completeness, and consistency with the databases.
  - Data provenance links measurements to plots, depths, and laboratories involved in analysis across partner institutions (UNAD, INPA, James Cook University).

- Relevance for monitoring frameworks
  - Provides a multi-indicator data package suitable for monitoring soil health and forest resilience under varying disturbance intensities.
  - Key indicators include:
    - Soil chemical status: pH, available and total P, exchangeable cations.
    - Soil physical/biophysical status: bulk density, root biomass.
    - Soil organic matter and carbon dynamics: TOC, pyrogenic carbon stocks, pyrogenic carbon fraction relative to total organic carbon, and isotopic composition (D13C) of pyrogenic carbon.
  - Spatial design supports comparison across altitude bands and disturbance levels, aiding the assessment of drivers of variation in ecosystem functioning.

- Considerations and potential limitations
  - Temporal scope spans 2019–2022; cross-sectional snapshots may require ongoing monitoring for trend analysis.
  - Data ownership and sharing policies are framed within the BioResilience project; ensure alignment with monitoring program governance and data-sharing agreements.
  - Some metadata presentation in the description includes formatting artifacts; users should rely on the four structured CSVs and accompanying metadata for precise field definitions.

- Practical implications for decision-making
  - Enables evidence-based selection of soil health indicators to inform land management and restoration strategies in Andean forests.
  - Facilitates reporting through structured data outputs (tables, charts, dashboards) to communicate soil health and resilience trends to stakeholders.