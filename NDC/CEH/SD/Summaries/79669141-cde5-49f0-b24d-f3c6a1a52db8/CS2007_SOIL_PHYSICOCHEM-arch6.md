# Soil physico-chemical properties 2007 [Countryside Survey], Great Britain

- A dataset from Countryside Survey 2007 providing soil physico-chemical properties across Great Britain.
- Up to 591 1km squares surveyed (England, Scotland, Wales) with five plots per square.
- Measurements cover pH (in water and CaCl2), loss on ignition (LOI) and derived carbon, carbon stock, bulk density, moisture, nitrogen, nitrogen stock, Olsen phosphorus, land class, and location metadata.

## Data content and structure

- Core fields (example):
  - SQUARE: 1km square sampling site code
  - PLOT: Plot identifier within each square
  - YEAR: Survey year
  - PH: Fresh soil pH in water
  - LOI: Loss on ignition (%)
  - C_CONC_LOI: Carbon concentration from LOI (g/kg)
  - C_STOCK_LOI: Carbon stock from LOI (t/ha)
  - BULK_DENSITY: Bulk density (g/cm3)
  - MOISTURE: Moisture content (%)
  - N_PERCENT: Nitrogen percentage
  - N_STOCK: Nitrogen stock (t/ha)
  - PO4_OLSEN: Olsen phosphorus (mg/kg)
  - LC07 / LC07_NUM: ITE Land Class 2007 (text and numeric code)
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: County or equivalent
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data include both raw measurements and derived metrics (e.g., carbon from LOI, carbon stock).

## Measurement methods

- pH in water (fresh soil):
  - 10 g soil + 25 ml deionised water (1:2.5 w/w)
  - Read after 30 seconds of settling; measurements taken soon after sample opening
  - Calibration with pH buffers; temperature control within 1°C of soil suspension
- pH in CaCl2:
  - Two measurements per subsample (method details align with CS2007 protocols)
- LOI (loss on ignition):
  - Up to 3145 black cores; 10 g air-dried sub-sample
  - Dry at 105°C for 16 h, weigh, combust at 375°C for 16 h, reweigh
  - Use CS2000 and 1978 methods context; selected 1978 method for CS2007 compatibility
- Bulk density (BD):
  - Based on LOI sub-sample workflow; requires precise core dimensions and weight
  - Co-derived using LOI moisture steps; stones and soil density considered
  - ISO 11272:1998 reference not used due to dataset structure; alternative protocol implemented
- Olsen-P:
  - Extraction with 0.5 M NaHCO3 (pH 8.5), 5 g soil, 100 ml extract
  - Colorimetric determination (molybdenum blue) with dialysis step
  - Note on potential drying effects and organic matter co-extraction; consistent procedure with CS2000
- Total nitrogen (N):
  - Elementar Vario-EL analyzer; oxidative combustion
  - Calibration with acetanilide; two in-house references per batch
  - Typical sample weights 15 mg (peat) to 15–60 mg (mineral soil)

## Quality assurance and quality control

- QA/QC framework:
  - Defra/NERC/BBSRC Joint Codes of Practice followed
  - Batch-level QC: calibration checks after 25 samples; standard and certified reference materials; duplicates
  - Cross-checks and re-analyses when method changes or issues arise
- Bulk density QC:
  - Limited direct control soil; use proxy checks and inter-batch comparisons to assess reliability
- Olsen-P QC:
  - Replicate analyses plus standard and certified reference soil per batch of 25 samples
  - Consistency of extraction conditions emphasized
- Documentation of protocols and cross-comparison tests in the CS Soils Manual (2008)

## Sampling design and scope

- Sampling strategy:
  - Based on a stratified random design across Land Classes to capture environmental gradients
  - 591 sample squares selected (England 289, Wales 107, Scotland 195)
  - Field sampling from 1 km squares with soils collected from the western corner of Main Plots in 2007
- Sample processing:
  - Standard field and lab protocols; archiving of final samples
  - Power analyses conducted to ensure detection capabilities for major soil properties
- Comparability:
  - Efforts to align with CS2000 methodologies; LOI method harmonized for cross-year consistency
  - Field and laboratory procedures documented for reproducibility

## Data use and attribution

- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
- Copyright: Countryside Survey © CEH/NERC

## Related publications and resources

- CS Soils Manual and technical reports (CS Technical Report No. 3/07; 2008) detailing sampling, QA, archiving, and data manipulation
- Countryside Survey: Soils Report from 2007 (CS Technical Report No. 9/07; 2010)
- Key references on soil analysis methods and Land Classification (ITE MB lists)
- Countryside Survey website and CEH/NERC data repositories for access to reports and data

## Notes and caveats

- LOI method harmonization: CS2007 reused the 1978 LOI method to ensure consistency with CS1978 and CS2000 data
- Olsen-P methodological considerations:
  - Drying effects and temperature sensitivity can influence extraction and colorimetric results
  - Organic matter co-extraction may occur; results reflect extractable inorganic P under defined conditions
- Data processing:
  - Derived carbon concentrations and stocks depend on LOI values and a conversion factor (0.55)
  - Bulk density calculations rely on core measurements and LOI-derived moisture; where QC is limited, cross-batch comparisons are used to assess reliability