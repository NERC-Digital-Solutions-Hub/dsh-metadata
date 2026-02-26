# Brief description of methods

- Overview
  - Two plant species, Leontodon hispidus (Rough Hawkbit) and Succisa pratensis (Devil's-bit Scabious), were grown from plug plants in April 2016 at Abergwyngregyn, North Wales, UK (soil Orthic Podzol, pH 5; latitude 53.2389, longitude -4.0185).
  - Plants were arranged in 1 m blocks within nine Free Air Ozone Enrichment (FAOE) rings (4 m diameter) and exposed to three ozone treatments (Low, Medium, High) over three growing seasons, with and without nitrogen in year one.
  - Natural irrigation; growth and physiological responses recorded (leaf ground cover, leaf litter, flowering, chlorophyll index, photosynthesis, stomatal conductance).

- Experimental design
  - Latin square layout with species alternating within 1 m blocks inside each FAOE ring.
  - Nine FAOE rings configured to provide ozone treatments: Low, Medium, High assigned across rings (e.g., A1/B2/C3 Low; A3/B1/C2 Medium; A2/B3/C1 High).
  - Nitrogen added to one block at 40 kg N ha-1 yr-1 during the first year.

- Treatments and measurements
  - Ozone treatments: Low (~24 ppb), Medium (~40 ppb), High (~57 ppb).
  - Nitrogen treatment: Yes (40 kg N ha-1 yr-1) or No.
  - Measurements recorded:
    - Asat: Light-saturated photosynthesis (µmol CO2 m-2 s-1).
    - gs: Stomatal conductance (mmol H2O m-2 s-1).
    - Chlorophyll index.
    - Flower stems count.
    - Leaf ground cover, leaf litter, frost damage, and purple leaf damage.

- Data collection facilities and protocols
  - Photosynthesis and stomatal conductance measured with LI-COR 6400XT under mean chamber conditions: temp ~20°C, CO2 ~400 µmol mol-1, light ~1500 µmol m-2 s-1, RH 60–80%, leaf VPD 0.8–1.2 kPa.
  - Chlorophyll index measured with Opti-Sciences CCM200.
  - Ozone concentrations monitored with a calibrated Thermo 49i ozone analyser.
  - Quality checks included LI-COR pre-measurement controls and checks for chamber leaks, CO2, and H2O concentrations; data visually inspected for outliers.

- Data files and schema
  - Five CSV data files:
    - Asat_gs.csv: Date, Ring, Nitrogen, Ozone, Species, Asat, gs.
    - Chlorophyll.csv: Date, Ring, Nitrogen, Ozone, Species, Chl.
    - FlowerStems.csv: Date, Ring, Nitrogen, Ozone, Species, No_FlowerStems.
    - LeafCover.csv: Ring, Nitrogen, Ozone, Species, Cover, PurpleCover, FrostDamage (NA where not applicable).
    - WeightLitter.csv: Month, Year, Ring, Nitrogen, Ozone, Species, Litter.
  - Column descriptions indicate the treatment levels (Low/Medium/High), N addition status, and species identifiers; missing data indicated as NA where appropriate.
  - Data collection dates and monthly measurements span from 2016 to early 2017, with measurements tied to specific treatment rings and species.

- Quality control and data validation
  - Ozone levels continuously monitored with a calibrated analyser.
  - Pre-measurement checks for chamber conditions (temperature, light, pressure, flow rate) and verification of CO2 and H2O concentrations.
  - Data were graphically screened for outliers and unusual values to ensure consistency.

- Data governance and stewardship notes
  - Data are organized by clearly labeled CSV files with explicit metadata in column headings, enabling discoverability and interpretability.
  - Standard units and measurement conditions are documented (e.g., ppb for ozone, µmol CO2 m-2 s-1 for Asat, etc.).
  - NA values are used to denote missing measurements (e.g., frost damage for Leontodon).
  - Data are suitable for integration into broader datasets focusing on plant responses to ozone and nitrogen under controlled field-like conditions; provenance and measurement methods are described to support reproducibility and re-use.
  - Considerations for data management include maintaining the ring and treatment mapping, ensuring consistent lag between measurements and treatments, and documenting any data gaps or instrument calibration events if updating the dataset.