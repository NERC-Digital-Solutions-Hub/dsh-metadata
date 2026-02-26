# UK Environmental Change Network (http://www.ecn.ac.uk) Bats (BA)

## Overview
- A bat monitoring dataset from the UK Environmental Change Network (ECN) intended to support scrutiny of environmental health measures, policy evaluation, and informing future decisions.
- Data are collected and managed by the ECN Data Centre with input from a consortium of UK government departments and agencies funding site monitoring or network coordination.
- Dataset owner: UK Environmental Change Network; sponsors include Agri-Food and Biosciences Institute, BBSRC, Natural Resources Wales, DSTL, DEFRA, Environment Agency, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, and SNH.
- Users are asked to acknowledge data sources and to send one reprint of publications citing the data.

## Data provenance, ownership and access
- Dataset origin: ECN programme focusing on environmental change impacts on bat populations.
- Data centre contact: ECN Data Centre (ecn@ceh.ac.uk); data hosted in an Oracle database with site-specific tables.
- Data sharing and metadata: users should refer to accompanying quality information; data governance practices apply; open sharing of underlying data is encouraged but may present barriers.

## Sampling protocol and data collection
- Survey method: bats detected and mapped with a bat detector along transects; observations are linked to habitat and environmental context.
- Methodology basis: derived from the Bats and Habitats survey by Prof S. Harris and colleagues for the JNCC; designed to complement broader monitoring programmes.
- Survey schedule: transects walked four times per year in fixed periods (three-week windows: 15 Jun–6 Jul; 7–27 Jul; 28 Jul–17 Aug; 18 Aug–7 Sep); surveys not conducted in heavy rain or strong winds.
- Limitations: the approach provides limited information on precise population-environment change relationships; linking ECN results with other datasets helps mitigate this.

## Data structure and schema
- Core data are organized into three Oracle-based data groups, one per site:
  - D1BA_xxx: Core observational data
    - Key fields: SITECODE, SDATE, TRANSECT, BATLOC_ID, FIELDNAME, VALUE, ACTS, ACTH, ACTF
    - FIELDNAME holds bat species codes; VALUE holds counts
  - D2BA_xxx: Survey conduct and equipment information
    - Key fields: BATDETECTORTYPE, KEPTPROTOCOLFREQUENCY, ADJUSTFREQUENCY, USEREFERENCECD, USESONOGRAMANALYSIS
  - D3BA_xxx: Habitat observations on transect
    - Key fields: HAB1, HAB2, HAB3 (habitat types); BATLOC_ID; plus habitat-related metadata
- Data are organized per site, with table suffixes corresponding to site codes.

## Site codes and dataset coverage
- T01 Drayton: coordinates 52°11'37.95"N 1°45'51.95"W; date range 29-JUN-1993 to 05-SEP-2006
- T02 Glensaugh: coordinates 56°54'33.36"N 2°33'12.14"W; date range 07-JUL-1994 to 30-AUG-2012
- T03 Hillsborough: coordinates 54°27'12.24"N 6°4'41.26"W; date range 12-AUG-1994 to 05-SEP-2002
- T04 Moor House - Upper Teesdale: coordinates 54°41'42.15"N 2°23'16.26"W; date range 16-JUN-1993 to 28-AUG-2012
- T05 North Wyke: coordinates 50°46'54.96"N 3°55'4.10"W; date range 04-JUL-1993 to 30-AUG-2012
- T07 Sourhope: coordinates 55°29'23.47"N 2°12'43.32"W; date range 12-JUL-1994 to 03-SEP-2012
- T08 Wytham: coordinates 51°46'52.86"N 1°20'9.81"W; date range 05-JUL-1993 to 21-AUG-2012
- T09 Alice Holt: coordinates 51° 9'16.46"N 0°51'47.58"W; date range 29-JUN-1994 to 05-SEP-2012
- T10 Porton Down: coordinates 51° 7'37.83"N 1°38'23.46"W; date range 04-JUL-1994 to 03-SEP-2006
- T11 Y Wyddfa - Snowdon: coordinates 53° 4'28.38"N 4° 2'0.64"W; date range 16-JUL-1996 to 31-AUG-2011

(Note: site T06 is not listed in the provided data.)

## Encoding of species and habitats
- Fieldname (D1BA) species codes and their Latin/Common names (examples):
  - Bb: Barbastella barbastellus (Barbastelle)
  - Es: Eptesicus serotinus (Serotine)
  - M, Ms, Mb, Md, Mm, Mw, Mn: various Myotis species
  - Nl, Nn: Nyctalus leisleri, Nyctalus noctula
  - Pp, Ppl, Ppg, P: Pipistrellus spp. and related
  - Pa, Pg: Plecotus spp. (brown/grey long-eared)
  - Rf, Rh: Rhinolophus ferrumequinum, Rhinolophus hipposideros
  - UU: Unidentified bat
  - XX: No bats found
- Habitat types (HAB1–HAB3) are recorded as codes with descriptions, e.g. hedgerows, treelines, roads, streams, woodlands, grasslands, arable, built land, etc.
- The habitat codes under VALUE describe a long list of categorized landscape features (1–43), each with a detailed description (e.g., hedgerows, treelines, walls, roads, streams, ponds, various woodland types, grasslands, arable, built land, etc.).

## Data quality, metadata and governance
- Metadata: core metadata tables exist; the documentation refers readers to the core metadata documentation for structure details.
- Data governance: adherence to quality information, data cleaning, transformation, and transparent presentation through reports, charts, or dashboards; data sharing of underlying data is encouraged under governance standards.
- Methodological transparency: protocol reference provided and linked; acknowledges limitations in deriving precise population-environment relationships from this specific bat-monitoring approach.

## Limitations and interpretation cautions
- The methodology provides limited insight into precise population levels and their direct links to environmental change.
- Use of accompanying quality information is essential to correctly interpret the data.
- Some survey components (e.g., data fields in D2BA and D3BA) include optional entries, requiring careful handling of missing data.

## How to use and attribution
- Data usage should include acknowledgment of ECN data and the data centre; authors are requested to send one reprint of any publication citing the data.
- Protocol reference and data governance processes are provided to ensure correct application and interpretation.
- The dataset is designed to be linked with broader monitoring programmes to enhance interpretability of bat responses to environmental change.