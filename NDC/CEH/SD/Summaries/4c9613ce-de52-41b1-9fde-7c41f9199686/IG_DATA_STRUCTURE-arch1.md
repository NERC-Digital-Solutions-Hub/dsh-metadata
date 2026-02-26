# UK Environmental Change Network (http://www.ecn.ac.uk) Ground Predators (IG) Dataset

- Overview
  - Focus: abundance of ground predators (Carabidae) monitored with pitfall traps.
  - Sampling protocol: data collected fortnightly from May to October (seasonal trapping cadence).
  - Scope: data across 12 ECN sites (Drayton, Glensaugh, Hillsborough, Moor House Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Y Wyddfa - Snowdon, Cairngorms).
  - Data accompany quality information and usage acknowledgments.

- Data Origin, Ownership, and Access
  - Dataset Originator: UK Environmental Change Network (ECN) Data Centre.
  - Dataset Owners: ECN programme sponsors (multiple UK government departments and agencies funding monitoring and coordination).
  - Acknowledgement: please acknowledge data use and send one reprint of any publication citing the data.

- Protocol and Metadata Context
  - Protocol: pitfall traps to monitor ground predator abundance.
  - Temporal coverage: data recorded for each site across multiple years, with site-specific date ranges.
  - Quality: use accompanying quality information; unusual events may be flagged with quality code 999 and textual notes.

- Data Structure and Schema
  - Storage: data are held in an Oracle database with 12 site-specific tables for each data type.
  - Data types and tables:
    - D1IG_xxx: abundance data (one table per site). Core fields include SITECODE, LCODE, SDATE, TRAP, FIELDNAME, VALUE.
    - D2IG_xxx: trap deployment/outcome data (one table per site). Core fields include SITECODE, LCODE, FROMDATE, SDATE.
    - D3IG_xxx: habitat information (one table per site). Core fields include SITECODE, LCODE, HABDESC.
  - Metadata references:
    - M_DESC and M_REFFIELD provide description and field reference information.
  - Data schema notes: core metadata documentation exists separately; accompany data with relevant quality metadata.

- Site Codes, Names, and Ranges
  - T01 Drayton: coordinates 52°11'37.95"N 1°45'51.95"W; 12-MAY-1993 to 28-OCT-2009.
  - T02 Glensaugh: coordinates 56°54'33.36"N 2°33'12.14"W; 27-MAY-1994 to 31-OCT-2012.
  - T03 Hillsborough: coordinates 54°27'12.24"N 6°4'41.26"W; 14-MAY-1993 to 31-OCT-2012.
  - T04 Moor House - Upper Teesdale: coordinates 54°41'42.15"N 2°23'16.26"W; 20-MAY-1993 to 17-OCT-2012.
  - T05 North Wyke: coordinates 50°46'54.96"N 3°55'4.10"W; 05-MAY-1993 to 30-NOV-2010.
  - T06 Rothamsted: coordinates 51°48'12.33"N 0°22'21.66"W; 28-JUL-1992 to 03-NOV-2009.
  - T07 Sourhope: coordinates 55°29'23.47"N 2°12'43.32"W; 25-MAY-1994 to 14-NOV-2012.
  - T08 Wytham: coordinates 51°46'52.86"N 1°20'9.81"W; 26-MAY-1993 to 31-OCT-2012.
  - T09 Alice Holt: coordinates 51° 9'16.46"N 0°51'47.58"W; 18-MAY-1994 to 31-OCT-2012.
  - T10 Porton Down: coordinates 51° 7'37.83"N 1°38'23.46"W; 24-MAY-1994 to 31-OCT-2012.
  - T11 Y Wyddfa - Snowdon: coordinates 53° 4'28.38"N 4° 2'0.64"W; 19-MAY-1999 to 28-NOV-2012.
  - T12 Cairngorms: coordinates 57° 6'58.84"N 3°49'46.98"W; 23-JUN-1999 to 14-NOV-2012.

- Field Names and Quality Codes
  - Fieldname: stores either a species code or a quality code.
  - Quality codes: ECN provides a standard set (e.g., 100, 101, 102, ..., 999 for unusual events). Descriptions cover data loss, sampling issues, equipment problems, environmental conditions, non-standard sampling, data editing, and other qualifiers.
  - Non-standard or unusual entries may be accompanied by free-text quality notes when codes do not cover the event.

- Species Codes and Taxonomic Mapping
  - The dataset includes extensive species/genus codes (e.g., Cicindela, Carabus, Bembidion, Harpalus, etc.) with hierarchical taxonomy (GENUS and SPECIES levels) and many synonyms/allocations.
  - Example structure: codes map to Latin names, taxonomic rank (GENUS or SPECIES), and typical groupings within Carabidae.
  - The mapping table provides broad coverage across genera and species, enabling detailed taxonomic analyses.

- Using the Data for Analysis
  - Keys to join: use SITECODE, LCODE, SDATE (and FROMDATE for deployment data) to link abundance, trap deployment, and habitat information.
  - Data quality: incorporate ECN quality codes and accompanying text when assessing data reliability.
  - Data provenance and reproducibility: record data sources and dataset versions; datasets can be made discoverable with metadata through ECN portals.

- Protocol Reference and Contact
  - Protocol reference: http://www.ecn.ac.uk/measurements/terrestrial/i/ig
  - Contact: ecn@ceh.ac.uk for data access or questions.
  - Publication acknowledgement: send one reprint of any work citing the data.