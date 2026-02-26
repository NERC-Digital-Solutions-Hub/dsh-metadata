# LOCATE Part 2 (ICP-MS) river dataset

- Multidisciplinary LOCATE project (NERC) combining National Oceanography Centre, British Geological Survey, UK Centre for Ecology and Hydrology, Plymouth Marine Laboratory, with university partners and the Environment Agency.
- Objective: understand flow of carbon from land into the ocean; Part 2 provides river water cation data to complement Part 1 (which covers river water parameters) and accompanying estuary datasets; Part 1 data and estuary companion data are available via EIDC/BODC.
- Part 2 scope: results of ICP-MS analyses for river samples collected concurrently with Part 1 samples; monthly sampling of 41 rivers across England, Scotland, and Wales in 2017 (plus additional November 2016 sampling as a trial).

## What is in the dataset

- Contains major and trace element concentrations from river waters (ICP-MS).
- Data cover 61 columns with element concentrations (Calcium, Magnesium, Sodium, Potassium, Phosphorus, Sulphur, Silicon, SiO2, Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, V, Cr, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, La, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Yb, Tm, Lu, Hf, Ta, W, Tl, Pb, Bi, Th, U) with units (mg/L or μg/L) and associated detection limits.
- Includes sample identifiers (LIMS code), river name, and sampling month.
- Data format notes: two detection limit values per element (batch DL and method DL); when concentrations are below DL, reported as < DL.
- Data are organized in a CSV file with 61 columns describing sample metadata and element concentrations.

## Sampling design and regime

- Fixed-site monthly sampling across 41 rivers in 2017; some sites excepted due to weather; Dorset Stour (DSTO) first sampled in April 2017; November 2016 included as a trial run for some sites.
- Coordination and logistics mainly handled by the British Geological Survey (Andy Tye).
- Sampling window: each month, most sites were visited within a 2–3 day period; a few exceptions due to access/weather.
- Sampling sites were aligned with HMS sites for easier data integration.

## River sampling procedure

- Field processing majority of filtering and bottle preparation; POC samples filtered in the lab after return.
- All samples kept dark and in coolers/freezers; field measurements recorded for salinity, electrical conductivity (SEC), and temperature where possible.
- Water collected from ~0–30 cm depth in mid-channel when feasible; representative of main river body.
- Sampling vessels rinsed, bottles filled, and COLLECTING vessel rinsed with sample water three times.
- SEC, temperature measurements recorded in the field; temperature recorded to 0.1°C precision.
- Isotope samples filtered and handled separately; isotopes collected in 20 mL glass vials.
- Samples transported in cool boxes or freezers to institute; acidified in the lab to 1% HNO3 for ICP-MS analysis; blanks prepared by acidifying MQ water with 1% HNO3.

## ICP-MS analyses and QC

- Instrument: Agilent 8900 ICP-QQQ; method Ag_2.3.21 for major and trace elements in aqueous samples.
- Sample type for ICP-MS: 0.45 μm filtered water acidified to 1% HNO3; post-receipt, 0.5% v/v HCl added to all F/A samples.
- Detection limits: two DL entries per element (batch DL and method DL); method DL based on 4.65σ of 20 typical between-run blanks for the BGS method.
- Quality control: UKAS accredited laboratory (ISO/IEC 17025:2017, lab number 1816); QC run every 20 samples with three calibration blocks per run; use of multi-element standards and certified element standards.
- Data handling notes: below DL treated as analytically indistinguishable from noise; concentrations reported as < DL accordingly.

## Data structure and contents

- Data file format: CSV with 61 columns, including sample metadata (LIMS code, River, Month) and concentrations for 61 element-related columns.
- Units are element-specific (mg/L or μg/L) with explicit detection limit information.
- The dataset is designed to support analyses of geographical and seasonal variation in cations across Great Britain.

## How this data can support analysis

- Enables examination of spatial (river/region) and temporal (monthly) patterns in major and trace element concentrations.
- Can be integrated with Part 1 river water parameter data to explore linkages between elemental composition and carbon flow from land to rivers and ultimately to the ocean.
- Suitable for correlations with land-use types across catchments, hydrological conditions, and seasonal factors.
- Helps assess data quality and measurement uncertainty via documented QC procedures, DLs, and UKAS accreditation.

## Related data and accessibility

- Part 1 dataset (river water parameters) and companion estuary datasets exist and can be accessed through the EIDC and BODC.
- The LOCATE project coordinates data collection across multiple institutions to support comprehensive analyses of land-to-sea carbon and associated chemical dynamics.