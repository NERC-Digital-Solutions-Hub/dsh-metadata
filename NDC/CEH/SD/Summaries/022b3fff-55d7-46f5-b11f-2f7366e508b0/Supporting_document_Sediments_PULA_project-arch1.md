# A brief description/overview of the data being described

- The PULA sediments characterization data folder contains 14 files presenting sedimentological and geochemical analyses for 7 cores from the Notwane Reservoir.
- Core identifiers: 1, 3, 7, 8, 9, 10, 11; collection dates include 22-Nov-2017 and 19-Feb-2018; coordinates provided for each core location (latitude and longitude in decimal degrees).
- Core lengths range from 35 cm to 85 cm; sampling sites were along shore or from a small boat.

## Sampling techniques

- Seven sediment cores collected with a push corer (50 mm diameter PVC) using extension rods from shore or a small boat.
- Cores stored at 4 °C to retain water content; split in half, photographed, and sub-sampled for grain size and geochemical analyses.

## Analytical techniques

- Grain size: a Malvern Mastersizer 3000 laser diffraction particle size analyzer was used; grain-size distributions are provided as D50 per subsample.
- Organic matter (OM): determined by loss on ignition (LOI) after calcination; detailed drying and heating steps implemented (105 °C drying, 550 °C calcination).
- Trace metals: 95 sediment samples analyzed for Fe, Zn, Cu, Cr, Pb using a 65% HNO3 digestion and Microwave Plasma-Atomic Emission Spectrometry (MP-AES) after filtration to <0.45 µm and dilution to 50 mL.
  - Reported average standard deviations (Fe 1.81% RSD, Zn 4.02% RSD, Cu 1.43% RSD, Cr 0.82% RSD, Pb 1.72% RSD).
  - Detection limits: Cr 0.8 µg/kg, Fe 1.7 µg/kg, Cu 0.5 µg/kg, Zn 28 µg/kg, Pb 2.5 µg/kg (as weights of dry sediment).

## Data structure and content

- The dataset comprises 7 spreadsheets named Core_*_Grain_size_details.csv:
  - Contain grain size measurements at different depths (in cm) for each core.
  - Report Dv(10), Dv(50), Dv(90) in µm for each of the 3 measurements, plus average values.
- A second set of 7 spreadsheets named Core_*_Grain_size_avg_and_metals.csv:
  - Column 1: core sequential number.
  - Column 2: depth from the sediment–water interface (0 cm).
  - Column 3: average Dv(50) grain size (µm) for the interval.
  - Column 4: Organic Matter content (OM %) for the interval.
  - Columns 5–9: Fe, Cu, Pb, Cr, Zn concentrations (µg/kg).
- Blanks indicate data below detection limits or missing results.

## Data quality and notes

- Some cells are blank due to measurements below detection limits or data loss.
- The data allow analysis of relationships between grain size, organic matter, and trace metal concentrations across depths and cores.