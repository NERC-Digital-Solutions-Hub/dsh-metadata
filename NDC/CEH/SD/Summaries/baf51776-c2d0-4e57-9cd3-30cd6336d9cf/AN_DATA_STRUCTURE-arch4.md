# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- The ECN (UK Environmental Change Network) dataset is managed by the ECN Data Centre and is part of a network sponsored by multiple UK government departments and agencies.
- Data are collected from a network of sites and are intended for understanding environmental change.

## Dataset Owners and Governance

- Sponsoring organisations include: Agri-Food and Biosciences Institute, Biotechnology and Biological Sciences Research Council, Cyfoeth Naturiol Cymru - Natural Resources Wales, Defence Science & Technology Laboratory, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, Natural Environment Research Council, Northern Ireland Environment Agency, Scottish Environment Protection Agency, Scottish Government, and Scottish Natural Heritage.
- Users are asked to acknowledge use of the datasets and to send one reprint of any publication citing the data.

## Protocol and Standardization

- ECN maintains standard operating procedures to ensure data comparability across sites.
- An accompanying PDF explains how data are collected.

## Usage Notes

- Passive diffusion tubes measure NO2 concentration over a two-week exposure period.
- Blank tubes are included as a quality check; they are unexposed upon arrival and analyzed with experimental tubes.
- Users should apply accompanying quality information when using the data.

## Data Structure and Download

- Core data fields in downloads:
  - SITECODE: Unique ECN site code
  - SDATE: Sampling date
  - TUBEID: Tube identifier (E = Experimental, B = Blank)
  - FIELDNAME: Variable measured
  - VALUE: Measured value
- Supporting documentation includes:
  - ECN_AN2.csv: Sample collection details (SITECODE, TUBEID, DEPDATE, DEPHOUR, DEPMINS, SDATE, SHOUR, SMINS)
  - ECN_AN_qtext.csv: Site manager quality text linked to quality codes

## Site Codes and Variables Measured

- Explanatory information for sites:
  - T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House - Upper Teesdale, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T11 Snowdon (Y Wyddfa), T12 Cairngorms
  - Each site has precise geographic coordinates provided
- Variables being measured:
  - WEIGHTNO2: Weight of NO2 on mesh (micrograms)
  - NO2: NO2 concentration (micrograms/m3)
  - NO2PPB: NO2 concentration (ppb)
  - TDIFF: Exposure time (minutes)
  - Q1–Q8: Quality codes (integer)

## Quality Codes

- Quality codes cover a wide range of data quality factors from 100 to 999, including:
  - 100: No information available - data lost
  - 101–199: Various operational issues (e.g., no sample, partial loss, equipment issues)
  - 200–299: Adverse conditions affecting sampling/recording (e.g., insects, light)
  - 500–599 and beyond: Laboratory-related issues, contamination, measurement flags
  - 999: Unusual event — see associated quality text
- The ECN_qtext.csv file provides descriptive text for non-standard or unusual quality events (coded as 999)

## Data Usage and Community

- Data are intended for use by researchers and policy colleagues; metadata and quality codes facilitate assessment of suitability and data quality.
- The dataset supports collaboration across the ECN network and requires acknowledgment and sharing of publication outputs.