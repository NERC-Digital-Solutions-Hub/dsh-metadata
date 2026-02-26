# Brief description of the dataset

## Origin, site, and sampling
- Chemistry dataset produced by CEH Dorset between 2004 and 2006.
- Sampling and analysis conducted by Mike Bowes.
- Location: River Frome at East Stoke, Dorset (National Grid Reference SY 867868), near the CEH River Laboratory.
- Sampling method: Epic water samplers at the gauging weir; occasional manual dip-sampler samples during storm events.

## Analytes and measurements
- Total phosphorus (TP): includes both dissolved and acid-extractable particulate phosphorus in unfiltered samples.
- Suspended sediment concentration (SSC): mass of solids retained on Whatman GF/C filter per liter of river water.
- Soluble reactive phosphorus (SRP): filterable reactive phosphorus, measured in 0.45 μm filtered samples.
- Dissolved oxidisable nitrogen (TON): total dissolved nitrogen present as nitrate and nitrite (nitrate dominates in river waters).
- Dissolved reactive silicon (Si): molybdate-reactive silicon in 0.45 μm filtered samples.
- Notes: Dissolved reactive silicon and soluble reactive phosphorus are determined from 0.45 μm filtered water; TP combines dissolved and acid-extractable particulate fractions.

## Analytical methods
- Primary method: colorimetric analysis using a Seal AQ2 discrete analyzer.
- TP determination: digestion with acidic potassium persulphate in an autoclave at 121°C, reaction with acidic ammonium molybdate to form a molybdenum-phosphorus complex; measured colorimetrically at 880 nm.
- Other determinands: standard spectrophotometric methods (DoE 1981, 1993; Murphy & Riley, 1962).
- Sample preparation: 0.45 μm filtration prior to SRP, TON, and Si analyses.
- Quality control: QC standards analysed alongside each batch.

## Data format and definitions
- Date/time format: day/month/year hours:minutes.
- TP: includes both dissolved and acid-extractable particulate phosphorus.
- TON: interpreted as total dissolved nitrogen in nitrate/nitrite form (nitrate dominates in river waters).
- SRP: also known as filterable reactive phosphorus; determined from 0.45 μm filtered water.
- Si: dissolved reactive silicon (molybdate-reactive) after 0.45 μm filtration.

## Context and references
- Data linked to high-resolution nutrient monitoring: Bowes MJ, Smith JT, Neal C. The value of high resolution nutrient monitoring: a case study of the River Frome, Dorset, UK. Journal of Hydrology 2009; 378:82-96.

## GIS-related considerations and potential uses
- Suitable for time-series mapping of nutrient and sediment constituents at a fixed site along the River Frome.
- Variables available for mapping: TP, SRP, TON, dissolved Si, SSC.
- Spatial scope currently single-site; can be enhanced by integrating additional sites or overlapping datasets.
- Ideal for linking with hydrological or rainfall data to explore event-driven nutrient dynamics.
- Important notes for GIS work: data collected 2004–2006; ensure unit consistency and account for older measurement standards; refer to the cited QC practices for data reliability.