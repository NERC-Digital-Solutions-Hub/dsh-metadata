# Soil physico-chemical properties 2007 [Countryside Survey], Great Britain

- A dataset of soil physico-chemical properties collected in 2007 across Great Britain, covering up to 591 1km squares.
- Measured properties include pH, loss on ignition (LOI), moisture, bulk density, carbon and nitrogen content/stock, and Olsen phosphorus.
- Data are organized per 1km square (SQUARE) with up to five plots (PLOT) within each square and a recorded year (YEAR).

## Dataset scope and structure

- Spatial coverage: Great Britain, 591 1km squares (England, Wales, Scotland) sampled in 2007.
- Attributes (columns):
  - SQUARE, PLOT, YEAR
  - PH (pH in water), LOI (loss on ignition), C_CONC_LOI (carbon concentration, g/kg; 0.55 × LOI), C_STOCK_LOI (carbon stock, t/ha; 0.55 × LOI)
  - BULK_DENSITY, MOISTURE, N_PERCENT, N_STOCK (0–15 cm), PO4_OLSEN (Olsen P, mg/kg)
  - LC07 (ITE Land Class 2007), LC07_NUM (numeric code)
  - COUNTRY, COUNTY07, EZ_DESC_07 (environmental zone description)
- Derived metrics: C_CONC_LOI and C_STOCK_LOI computed using a bespoke conversion factor (0.55 × LOI).

## Variables and derived metrics

- pH measurements:
  - PH: fresh soil pH in water
  - Two measurements per subsample: pH in water and pH in 0.01M CaCl2
- Carbon and nitrogen:
  - C_CONC_LOI: carbon concentration from LOI (g/kg)
  - C_STOCK_LOI: carbon stock from LOI (t/ha)
  - N_PERCENT: nitrogen percentage
  - N_STOCK: nitrogen stock (t/ha)
- LOI and moisture:
  - LOI: percentage loss on ignition (Colorado method; 1978 consistency)
  - MOISTURE: moisture content
- Other soil properties:
  - BULK_DENSITY: bulk density (g/cm3)
  - PO4_OLSEN: Olsen phosphorus (mg/kg)
- Classification and location:
  - LC07 / LC07_NUM: ITE Land Class 2007
  - COUNTRY, COUNTY07: geographic identifiers
  - EZ_DESC_07: Countryside Survey environmental zone description

## Measurement protocols and quality control

- pH in water:
  - 10 g soil with 25 ml deionised water; measure after 30 minutes; temperature consistency with buffers; electrode rinsed between measurements
  - QC: batch calibration checks using pH 4 and pH 7 buffers; replicate analyses; standard/ certified reference soil per batch
- LOI (loss on ignition):
  - Up to 3145 cores; 10 g sub-sample dried at 105°C, weighed, combusted at 375°C for 16 hours
  - Method aligned with CEH Lancaster SOP3102; data reanalysed to maintain consistency with CS2000 and 1978 methods
  - QC: standard material and duplicate analyses within batches; cross-lab/ method comparisons as needed
- Bulk density:
  - Derived from LOI protocol material; exact core dimensions recorded; stone density measured to adjust topsoil BD
  - ISO 11272:1998 not strictly applied; internal QC via plausibility checks and year-to-year comparisons
- Olsen-P:
  - Up to 1280 samples; 5 g soil extracted with 100 ml 0.5M NaHCO3 (pH 8.5); colorimetric molybdenum blue analysis
  - QC: replicate, standard soil, and certified reference soil per batch; temperature and drying effects noted as potential error sources
- Total nitrogen (N):
  - Up to 1280 samples; elemental analysis using CEH Lancaster Vario-EL; auto-analyzer setup with calibration via acetanilide standard
  - QC: two in-house reference materials per batch
- Quality assurance:
  - Defra/NERC/BBSRC Joint Codes of Practice followed; cross-checks and re-analyses where needed

## Sampling design and data collection

- Sampling strategy:
  - Stratified GB-wide sampling by Land Classes to capture environmental gradients
  - 591 sample squares (1km × 1km): 289 England, 107 Wales, 195 Scotland
  - Each square typically contains five plots; soil collected from top 0–15 cm near main plot corners
- Power and scope:
  - Power analyses ensured sufficient sample size to report major measurements with required confidence
  - Some analytes with tighter resources used reduced sample numbers while maintaining confidence
- Processing and QA:
  - Field and lab protocols provided; standard samples and blind replicates included; cross-checks when methods changed
  - Methods cross-validated against CS2000 and earlier CS methods; results documented in Soils Manual and CS Technical Reports

## Data usage, attribution and rights

- Acknowledgement requirements:
  - All CS data must be acknowledged as Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Include Countryside Survey © / database rights where applicable
- Documentation:
  - Methods, QC procedures, archiving, and data manipulation detailed in Countryside Survey: Soils Manual (CS Technical Report No. 3/07) and related technical reports

## References and documentation

- Emmett et al. (2008) Countryside Survey: Soils Manual; CS Technical Report No. 3/07
- Emmett et al. (2010) Countryside Survey: Soils Report from 2007
- Emmett et al. (2010) Countryside Survey UK Results from 2007
- Bunce et al. (1996, 1981, 2007) ITE Land Classification of Great Britain
- Additional methodological references on soil analysis and QA/QC