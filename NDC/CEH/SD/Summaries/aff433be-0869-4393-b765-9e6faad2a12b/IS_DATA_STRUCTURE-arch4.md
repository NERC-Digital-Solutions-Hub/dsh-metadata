# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Overview: A dataset from the UK Environmental Change Network (ECN) focusing on spittlebug (Philaenus spumaris) and related nymphs/morphs, collected annually using standardized protocols to support environmental change research.
- Data scope: Includes nymph density data and adult colour morph data collected once per year from multiple ECN sites.

## Dataset Owners and Sponsorship

- Owners and sponsorship: The ECN programme is sponsored by a consortium of UK government departments and agencies (e.g., Agri-Food and Biosciences Institute; BBSRC; Natural Resources Wales; DEFRA; Environment Agency; Natural England; NERC; Scottish Government; etc.).
- Acknowledgement and use: ECN requests acknowledgement of data use and a copy of any publication citing ECN data; please send one reprint of such publication.

## Protocol, Quality, and Usage

- Protocol: Standard operating procedures ensure data comparability across sites. An accompanying is.pdf explains data collection methods.
- Purpose of protocol: To estimate annual indices of nymph densities and adult morph proportions using sweep nets; data are recorded annually with accompanying quality information.
- Data quality: Quality codes assigned by site managers from a standard list; unusual events can be described with text (quality code 999). Quality text files provide additional context for data quality issues.
- Usage notes: Data are intended for analysis of nymph counts and adult morphs with attention to data quality indicators; users should consult the quality information when using the data.

## Data Download and File Structure

- Nymph data file: ECN_ISN.csv
  - Key fields: SITECODE, LCODE, SDATE, ISN_SPEC, FIELDNAME, VALUE, plus multiple quality-related Q1–Q8 fields.
- Adult data file: ECN_ISA.csv
  - Key fields: SITECODE, LCODE, SDATE, ISA_MORPH, FIELDNAME, plus quality fields.
- Supporting quality documentation: ECN_ISN_qtext.csv and ECN_ISA_qtext.csv provide readable explanations for quality codes and events.
- Site and location codes: Explanatory Information for Site Codes (T01–T12 and corresponding coordinates) and for location names.
- Variable descriptions: FIELDNAME entries describe measured spittlebug counts per quadrat and related metrics (e.g., number of spittles in quadrats, mean nymph counts, morph counts).

## Metadata, Site/Variable Details

- Site codes: 12 ECN sites with both site name and precise location coordinates (e.g., T01 Drayton; T12 Cairngorms).
- Variables measured: A standardized set of 1–40 FIELDNAME entries representing counts per quadrat, along with derived metrics (e.g., NSPITCHK, MEANNYM, NMAL, NFEM, NTOT) and quality indicators (Q1–Q8).
- Adult colour morphs: Codes for morphs such as ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU.
- Quality codes: Extensive list (e.g., 100–109 for sample issues, 114–... for environmental/field conditions, 200–? for sampling/recording conditions, 501–508 for laboratory issues, 999 for unusual events). A separate quality text file provides descriptions for non-standard codes.

## How to Use and Cite

- Access and reuse: Data are provided with structure and metadata to support discovery, compatibility checks, and reuse across research and policy contexts.
- Acknowledgement: Include acknowledgement of ECN data use and provide a reprint of any publication citing ECN data as part of dataset usage.

## Contact and Further Information

- For more information about ECN sites and data, refer to the provided site catalogue link: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27
- Primary data contact: ECN Data Centre at CEH (ecn@ceh.ac.uk) via the dataset originator address.