# UKCEH Countryside Survey data 2020

- The Countryside Survey is a rolling, national-scale monitoring program (started in 2019 cycle) aimed at assessing soil condition and function across Great Britain and its constituent countries. It supports understanding how multiple pressures affect soil health and related vegetation interactions, informing policy and management.

## Study design and sampling coverage

- Rolling survey design: repeats on a five-year cycle or after 500 squares completed to detect change while buffering against climate variability.
- Sampling frame: 1 km squares selected from the Countryside Survey baseline (1978; 256 squares) plus 1998 and 2007 squares; 500 squares sampled over a five-year cycle, with 100 squares visited per year.
- Stratification and exclusions: squares are stratified by the Land Classification of Great Britain; exclusions include squares with >75% urban land or >90% sea.
- Covid disruption (2020): surveying paused in early 2020; 50 squares were reselected from England to complete fieldwork in the latter part of the year.

## Field sampling and measurement scope

- Within each 1 km square, 49 sample locations are used for soil sampling and vegetation X-Plots; five core soil samples are collected at pre-determined random locations per square.
- Core sampling: 15 cm long C-core samples from the top 0–15 cm, co-located with vegetation plots. Depths and locations have historical documentation to aid relocation in successive surveys.
- Sample handling: soils are refrigerated post-collection and sent to UKCEH laboratories for analysis.

## Laboratory methods and metrics

- Field protocols: detailed in accompanying field manuals; soil sampling and analytical workflows follow standardized methods.
- pH and EC: measured in deionised water and CaCl2 solutions; internal quality controls included.
- Soil organic matter and carbon: Loss on Ignition (LOI) and derived carbon (SOC) using loss-on-ignition data; hygroscopic water content and CaCO3 (calcite) determined via thermogravimetric analysis (TGA) from 25°C to 1000°C with four heating steps; carbon concentration derived from LOI with a regression-based conversion.
- Soil bulk density and porosity: calculated from core weights and volumes; stone content recorded; porosity derived from bulk and particle densities.
- Water content: gravimetric and volumetric water content computed from gravimetric data and bulk density.
- Nutrients: Olsen-P (for arable/improved grassland only) and total phosphorus (TP) measured via digestion and colorimetric methods; total soil organic carbon (SOC) and total nitrogen (TN) measured by an elemental analyzer after inorganic carbon removal.
- Quality control: multiple internal standards, duplicates (~10%), blanks, and reference materials used across batches; CaCO3 recovery checks and LOI validators included.

## Data structure and key variables

- Primary identifiers: SQ_ID (1 km square), PLOT_ID (X-Plot), YEAR, and land class descriptors (ITE Land Class 2007).
- Habitat and environment: BROAD_HABITAT, BROAD_HABITAT_DESC, AVERAGE_O_DEPTH (peat horizon depth), and multiple soil group classifications (SOIL_LOI_CS_GROUP, SOIL_GP_LOI_CS_1_4, SOIL_GP_1_3, SOIL_GP_1_5).
- Core soil measurements (examples): C_B_PH_DIW, C_B_PH_CACL2 (pH in DIW and CaCl2), C_B_EC (electrical conductivity), C_FE_LOI (LOI), C_FE_CACO3 (calcite%), C_FE_BULK_DENSITY, C_FE_PTOTAL (total phosphorus), C_FE_POLSEN (Olsen-P, arable/improved land only), C_FE_CTOTAL (total soil carbon), C_FE_NTOTAL (total nitrogen), CN_RATIO_FE, C_FE_SOC_LOI_TC_HA (SOC stock per hectare.
- Derived quantities: C_FE_C_CONCLOI_GCPER100G (%C), C_FE_C_CONCLOI_GCPERKG (gC/kg), C_FE_SOC_LOI_TC_HA (tC/ha), C_FE_VWC (volumetric water content), C_FE_GWC_D and C_FE_GWC_W (gravimetric/gravimetric water contents), C_FE_PTOTAL, and various LOI- and density-related derived fields.
- Data completeness: -9999 denotes missing sample data.

## Analysis and outputs

- Annual rolling analysis: time-series updates for soil organic matter (LOI) and soil pH in water, following established methodologies (Scott 2008; Reynolds et al. 2013).
- UKCEH Countryside Survey data 2020 Summary Figures present relationships and distributions for key metrics, including:
  - LOI vs. porosity
  - LOI vs. bulk density
  - pH vs. LOI and pH in CaCl2 vs. LOI
  - EC vs. LOI and calcite vs. LOI
  - LOI vs. gravimetric and volumetric water content
  - LOI vs. porosity distributions and histograms of LOI and pH
- Outputs are designed to support cross-year comparisons, national or sub-national indicators, and analyses linking soil condition to vegetation and land-use factors.

## Data quality, interpretation, and cross-references

- Employed standardized, traceable laboratory protocols with rigorous QC, including internal standards, duplicates, and batch-level controls.
- Data are intended for integration with vegetation metrics (accompanying vegetation dataset) to enable ecosystem-level analyses.
- Key literature and methodological references underpinning the design and analysis include Emmett et al. (2010, 2015), Scott (2008), Reynolds et al. (2013), Ruehlmann (2020), and foundational soil science references.

## Practical notes for data use

- The dataset provides a robust, long-term view of soil change across GB, suitable for stock-and-change assessments and policy-relevant reporting.
- The rolling design enables detection of gradual and episodic changes, while the 2020 Covid disruption highlights the need to account for sampling adjustments when interpreting year-on-year trends.
- Researchers should reference the standard codes and derived fields carefully, noting which measurements are available only for certain land-use classes (e.g., Olsen-P) and the hierarchical soil classifications used.