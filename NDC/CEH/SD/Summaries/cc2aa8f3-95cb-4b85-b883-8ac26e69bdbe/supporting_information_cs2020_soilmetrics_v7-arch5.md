# UKCEH Countryside Survey data 2020

## Purpose and Context
- National rolling survey to monitor soil condition and function across Great Britain, linking to vegetation data for an ecosystem-based assessment.
- Aims to determine the direction and magnitude of soil change and how multiple pressures interact, informing soil health, climate, and food/public health relevance.
- Rolling program supports generation of stock and change maps and data across a 5-year cycle, with 2019 as the start of the current phase.

## Sampling Design and Scope
- Rolling survey: 500 x 1km squares sampled over five years; 100 squares visited annually.
- Squares selected within strata defined by the Land Classification of Great Britain (2007); older 1978/1998/2007 squares form part of the resampling scheme.
- Exclusions: squares with >75% urban land or >90% sea.
- 2020 Covid disruption: May–June fieldwork hindered; 50 England-only squares reselected for the latter portion of the year.

## Data Collection and Field Methods
- In each selected 1km square, 49 sample squares are surveyed, with soil samples collected from 5 randomly dispersed locations alongside vegetation X-Plots.
- Soil samples collected from the top 0–15 cm using a 15 cm C-core; cores stored refrigerated and sent to UKCEH Bangor laboratories.
- Historical sampling locations have shifted over time (1978, 1990, 1998, 2007, 2019) to maintain relocalisation accuracy.
- Field methods are detailed in an accompanying field manual.

## Metrics, Laboratory Protocols, and Calculations
- Key soil metrics measured or derived include:
  - Soil organic matter (Loss on Ignition, LOI), soil carbon concentration, bulk density, porosity, hygroscopic water content, and CaCO3.
  - pH in deionised water (DIW) and in CaCl2; electrical conductivity (EC) in DIW.
  - Olsen phosphorus (P Olsen), total phosphorus (TP), total soil organic carbon (SOC) and total nitrogen (TN), and CN ratio.
  - Soil classification and grouping (ITE Land Class 2007; UKCEH-CS soil carbon groups).
  - Depth of peaty horizons to distinguish peat soils.
- Laboratory methods include:
  - LOI and hygroscopic moisture via LECO TGA701 (thermogravimetric analysis).
  - pH measurements with internal QC standards; DIW and CaCl2 extraction.
  - Olsen-P via molybdate-antimony colorimetric method; TP via H2O2/H2SO4 digestion with colorimetric analysis.
  - SOC and TN via elemental analysis (Vario-EL) after inorganic carbon removal; QC with in-house references and standard materials.
- Derived calculations:
  - Carbon concentration (%C) from LOI using established calibration (0.5453*LOI + 0.4366) with conversions to gC/kg and tC/ha.
  - Bulk density, porosity, mineral/organic fractions, and related conversions to enable stock and density calculations.
  - Carbon to nitrogen ratio and related soil stock metrics.
- Quality control:
  - Internal standards and duplicates in each batch; moisture, LOI, CaCO3 and Olsen-P controls; repeat analyses if QC criteria are not met.

## Data Structure and Metadata
- Data are stored in a structured, field-defined dataset with numerous variables, including:
  - Spatial/unit identifiers: SQ_ID (1km square), PLOT_ID (X-plot), YEAR, LC07 (ITE Land Classification), BROAD_HABITAT, and habitat descriptors.
  - Soil measurements: C_B_PH_DIW, C_B_PH_CACL2, C_B_EC, C_FE_MOISTURE_HYGRO, C_FE_LOI, C_FE_CACO3, C_FE_C_CONCLOI_GCPER100G, C_FE_C_CONCLOI_GCPERKG, C_FE_SOC_LOI_TC_HA, C_FE_LOI_FRACTION, C_FE_MIN_FRACTION, C_FE_PD_GPERCM3, C_FE_BULK_DENSITYGPERCM3, C_FE_POROSITY, C_FE_MASSSTONES, C_FE_VOLSTONES, C_FE_VWC, C_FE_GWC_D, C_FE_GWC_W, C_FE_POLSEN, C_FE_PTOTAL, C_FE_CTOTAL, C_FE_NTOTAL, CN_RATIO_FE.
  - Derived metrics and units for stock calculations (e.g., SOC stocks per hectare) and vegetation-linked fields.
- Data dictionary and methodological notes accompany the dataset to support discovery, interpretation, and reuse.

## Data Quality, Validation, and Governance
- Use of standardized methods with QA checks (internal standards, replicates, blanks, and repeat analyses where QC thresholds are not met).
- Detailed documentation of laboratory protocols, data derivations, and data conversions to ensure comparability with legacy Countryside Survey datasets.
- Data governance emphasizes traceability from field collection to laboratory analysis, archiving, and sharing within UKCEH data infrastructures and accompanying data papers.

## Annual Analysis, Trends, and Outputs
- Each year contributes to a rolling analysis of soil change (e.g., LOI and pH time series) following established methods (Scott 2008; Reynolds et al. 2013).
- UKCEH Countryside Survey data 2020 includes summary figures illustrating relationships such as:
  - Porosity vs LOI, LOI vs Bulk Density, LOI vs pH, LOI vs CaCO3, and LOI vs gravimetric/volumetric water content.
- Figures and datasets provide location-specific and depth-related insights, enabling national- and sub-national trend analysis.

## Covid-19 Impact (2020)
- Fieldwork interruption limited May–June 2020; later activities proceeded with reselected squares (50 England-only) to complete the year’s sampling.

## Data Access and Stewardship Considerations
- Data are backed by extensive methodological documentation, data dictionaries, and QC records to facilitate reuse and governance.
- The dataset forms part of a broader rolling program intended to feed national-scale soil change assessments and to support policy-relevant evidence on soil health and carbon dynamics.
- Coordination across CEH/UKCEH staff and field teams ensures consistent data capture, processing, archiving, and dissemination.

## People, Roles, and Acknowledgments
- CEH staff contributions span data management, soil processing, laboratory analysis, rolling program design, field operations, and project management.
- 2020 UKCEH Field Survey Teams and various CEH personnel are documented to support provenance and accountability.

## References and Supporting Materials
- Foundational works include Emmett et al. (2010), Scott (2008), Reynolds et al. (2013), Bunce et al. (2007), Ruehlmann (2020), and related Countryside Survey documentation and field manuals.
- The dataset is part of UKCEH’s ongoing Countryside Survey program, with supporting methodological and analytical citations.