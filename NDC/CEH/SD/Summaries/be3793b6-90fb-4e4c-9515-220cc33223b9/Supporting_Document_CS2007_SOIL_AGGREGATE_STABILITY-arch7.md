# Soil aggregate stability data from arable and grassland in Countryside Survey, Great Britain 2007

- Two main data files accompany the Countryside Survey 2007 soil work:
  - Particle_Size_Distribution_data.csv
  - Aggregate_stability_metrics.csv
- Scope: 419 soils sampled across 150 1km squares in Great Britain (England, Scotland, Wales) as part of the 2007 Countryside Survey; methods focus on laser granulometry to quantify PSD and aggregate stability (water-stable vs post-sonication).

## Data files and structures

- Particle_Size_Distribution_data.csv
  - Columns:
    - SQUARE: 1km square sampling site code (text)
    - PLOT: Plot identifier within each square (text)
    - PSIZE: Particle size class (numeric)
    - VOL_WS: Proportional volume for water-stable aggregates (numeric)
    - VOL_SON: Proportional volume after sonication (numeric)

- Aggregate_stability_metrics.csv
  - Columns:
    - SQUARE: 1km square sampling site code (text)
    - PLOT: Plot identifier within each square (text)
    - MWD1: Mean Weight Diameter of water-stable aggregates (numeric)
    - MWD2: Mean Weight Diameter of sonicated aggregates (numeric)
    - DR: Disaggregation Reduction (numeric)
    - LC07: ITE Land Class 2007 description (text)
    - LC07_NUM: Land Class 2007 numeric code (numeric)
    - COUNTRY: Country location (England ENG, Scotland SCO, Wales WAL)
    - COUNTY07: County or Council (text)
    - EZ_DESC_07: Countryside Survey Environmental Zone description (text)
  - Note on DR: DR2000 values are used in this dataset (DR = MWD1 − MWD2). Earlier DR500 values are available in older methods but are not included here. Measurements were not rescaled to <500 µm for this dataset.

## Sampling design and geography

- Countryside Survey framework
  - Great Britain stratified by Land Classes across environmental gradients; 1km × 1km sample squares randomly selected within Land Classes.
  - 591 squares surveyed in 2007; 424 plots selected for soils analysis; 419 plots analyzed for aggregate stability.
  - Spatial scope covers England, Scotland, and Wales with distribution across major geographic units (COUNTRY, COUNTY07).
- Plot selection and sampling
  - Soil samples collected from archived Countryside Survey 2007 samples (air-dried, 2 mm sieved).
  - Sampling targeted specific land cover and AVC classes to ensure representation of arable and grassland environments.
  - Each 1km square contributed up to five plots; 1km square codes used to link to geographic locations.
- Data provenance
  - Ground-truthing and sampling align with the Countryside Survey methodology and soil manual (Carey et al. 2008; Emmett et al. 2010; Emmett et al. 2008).

## Laboratory methods and metrics

- Measurement approach
  - Laser granulometry measures Particle Size Distribution (PSD) of soil aggregates.
  - MWD (Mean Weight Diameter) calculated from PSD for two states:
    - MWD1: Water-stable aggregates (pre-sonication; after circulating water treatment)
    - MWD2: Fundamental particles after sonication
  - Disaggregation Reduction (DR) = MWD1 − MWD2 (DR2000 in this dataset; no <500 µm rescaling)
- Protocol details
  - Larger sample mass used in this dataset (1.8× previous protocol) with longer measurement time (60 seconds) per PSD run.
  - 7-metre circulating-water system added to increase sample mass handling and stability; original 30-second measurement extended to 60 seconds.
  - Pre-wetting and mass estimation steps to optimize PSD obscuration (target initial obscuration 1–3%; final post-sonication obscuration ≤ 30%).
  - Pump speed set to 60 (≈45 ml/s) to prevent large aggregates from settling and biasing PSD.
  - Temperature monitoring of the aqueous vessel; sonication performed at 100 W for five minutes; post-sonication PSD measured again.
- Quality control and assurance
  - Field sampling staff trained; field sampling manual provided.
  - Use of a palaeosol reference material and two standard PSD materials to check instrument accuracy and precision.
  - In cases where obscuration > 30% in post-sonication measurements, tests were repeated with smaller aggregate masses.
  - UK Centre for Ecology & Hydrology maintains ISO 9001:2015 certified Quality Management System; QA policies and procedures documented.

## Data quality and considerations for GIS

- Representativeness and scale
  - Data are collected at the 1km grid scale across Great Britain; suitable for national/regional mapping of soil aggregate stability indicators.
  - Variables include geographic, land-class, and environmental zone descriptors (COUNTRY, COUNTY07, LC07, EZ_DESC_07) to support spatial analyses by landscape context.
- Data limitations
  - Data reflect conditions from 2007 Countryside Survey; temporal relevance depends on use case.
  - Spatial resolution limited to 1km squares; precise point coordinates are represented by square codes rather than exact GPS points.
  - DR values reflect a specific laboratory protocol (DR2000) without rescaling to <500 µm; users should be aware of protocol differences when comparing to other studies or DR500 datasets.
- Practical GIS applications
  - Join capability: SQUARE and PLOT can be linked to a 1km gridded shapefile or map layer to produce map-based visuals of PSD and DR values.
  - Potential outputs:
    - Map of DR (disaggregation reduction) by 1km square or by plot within squares.
    - Spatial layers for MWD1 and MWD2 to illustrate water-stable vs post-sonication aggregate sizes.
    - Attribute tables for COUNTRY, LC07 (Land Class), COUNTRY and EZ_DESC_07 (Environmental Zone) to explore regional patterns.
  - Data provenance and acknowledgment: Use of Countryside Survey data must acknowledge UK Centre for Ecology & Hydrology; data rights and citations per CEH policies.

## Provenance, references, and licensing

- Data origin: Countryside Survey 2007, UK Centre for Ecology & Hydrology (UKCEH)
- Key references for methodology and context:
  - Rawlins et al. (2013, 2015) – laser granulometry method and protocol refinements
  - Carey et al. (2008); Emmett et al. (2010, 2008) – Countryside Survey soils framework and manual
  - Bunce et al. – ITE land classification (LC07)
  - Emphasis on QA, field manuals, and ISO 9001:2015 certification
- Acknowledgement and licensing
  - Data acknowledged as Countryside Survey data owned by UKCEH; copyright and database rights apply; proper acknowledgment required in all uses.