# Brief description of methods

- Location and context
  - North Wales, UK: Abergwyngregyn, with soil classified as Orthic Podzol, pH 5.
  - Coordinates: Latitude 53.2389, Longitude -4.0185.
  - Plants: Leontodon hispidus (Rough Hawkbit) and Succisa pratensis (Devil's-bit Scabious) grown from plug plants in April 2016.

- Experimental design
  - Nine Free Air Ozone Enrichment (FAOE) rings, each 4 m in diameter.
  - Within-ring layout: 1 m square blocks arranged in a Latin square design; two species grown in alternating blocks.
  - Rings and blocks used to apply ozone treatments and nitrogen (N) additions.
  - Ozone treatments assigned to rings as follows: Low (A1, B2, C3), Medium (A3, B1, C2), High (A2, B3, C1) to achieve mean ring concentrations of 24 ppb, 40 ppb, and 57 ppb, respectively.
  - Nitrogen: One block per ring received N at 40 kg N ha-1 yr-1 during the first year; irrigation was natural (no extra watering besides N addition).

- Measurements and data collection
  - Growth and physiological responses recorded: leaf ground cover, leaf litter, flowering, chlorophyll index, photosynthesis (Asat) and stomatal conductance (gs).
  - Instruments: LI-COR 6400XT for Asat and gs; chlorophyll index measured with Opti-Sciences CCM200.
  - Conditions during measurements: mean chamber conditions included ~20°C air temperature, CO2 about 400 µmol mol-1, light about 1500 µmol m-2 s-1, relative humidity 60–80%, leaf VPD 0.8–1.2 kPa.

- Quality control
  - Ozone monitored with calibrated Thermo 49i ozone analyser.
  - LI-COR 6400XT checks for chamber temperature, light, pressure, flow rate, leaks, CO2 and H2O.
  - Data checked graphically for outliers or anomalies.

- Data files and structure
  - Five CSV data files:
    - Asat_gs.csv: Light-saturated photosynthesis (Asat) and stomatal conductance (gs).
      - Key fields: Date, Ring, Nitrogen, Ozone, Species, Asat (µmol CO2 m-2 s-1), gs (mmol H2O m-2 s-1).
      - Measurement conditions: mean chamber ~20°C, CO2 400 µmol mol-1, light 1500 µmol m-2 s-1, humidity 60–80%, VPD 0.8–1.2 kPa.
    - Chlorophyll.csv: Chlorophyll index (Chl).
      - Key fields: Date, Ring, Nitrogen, Ozone, Species, Chl (index value).
      - Chlorophyll index measured with Opti-Sciences CCM200; NA for missing data.
    - FlowerStems.csv: Number of flowering stems.
      - Key fields: Date, Ring, Nitrogen, Ozone, Species, No_FlowerStems.
    - LeafCover.csv: Leaf cover metrics.
      - Key fields: Ring, Nitrogen, Ozone, Species, Cover (percent grid squares with leaves, Oct 2016), PurpleCover (percent damaged leaves, Oct 2016), FrostDamage (percent frost-damaged leaves, Jan 2017).
      - Leaf cover assessed from 100-square grids overlaid on plant block photographs; NA where not observed (e.g., Leontodon had no observed damage).
    - WeightLitter.csv: Dried litter mass.
      - Key fields: Month, Year, Ring, Nitrogen, Ozone, Species, Litter (grams).
      - Litter measured monthly from July 2016 to February 2017 after oven-drying at 60°C.
  - NA indicates missing measurements.

- Spatial and GIS-relevant aspects
  - Rings provide spatial units (4 m diameter) with 1 m blocks inside; arrangement supports spatial mapping of treatment effects.
  - Data can be linked by Ring, Nitrogen, Ozone, and Species for spatio-temporal analysis.
  - Coordinates and ring geometry enable creation of polygon shapefiles representing ring boundaries and 1 m block grids for GIS visualization.

- Practical GIS applications
  - Generate maps of physiological responses (Asat, gs, Chl), phenology (flowering stems), and tissue status (leaf cover, frost damage) by ozone and nitrogen treatments.
  - Analyze treatment interactions over time across space (ring-level and block-level), and compare species responses.
  - Integrate with other geospatial data (soil, climate, atmospheric measurements) to assess spatial drivers of ozone effects.

- Notable limitations and caveats
  - LeafCover data includes NA for Leontodon in October 2016, indicating no observed damage.
  - FrostDamage and some other measurements are time-limited to specific months (e.g., leaf damage Jan 2017; Oct 2016 for leaf cover).
  - The dataset covers a defined experimental window (2016–2017) and is limited to ring/block-scale measurements.