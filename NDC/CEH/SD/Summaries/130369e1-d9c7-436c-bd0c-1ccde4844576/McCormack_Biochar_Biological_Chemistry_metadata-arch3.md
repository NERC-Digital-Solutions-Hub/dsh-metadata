# Mesocosm Experiment Data Schema: Measurements of Biochar Treatment, Soil Properties, and Biota

- Purpose: Provides a structured set of environmental health metrics from a fully-factorial mesocosm experiment assessing biochar presence, crop treatments, and soil texture, to inform monitoring frameworks, policy scrutiny, and decision-making.

## Overview of the Dataset

- Experimental design: Fully-factorial mesocosm setup with four spatial blocks; each treatment combination represented in each block.
- Treatments and treatments metadata:
  - Biochar: Presence of 2% biochar (w/w) in soil; + indicates presence, - indicates absence.
  - Crop_Type: Barley seeded at 1.8 t ha-1, Ryegrass seeded at 2.0 t ha-1, or Unvegetated.
  - Soil_Texture: SC (sandy clay), SZL (sandy silt loam), or CL (clay loam).
- Sampling context:
  - Year: Year of sampling.
  - Block: Spatial block within the enclosure.
  - Sampling depth: Top 10 cm of soil (for biological densities and PLFA).
  - Core dimensions: 3.5 cm diameter soil cores.
- Data types included:
  - Biotic densities in soil (nematodes, microarthropods, collembola, Acari) per gram dry soil.
  - Plant biomass: Aboveground biomass per mesocosm; belowground biomass per g-1 soil.
  - Microbial community markers: Total PLFA and individual PLFA groups (Bacterial_PLFA, Fungal_PLFA, AM_Fungal_PLFA) per g-1 soil.
  - Soil chemical properties: Soil_C and soil_N (percent), non_py_soil_c (adjusted carbon content), soil_moisture, and soil_pH.
  - Note on missing samples: '.' indicates no sample taken.

## Key Variables and What They Measure

- Identifiers and treatments
  - Pot_Number: Unique identifier for each mesocosm.
  - Biochar: 2% biochar presence in soil (± notations).
  - Crop_Type: Barley, Ryegrass, or Unvegetated.
  - Soil_Texture: SC, SZL, or CL.
  - Year: Sampling year.
  - Block: Spatial block identifier.

- Biota and soil fauna
  - Density_Nematoda: Individuals per gram dry soil (top 10 cm).
  - Density_Microarthropod: Individuals per gram dry soil (top 10 cm).
  - Density_Collembola: Individuals per gram dry soil (top 10 cm).
  - Density_Acari: Acari density per gram dry soil (top 10 cm).

- Plant biology
  - Aboveground_Biomass: Grams of aboveground plant biomass per mesocosm (destructively harvested annually).
  - Belowground_Biomass: Grams of belowground biomass per g-1 soil.

- Microbial community indicators
  - Total_PLFA: nmol phospho-lipid fatty acid per g-1 soil.
  - Bacterial_PLFA: nmol bacterial PLFA per g-1 soil (markers listed).
  - Fungal_PLFA: nmol fungal PLFA per g-1 soil.
  - AM_Fungal_PLFA: nmol arbuscular mycorrhizal fungal PLFA per g-1 soil.

- Soil chemistry and physical state
  - soil_C: Soil nitrogen content (%) (note potential labeling inconsistency in the source).
  - soil_N: Soil carbon content (%) (note potential labeling inconsistency in the source).
  - non_py_soil_c: Adjusted non-pyrogenic soil carbon, calculated to subtract biochar-derived carbon (Ca = Ct - 0.02*Cb/0.98; with Ct total C, Cb biochar C, Cb = 72.3%).
  - soil_moisture: Soil moisture by weight difference before/after oven drying.
  - Soil_pH: pH measured from a 1 g soil subsample with 2 ml deionised water after shaking.

- Data quality and handling notes
  - Note: '.' indicates no sample was taken for that variable/time point.

## Sampling Design and Analytical Methods

- Sampling design
  - Fully-factorial combination of biochar treatment, crop type, and soil texture across four spatial blocks.
  - Annual destructive harvests for aboveground biomass; soil samples collected from top 10 cm for biotic and chemical analyses.

- Analytical methods
  - Carbon and nitrogen: Flash combustion at 950 °C (EL Cube).
  - pH: Soil-water suspension with a standardized shaking and measurement protocol.
  - PLFA: Biomarker lipid analysis to quantify microbial community structure (bacteria, fungi, AM fungi).
  - Biomass and densities: Destructive biomass harvests and microscopic or chemical quantification of soil biota per gram soil.

## Data Quality, Metadata, and Governance Considerations

- Metadata needs and gaps
  - Metadata completeness is crucial for reuse; potential barriers include data silos and the need for robust metadata to verify dataset suitability.
  - Some fields may require clarification or correction (notably the potential label swap between soil_C and soil_N).

- Data sharing and openness
  - Underlying data should be openly shared with clear documentation, but sharing can be a barrier without proper governance and quality standards.

- Data transformation and standardization
  - Some measurements require transformation (e.g., PLFA units, biomass normalization per g-1 soil) to enable cross-study comparisons.
  - Consistent unit usage and documentation of methods are essential for comparability in monitoring frameworks.

- Data governance implications
  - Need for retaining provenance, versioning, and clear data-quality checks to support policy-relevant analyses and reporting.

## Relevance for Environmental Monitoring and Policy

- Indicators covered
  - Soil biodiversity and microbial community structure (Density metrics; PLFA profiles).
  - Soil biogeochemistry (C and N content; non-pyrogenic carbon adjustments).
  - Plant-soil interactions (aboveground and belowground biomass).
  - Physical-chemical soil properties (moisture, pH).

- Policy and decision use
  - Provides a framework to assess the environmental health impacts of biochar amendments under different crop management and soil textures.
  - Supports development of monitoring indicators for soil health, carbon sequestration, and ecosystem function in policy evaluations.

- Limitations to consider for policy transfer
  - Mesocosm results are controlled experiments; field-level generalization requires caution.
  - Sampling is focused on the top 10 cm; deeper soil processes are not captured.
  - Temporal scope and frequency may limit long-term trend assessment.