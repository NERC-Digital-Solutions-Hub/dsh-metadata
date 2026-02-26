# ReadMe file for SpringN2OData.csv

## Purpose and scope
- Describes data on N2O emissions measured under three treatments: Control, artificial urine (ArtUrine), and real urine (Urine).
- Data originate from an orthic podzol in semi-improved upland grassland at Henfaes Research Station, North Wales, collected in spring 2016.
- Aimed at providing quality-assured, usable flux data for environmental monitoring and related analyses.

## Site, timing, and experimental design
- Location: Henfaes Research Station, Abergwyngregyn, North Wales (270 m above sea level; 53°13'N, 4°0'W).
- Site description: upland grassland on orthic podzol.
- Timeframe: spring 2016.
- Experimental design: randomized block design with plots assigned to Control, ArtUrine, or Urine treatments.

## Data collection methods
- Automated flux measurements:
  - System: automated greenhouse gas monitoring (GC) setup.
  - Instrument: SRI 8610 GC.
  - Frequency: eight N2O flux measurements per chamber per day (1-hour chamber closure; four gas samples per closure).
  - Calibration: standard analysed after every fourth gas sample.
  - Chamber size: 0.25 m2 base area; dimensions 50 cm x 50 cm x 15 cm (l x w x h).
- Manual measurements:
  - After automated period, monthly flux measurements from smaller chambers (40 cm x 20 cm x 20 cm).
  - Analysis: Perkin Elmer 580 GC with Turbo Matrix 110 autosampler.
  - Calibration: four gas standards spanning measured concentration ranges (BOC gases, Liverpool).

## Data content and structure
- Data include high-frequency flux measurements from the automated system and monthly flux measurements from manual sampling.
- The dataset represents quality-assessed flux data (not raw gas concentration data).
- Data headers (example): Timestamp: dd/mm/yy hh:mm.
- Columns B to M: N2O fluxes (in micrograms N2O-N m-2 h-1).
- Treatments and chambers/plots are encoded in the column headers (Control = Control, ArtUrine = artificial urine treatment, Urine = real urine treatment).

## Data processing and quality assurance
- Quality assurance: inspection of raw data files and GC chromatograms for anomalies; removal of anomalies as needed.
- Handling of detection limits: fluxes below the detection limit from manual data replaced with zero.

## Data headers and metadata
- Data headers provide information on treatment and chamber/plot numbers.
- Data represent processed flux values rather than raw gas concentrations.
- Authors must be acknowledged if data are reused or reproduced.

## Usage, access, and attribution
- Users should acknowledge the authors when re-using or reproducing the data.
- Information provided includes measurement methods, instrumentation, calibration, and QA steps to support appropriate use and interpretation.

## Limitations and notes
- The dataset does not include raw gas concentration data; only processed N2O flux measurements.
- Metadata quality and completeness are addressed through described QA procedures, but users may need to refer to the ReadMe for context on units, treatments, and chamber definitions.