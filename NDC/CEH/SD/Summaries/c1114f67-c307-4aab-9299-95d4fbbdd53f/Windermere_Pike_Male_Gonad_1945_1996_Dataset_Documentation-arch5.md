# Windermere Pike Male Gonad Weight Data (1945 to 1996)

## Overview
- Dataset of estimated gonad weight and related data for male pike (Esox lucius) from net sampling.
- Data collection started in 1945; originally by the Freshwater Biological Association (FBA), subsequently collected by CEH and its predecessor Institute of Freshwater Ecology (IFE) since 1989.

## Dataset and File Details
- File: Windermere_Pike_Male_Gonad_Data_1945_to_1996.csv
- Format: CSV
- Size: 225 KB
- Columns (sampled fields with units):
  - Individual: Individual number; Units: None
  - Weight: Body weight; Units: g
  - Length: Length at capture; Units: cm
  - Age: Age at capture; Units: Years
  - Year: Year of capture; Units: Calendar year
  - Temp: Annual average water surface temperature; Units: °C
  - GSI: Gonadosomatic Index; Units: None
  - Gonad: Estimated gonad weight; Units: g
  - Description fields provide descriptive text for each column
- Sampling site: Windermere lake, Cumbria, Great Britain
  - Approximate grid reference: SD393960
  - OSGB36 Easting/Northing: 339385, 496080
  - WGS84 coordinates: 54.360193, -2.935836
- Species measured: Esox lucius (Pike)

## Experimental Design and Sampling Regime
- Pike monitored in the north and south basins via gill netting with site and effort variations from 1944 to present.
- Standardization since 1982:
  - Net type: 64 mm bar mesh multifilament gill nets
  - Net configuration: 40 m length, 3 m depth; set on the bottom
  - Timing: mid-Oct to late-Dec; 10 sites per basin
  - Procedure: five nets deployed at a site, inspected on a fixed schedule (Monday deployment, Wednesday catch removal, Friday lifting)
  - Coverage: sites rotated to sample the whole lake; each site fished for two weeks per season
- Annual sampling effort:
  - 1982–1989: ~348 net days total, roughly equally split between basins
  - 1990 onwards: ~240 net days total, roughly equally split between basins
- Earlier methods (pre-1982) used larger-mesh nets and less standardized protocols

## Collection Methods and Laboratory Analysis
- Lab processing:
  - Each pike measured (fork length to 1 mm) and weighed (wet weight to 100 g)
  - Sex determined via dissection
  - Left opercular bone aged; birth date nominally 1 April
- Gonad weight estimation:
  - Simple linear function: gonad weight estimated between 2% (lightest) and 4% (heaviest) of body weight, based on Craig (1996)

## Quality Control and Provenance
- Quality control:
  - Measurements checked by permutations of three individuals to ensure accuracy
- Provenance and documentation:
  - Data originally collected by FBA; later by CEH and IFE
  - Methodological references cited for age determination and gonad estimation
  - Metadata include precise location (grid coordinates and coordinate systems), timing, and sampling details

## Data Columns and Metadata
- Key fields include:
  - Individual (ID), Description fields (descriptions for each column), Weight (g), Length (cm), Age (years), Year, Temp (°C), GSI, Gonad (g)
- Units are specified for quantitative fields to support reproducibility and interoperability

## Rights, Access, and Usage Notes
- Copyright: © NERC - Centre for Ecology & Hydrology / Freshwater Biological Association (FBA)
- Document version: 1.0 (dated 4-6-2018)
- Users should reference the dataset and acknowledge custodianship (FBA and CEH) when using the data
- Data comprise historical records (1945–1996) with standardized methodology since 1982; interpret results with consideration of methodological changes over time

## Practical Considerations for Data Stewards
- Ensure ongoing accessibility of the CSV file and preserve metadata for future discoverability
- Maintain clear linkage to original sources and methodological references for aging, length/weight measurements, and gonad estimation
- Monitor potential limitations due to historical sampling biases, changes in netting practices, and gaps in metadata prior to standardization
- Preserve location metadata (grid references and coordinate systems) for spatial traceability
- Facilitate data updates and potential revalidation or recalibration of gonad weight estimates if needed in future analyses