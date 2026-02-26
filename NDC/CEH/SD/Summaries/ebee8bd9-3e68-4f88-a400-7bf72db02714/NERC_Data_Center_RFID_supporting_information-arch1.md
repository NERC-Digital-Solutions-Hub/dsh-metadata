# Supporting information for: Movement of songbirds between supplementary feeders in urban neighbourhoods in Southern England, UK

- Purpose of the dataset: Provides detailed RFID-based visit records for songbirds at supplementary feeders in urban neighbourhoods, enabling analysis of movement patterns between feeders and relationships with urban form.

- Study scope
  - Location: Three towns in Southern England, UK
  - Timeframe: 1 July 2013 – 31 August 2014 (14 months; setup period first two months; main data collection in the following 12 months)
  - Species: Seven garden bird species; blue tit and great tit were the most abundant
  - Data collection design: 17 RFID feeding stations per network, total of 51 feeding stations installed across private gardens

- Datasets included
  - NERC_Data_Centre_RFID_raw_data.txt
    - Contents: tag (unique PIT tag number), feeder site, garden, and the time/date of each visit
  - NERC_Data_Centre_ringing_data.txt
    - Contents: ringing subsite, date of capture, age (BTO aging system), sex/gender
  - NERC_Data_Centre_Coordinates.txt
    - Contents: coordinates showing relative positions of each feeder and ringing site
  - Access and reuse notes: Full details available at the provided DOIs; cite Cox, D.T.C.; Gaston, K.J. (2018) for dataset reference

- Data collection and hardware setup
  - RFID feeders: Integrated RFID reader and antenna mounted under a single feeder perch
  - Antenna specs: Rectangular antennas (~40 mm × ~32 mm) recording at 125 kHz
  - Recording protocol: Data loggers alternated 400 ms recording / 400 ms pause; time/date and tag ID logged to a 4 GB memory card
  - Power: 12 V battery, 24/7 operation
  - Station setup: Each feeder network had 17 stations; stations spaced approximately 81 m from each other on average
  - Installation: Feeders placed ~0.5 m from cover; residents supplied and maintained; feeder positions influenced by residents; setup occurred up to six weeks before data collection began
  - Maintenance: A researcher visited all stations every 30 days to replace batteries and download data

- Sampling and tagging details
  - Bird handling: Two garden species commonly visiting feeders (blue tit and great tit) were captured using mist nets and tape lures
  - Tagging: Birds fitted with BTO metal rings and implanted PIT tags (8 mm ring)
  - Capture locations: Two sites per network (private green spaces), chosen to maximize catching rates; nearest RFID feeding station ~15 m from capture location

- Data structure and contents
  - RFID raw data file: tag, site, garden, timestamp
  - Ringing data: age, sex, subsite of capture, capture date
  - Coordinates file: spatial relationships between feeders and ringing sites

- Analytical potential
  - Movement and visitation analyses: Link RFID visits with individual birds and spatial layout to model movement between feeders
  - Urban form associations: Examine how feeder-to-feeder movement relates to urban structure and garden networks (context of the main study)
  - Species-specific patterns: Compare visitation rates and movement tendencies across the seven species
  - Temporal patterns: Explore seasonal or monthly variation in feeder visitation

- Data quality and limitations
  - Local-scale data: High-resolution, location-specific data limited to feeder networks within private gardens
  - Accessibility: Data originate from private properties; spatial coverage constrained by resident participation
  - Detection limitations: Records only capture visits to monitored feeders; movements outside the RFID network are not observed
  - Maintenance and gaps: Battery changes and data downloads introduce potential short gaps; researchers performed regular maintenance to mitigate data loss
  - Integration challenges: Data come from multiple sources (RFID visits, ringing data, coordinates), requiring careful alignment and metadata management

- Key references
  - Dataset citation: Cox, D.T.C.; Gaston, K.J. (2018). Movement of songbirds between supplementary feeders in urban neighbourhoods in Southern England, UK. NERC Environmental Information Data Centre. https://doi.org/10.5285/ebee8bd9-3e68-4f88-a400-7bf72db02714
  - Related analysis: Cox, D.T.C.; Inger, R.; Hancock, S.; Anderson, K.; Gaston, K.J. (2016). Movement of feeder-using songbirds: the influence of urban form. Scientific Reports. 6:37669. https://doi.org/10.1038/srep37669

- Usage guidance for analysts
  - Data provenance: Datasets are accompanied by metadata and alignment with the main study on urban form effects on movement
  - Reproducibility: Refer to the DOIs for full dataset details and the associated publication for methodological context
  - Cautions: Consider private-garden sampling biases, observer maintenance intervals, and the limited observation window to interpret movement patterns accurately