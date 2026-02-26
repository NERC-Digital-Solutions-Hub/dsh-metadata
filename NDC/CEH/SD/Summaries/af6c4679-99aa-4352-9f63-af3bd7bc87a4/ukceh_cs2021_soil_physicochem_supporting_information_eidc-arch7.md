# UKCEH Countryside Survey QA metadata and analysis report 2021 - EIDC Topsoil physico-chemical data 2021

## Overview and purpose
- Describes QA metadata and analysis for UKCEH Countryside Survey topsoil physico-chemical data (2021).
- Documents sampling design, laboratory protocols, data processing, QA workflows, and dataset structure to support map-based data products for GIS applications.
- Aids understanding of soil condition and change (topsoil 0–15 cm) across GB for policy, planning, and public-facing maps.

## Survey design and geographic scope
- Rolling survey program adopted in 2019 to monitor soil and vegetation change on a five-year cycle or after 500 squares completed.
- 1-km × 1-km squares used as the primary spatial unit; 500 squares sampled per five-year cycle, with 100 squares visited each year.
- Squares selected within strata defined by the Land Classification of Great Britain (ITE LC07) to enable national and sub-national indicators.
- Exclusion criteria: any square with >75% urban land or >90% sea excluded.
- 2020 Covid disruption: restrictions in the first part of 2020; 50 squares reselected from England for the latter part of the year.

## Sampling design and field collection (topsoil)
- In each selected 1-km square, topsoil samples collected from up to five predefined random locations aligned with vegetation X-Plots.
- Soil cores: 15 cm long, collected from the top 0–15 cm at each sampling location; cores stored and transported to UKCEH laboratories.
- Historical protocol notes: sampling locations and relocation markers have been updated across survey years (1978, 1990, 1998, 2007, 2018/2019, 2020/2021) to maintain comparability.

## Metrics, laboratory protocols, and analytical methods
- Core soil metrics measured on bulk soil or fine earth (FE) fractions; key metrics include:
  - Soil pH in deionised water (PH)
  - Loss-on-Ignition (LOI) and derived soil carbon metrics (C_CONC_LOI, C_STOCK_LOI)
  - Soil carbon stocks calculated per hectare (C_STOCK_LOI)
  - Soil organic matter and LOI-related derivations
  - Bulk density (BULK_DENSITY)
  - Moisture content (MOISTURE, MOISTURE_DRY)
  - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils
  - Total nitrogen (N_PERCENT, N_STOCK)
  - Soil group classifications (SOIL_GROUP)
- LOI and carbon calculations use established equations and standard reference values; conversions and units explained (e.g., depth, area, bulk density, carbon conversion factors).
- Units and conversions specifically documented (e.g., LOI as g/100 g, C_CONC_LOI in g C/kg, N_STOCK in t N/ha, etc.).

## Quality control and QA procedures
- Field and lab QA integrated into a formal workflow using R-based data processing and guidance documents.
- In-lab QA for pH: internal standards and duplicate checks; acceptance within ±2 standard deviations.
- LOI QA: use of internal standards and calcite blanks; batches re-run if QC criteria fail.
- Olsen-P and N analyses include replicates, blanks, and calibration checks; results corrected for moisture and QC references.
- Data processing emphasizes traceability from field collection to laboratory results and dataset assembly.

## Data structure and metadata
- The topsoil dataset (2021) comprises 18 data columns and 496 rows; missing values denoted by -9999.
- Key fields include:
  - SQUARE: 1-km square identifier (text)
  - PLOT: plot/soil sampling location identifier within square (numeric)
  - YEAR: survey year (numeric)
  - PH: soil pH in water (numeric)
  - LOI: loss-on-ignition (% or g per 100 g as applicable) and related LOI metrics
  - C_CONC_LOI: soil carbon concentration (g C per kg oven-dry soil)
  - C_STOCK_LOI: soil carbon stock (t C per ha)
  - N_PERCENT: total soil nitrogen percentage
  - N_STOCK: nitrogen stock (t N per ha)
  - PO4_OLSEN: Olsen phosphorus (mg/kg)
  - BULK_DENSITY: dry bulk density (g cm-3)
  - MOISTURE, MOISTURE_DRY: gravimetric water content (wet and dry basis)
  - LC07, LC07_NUM: ITE Land Classification code and description (for stratification)
  - COUNTRY: GB country (England, Scotland, Wales)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
  - SOIL_GROUP: soil carbon group category based on LOI/organic matter content
- Additional context fields reference long-standing Land Classification and Environmental Zone frameworks used to harmonize and interpret results across GB.

## Data access, products, and GIS relevance
- Data are organized to support map-based visualization across 1-km squares, enabling spatial depiction of soil condition indicators (pH, carbon, nitrogen, phosphorus, moisture, density, etc.).
- Environmental Zones and Land Classification provide a framework to stratify and map soil properties by environmental context.
- Data are suitable for integration into GIS workflows to monitor changes over time and assess interactions between soil conditions and vegetation, climate, and land-use pressures.
- Data are stored and accessible via UKCEH data repositories and the UKCEH Soil Bank; references and contact details provided for access and support.

## References and further reading
- Extensive references covering soils methods, land classification systems, related Countryside Survey reports, QA protocols, and methodological guidance.
- Key sources include Emmett et al. 2008, 2010; Bunce et al. 2007; Reynolds et al. 2013; Keith et al. 2020; and related UKCEH technical reports and datasets.