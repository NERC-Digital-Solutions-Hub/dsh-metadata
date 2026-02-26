# ReadMe file for SpringN2OData.csv

- Purpose: Document the N2O emission data from control, artificial urine, and real urine treatments in a randomised block experiment, including high-frequency automated measurements and later monthly manual measurements.
- Location: Henfaes Research Station, Abergwyngregyn, North Wales; 270 m above sea level; coordinates 53°13'N, 4°0'W.
- Experimental design: Randomised block; plots/chambers with defined geometries and treatments.

## Location and Experimental Setup
- Treatments: Control, ArtUrine (artificial urine), Urine (real urine).
- Chamber geometry: Automated chamber base area 0.25 m2; dimensions 50 cm x 50 cm x 15 cm.
- Manual chamber geometry (later period): 40 cm x 20 cm x 20 cm.
  
## Data Collection Methods
- Automated gas monitoring system: QA/QC with SRI 8610 GC; calibration after every fourth gas sample; data from Queensland University of Technology.
- High-frequency period: Eight N2O flux measurements per chamber per day (1 h closure; four gas samples per closure).
- Manual period: Monthly flux measurements from smaller chambers; GC: Perkin Elmer 580 with Turbo Matrix 110 autosampler; four gas standards used.
- Data type: Quality-assessed flux data (not raw gas concentrations).

## Data Content and Structure
- Timestamp format: dd/mm/yy hh:mm.
- Flux data: Columns B–M represent N2O fluxes in micrograms N2O-N m-2 h-1.
- Headers indicate treatment and chamber/plot numbers (labels: Control, ArtUrine, Urine).

## Quality Assurance and Data Cleaning
- Inspection of raw data files and GC chromatograms for anomalies; problematic data removed.
- Fluxes below detection limit in manual data replaced with zero.

## Temporal Coverage
- Spring 2016; includes a period of high-frequency automated measurements followed by a period of monthly manual measurements.

## GIS and Spatial Considerations
- Spatial context is at the plot/chamber level within a field site; no plot-level coordinates are provided in the ReadMe.
- To map spatial emissions, additional metadata linking plot/chamber IDs to geographic locations would be required.

## Attribution and Usage
- Authors must be acknowledged if data are reused or reproduced.