# Movement of songbirds between supplementary feeders in urban neighbourhoods in Southern England, UK

## Overview
- dataset contains time, date, and location of visits by songbirds fitted with PIT tags to RFID-equipped feeders.
- seven species studied; Blue tits and Great tits were the most abundantly caught.
- data collected in three towns in Southern England over 14 months (1 July 2013 – 31 August 2014); initial two months as setup period, followed by 12 months of main data collection.
- aim is to support analysis of movement between supplementary feeders using map-based data representations.

## Data products / contents
- Three data files:
  - NERC_Data_Centre_RFID_raw_data.txt: unique tag number (bird), feeder site and garden, plus time and date of each visit.
  - NERC_Data_Centre_ringing_data.txt: ringing information per tag number (capture subsite, capture date, age, sex, gender of species).
  - NERC_Data_Centre_Coordinates.txt: coordinates showing relative positions of each feeder and ringing site (available in supporting documentation).

## Methodology
- RFID feeders built with Arduino components; rectangular antennas recording at 125 kHz, fixed under a perch; other perches sealed to ensure complete visit recording.
- Data loggers recorded in 400 ms on / 400 ms off cycles, capturing time, date, and tag ID to a 4 GB memory card; powered continuously by 12 V battery.
- Network design: 17 RFID feeding stations per network; stations placed in private gardens averaging 81 m apart (±20 m); feeders ~0.5 m from cover; gardens chosen with resident involvement; setup completed ~6 weeks before data collection.
- All stations included feeder, RFID reader, antenna, power source, stand, and squirrel baffle; feeder bottom ~1 m above ground.
- Maintenance: researchers visited every 30 days to replace batteries and download data.
- Operation window: 51 feeding stations operational from 1 September 2013 to 31 August 2014.
- Bird capture and tagging: two garden locations per network used for mist-netting; birds fitted with BTO metal rings and PIT tags (in an 8 mm plastic ring) after catching.
- Principal investigator: Dr Daniel T. C. Cox; analysis and conclusions published in Cox et al. (2016).

## Access and reuse
- Cite as: Cox, D.T.C.; Gaston, K.J. (2018). Movement of songbirds between supplementary feeders in urban neighbourhoods in Southern England, UK. NERC Environmental Information Data Centre. https://doi.org/10.5285/ebee8bd9-3e68-4f88-a400-7bf72db02714
- Full details available at https://doi.org/10.5285/ebee8bd9-3e68-4f88-a400-7bf72db02714

## References
- Cox, D.T.C.; Inger, R.; Hancock, S.; Anderson, K.; Gaston, K.J. (2016). Movement of feeder-using songbirds: the influence of urban form. Scientific Reports. 6:37669. https://doi.org/10.1038/srep37669