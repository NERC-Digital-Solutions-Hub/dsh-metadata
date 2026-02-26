# Overview

- This dataset details the seasonal abundance of all life stages of the mosquito species Culex pipiens at the Centre for Ecology & Hydrology (CEH) Wallingford site during 2015. Immature stages were monitored March–October 2015 (three times weekly); adult counts were recorded April–October 2015 (four times weekly).

## Experimental design and sampling regime and collection methods

- Immature mosquitoes were tracked using four 450 litre circular water butts placed in close proximity at the Wallingford field site, with varied exposure to sun and shelter.
- Hay infusion: In January, butts were filled with clean water and infused with hay (2 kg per butt) until end-March.
- Temperature monitoring: A HOBO surface water temperature logger recorded hourly temperatures in each butt.
- Immature sampling: Egg rafts were counted at 10 am on Mon/Wed/Fri. A 500 ml dip sample was taken from the north, south, east and west edges of each butt (not from the middle). Larvae and pupae were counted in the field when possible; otherwise photographs of trays were used and later counted on a computer.
- Species identification: Monthly sampling of 4th instar larvae for morphological identification to species level (Becker et al., 2003) in the laboratory after submersion in boiling water.
- Adult sampling: Four John W. Hock Miniature Downdraft Blacklight (UV) traps baited with dry ice were used, operated nightly 17:00–09:00 Apr–Oct (with some nights missed due to logistics). Traps were placed at four locations around the site, and adult females were identified to species in the laboratory (males not recorded).

## Fieldwork and laboratory instrumentation

- Adult sampling instrumentation: UV light traps baited with dry ice.
- Identification: Laboratory microscopy and standard dissection techniques.
- Field locations: Traps placed around the water butt area with reference to a site map (Figure 1 in the original document).

## Nature and units of recorded values

- Egg abundance: counts of egg rafts by butt.
- Larval and pupal abundance: counts per sampling occasion, by butt, with separate counts for 1st/2nd instars (L1/2) and 3rd/4th instars (L3/4) and pupae.
- Adult abundance: counts of adult female Cx. pipiens per trap per sampling occasion (males not recorded; other species recorded when identified).
- Temperature: water temperature in degrees Celsius.

## Quality control

- Larval and pupal counts derived from photos of tray contents; validation performed by comparing direct counts with photo counts on the first two sampling days, with results consistent.

## Details of data structure

- The dataset comprises six CSV spreadsheets:
  - Egg_abundance_2015_Wallingford.csv
  - Larval_abundance_2015_Wallingford.csv
  - Pupal_abundance_2015_Wallingford.csv
  - Adult_abundance_2015_Wallingford.csv
  - Larval_identification_2015_Wallingford.csv
  - Water_temperatures_2015_Wallingford.csv

- Egg_abundance_2015_Wallingford.csv
  - Rows: counts of egg rafts on a given day
  - Columns: Date, Butt n (n = 1–4)

- Larval_and_pupal_abundance_2015_Wallingford.csv
  - Rows: counts on a given day
  - Columns organized by butt (B–BI) with separate sections for larvae and pupae
  - Columns denote location (North/East/South/West corners) and instar stage (L1/2, L3/4) or Pupae

- Adult_abundance_2015_Wallingford.csv
  - Rows: counts of adult females caught per trap on a given date
  - Columns: Date, Location (trap), Cx. pipiens, Cs. annulata, Ae. Geniculatus
  - NA entries indicate missed traps due to staff or supply issues

- Larval_identification_2015_Wallingford.csv
  - Details occurrences of 4th instar larval identifications, counts identified as Cx. pipiens, and associated butt sources

- Water_temperatures_2015_Wallingford.csv
  - hourly water temperature measurements
  - Columns: Date, Time, Butt, Temperature (°C)

- Location and date references
  - Field site coordinates: CEH Wallingford (51˚ 36' 9.0144" N, 1˚ 6' 45.7344" W)
  - Monitoring spanned March–November 2015 for temperature, with biological sampling March–October 2015 (immature) and April–October 2015 (adults)