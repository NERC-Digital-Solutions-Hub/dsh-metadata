# Summary

- Location and site
  - Rural site in North Wales, UK; part of Bangor University farm; near the sea
  - Coordinates: 53°14N, 4°01W; elevation 15 m

- Experimental design
  - Eight solardomes with charcoal-filtered air; ozone added according to a weekly, computer-controlled profile (LabView)
  - Four replicate pots per species/cultivar; four plants per pot
  - Three solardomes heated by +7°C to mimic tropical/subtropical conditions; biomass/physiology data available only for these heated domes
  - Ozone exposure at night and day; watering as required; exposure ended at different times per species
  - Species and start/end exposure
    - Sweet Potato Erato orange: 13/06/2019 – 10/10/2019
    - Bean Orca: 13/06/2019 – 10/10/2019
    - Bean Pinto: 13/06/2019 – 01/10/2019
    - Bean Rajama: 18/06/2019 – 01/10/2019
    - Bean Turtle: 13/06/2019 – 01/10/2019

- Treatments
  - Low ozone, heated: peak ~35 ppb
  - Medium ozone, heated: peak ~80 ppb
  - High ozone, heated: peak ~115 ppb

- Data collection and variables
  - Ozone and meteorological data logged hourly automatically
  - Plant physiology data collected ad-hoc (stomatal conductance, soil moisture, chlorophyll content index)
  - Biomass/yield measured at experiment end
  - Stomatal conductance measured with AP4 porometer; soil moisture with theta probe; chlorophyll with CCM-200

- Instrumentation and calibration
  - LabView-controlled ozone exposure system
  - AP4 porometer (calibrated daily)
  - External calibration of ozone analysers
  - CCM-200 autocalibration
  - DO3SE model usage requires constant air pressure, wind speed, and dummy precipitation values

- Data files and structure
  - Biomass_and_Yield_2019.csv: 63 rows, 11 columns (e.g., Plant_Species_and_variety, Treatment, Pot_Number, Pod and Bean metrics, yields)
  - Ozone_and_meteorology_2019.csv: 10008 rows, 11 columns (Treatment, Day_of_Year, Date, Time, Ozone_ppb, meteorological and in-dome measurements; wind speed constant; precipitation dummy value)
  - Plant_Physiology_2019.csv: 692 rows, 12 columns (only for sweet potato; includes physiology readings)
  - Blank cells indicate missing readings

- Data quality, QA and transformations
  - Automated QA on ozone/meteorology data; plausibility checks and gap-filling as needed
  - Plant physiology QA for plausibility; biomass/yield QA for range and outliers
  - Gap-filling protocol for missing data (see below)

- Gap filling protocol
  - Create a complete hourly row for each day; gaps ≤5 hours filled by averaging adjacent values
  - Larger gaps investigated via lab book; fill using previous/next day values for the same time
  - If system was off, fill with a dummy value of 5 ppb
  - Identify and address anomalous values (e.g., negative ozone values set to zero)
  - All changes are tracked in a separate amended file to preserve originals

- Data resource structure and notes
  - Three CSV files with clearly defined column naming and units
  - DO3SE model inputs require constant wind speed and air pressure values; air pressure not measured at site and replaced with a latitude/altitude-appropriate constant
  - Windspeed is constant due to solardome fans; precipitation set to 1 mm/hour to maintain pot field capacity

- Miscellaneous
  - Facility description: CEH Solardomes and ozone field release system (link provided)

- Analytical status
  - No analysis has been performed on these data yet

- Access and references
  - Facility website: https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-fieldrelease-system

- End notes for data users
  - Be aware of missing data points and the applied gap-filling methods
  - Use the separate "filled and corrected" datasets for analysis, preserving the original data
  - Consider DO3SE model requirements when integrating ozone and meteorological data into analyses