# Dataset Originator

- ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology.

## Overview for GIS Specialists

- Purpose: Macrolepidoptera observations collected nightly via standard light-trap protocol (Rothamsted Insect Survey) to support environmental-change research and mapping of species distributions over time.
- Data focus: Moth counts and quality indicators from multiple ECN sites, suitable for map-based analysis and visualization of spatial-temporal trends.

## Dataset Scope and Site Coverage

- Site codes and metadata:
  - T01 Drayton; coordinates 52°11'37.95"N, 1°45'51.95"W; data 02-Jan-1993 to 26-Dec-2012.
  - T02 Glensaugh; 56°54'33.36"N, 2°33'12.14"W; 23-Mar-1994 to 09-Dec-2012.
  - T03 Hillsborough; 54°27'12.24"N, 6°4'41.26"W; 14-Feb-1993 to 23-Nov-2012.
  - T04 Moor House - Upper Teesdale; 54°41'42.15"N, 2°23'16.26"W; 01-Jan-1993 to 17-Nov-2012.
  - T05 North Wyke; 50°46'54.96"N, 3°55'4.10"W; 10-Dec-1992 to 21-Dec-2012.
  - T06 Rothamsted; 51°48'12.33"N, 0°22'21.66"W; 24-Feb-1992 to 17-Dec-2012.
  - T07 Sourhope; 55°29'23.47"N, 2°12'43.32"W; 14-Jan-1993 to 19-Dec-2012.
  - T08 Wytham; 51°46'52.86"N, 1°20'9.81"W; 22-Oct-1992 to 17-Dec-2012.
  - T09 Alice Holt; 51°09'16.46"N, 0°51'47.58"W; 10-Nov-1992 to 04-Dec-2012.
  - T10 Porton Down; 51°07'37.83"N, 1°38'23.46"W; 01-Mar-1994 to 24-Oct-2012.
  - T12 Cairngorms; 57°06'58.84"N, 3°49'46.98"W; 01-Jan-2001 to 31-Dec-2012.
- Observation structure:
  - One moth trap per site (LCODE is always 1).
  - Data recorded nightly.
  - Observations encoded via SITECODE, LCODE, SDATE, FIELDNAME, VALUE.
  - FIELDNAME indicates either a quality code or a species code; VALUE reflects quality detail or count of individuals.

## Data Structure and Key Codes

- Table 1 data structure:
  - SITECODE: site identifier
  - LCODE: location/trap code (always 1 in this dataset)
  - SDATE: sampling date (dd-mmm-yyyy)
  - FIELDNAME: either a quality code or a species code
  - VALUE: if QUALITY, detailed code; if SPECIES, observed count
- Quality codes (Table 3a / Table 4):
  - Standard ECN quality codes (e.g., 100 to 119, 120– etc.) capturing data issues such as no information, sample loss, debris, adverse weather, etc.
  - 999: unusual event (textual QC notes in supplemental files)
  - Quality codes are applied by ECN site managers; additional context may be provided in accompanying quality text.
- Species codes (Table 3b):
  - Extensive, hierarchical mapping of moth species codes to Latin and common names (e.g., 100 = Furcula bicuspis, Alder Kitten; many hundreds of codes spanning macro- and micro-moths).
  - Codes range from common, well-known taxa to unidentifiable taxa (e.g., “Unidentifiable …” placeholders) and micro-species groupings.
- Quality descriptors:
  - The ECN quality framework allows multiple codes per observation to reflect different issues; text-based explanations for non-covered cases may exist in supplementary files.

## Supplemental Quality Information

- ECN_IM2.csv: period over which traps were set (e.g., PERIOD = number of days traps were open). Primarily for understanding temporal aggregation at each observation.
- ECN_IM_qtext.csv: additional quality information and narrative explanations for absences or inconsistencies.

## Data Usage and Acknowledgement

- Acknowledge ECN data usage in publications; ECN requests one reprint of any publication citing their data.
- Data compatibility notes for GIS work:
  - Data are nightly and may be aggregated to daily, monthly, or yearly resolutions as needed.
  - Observations span multiple sites with varying date ranges; align by SDATE when creating spatio-temporal layers.
  - Quality codes should be used to filter or flag observations in GIS analyses (e.g., exclude low-quality periods or interpret carefully when quality codes indicate data loss or debris).

## Practical Considerations for GIS Work

- Spatial integration:
  - Use provided site coordinates to create point features with time stamps (SDATE) and attributes for species counts (VALUE) or quality indicators (FIELDNAME when it encodes quality).
  - Consider creating a time-enabled layer to visualize changes in species counts over time per site.
- Data cleaning and standardization:
  - Resolve FIELDNAME types by distinguishing whether an observation is a quality code or a species count.
  - Leverage supplemental quality files to interpret unusual periods or filter out questionable data.
  - Be aware of large, multi-code quality flags; implement rules to handle observations with multiple quality codes.
- Data resolution and aggregation:
  - The dataset’s per-site, nightly observations can be aggregated to coarser temporal units (e.g., monthly) for mapping trends.
  - If combining with other ECN datasets, account for differing resolutions and trap-periods (ECN_IM2 PERIOD).
- Documentation and provenance:
  - Include references to ECN data originator, the Rothamsted Insect Survey methodology, and the contributing partner organizations when publishing or sharing derived maps.

## Access and References

- Data originator: ECN Data Centre, http://data.ecn.ac.uk; ecn@ceh.ac.uk
- Dataset information: ECN site catalogue (https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27)
- Supplemental files: ECN_IM2.csv and ECN_IM_qtext.csv (accompanying quality and trap-period data)

## Notes

- Protocol and data characteristics:
  - Macrolepidoptera collected using standard light traps; Rothamsted Insect Survey methodology.
  - Data recorded nightly with accompanying quality information necessary for robust GIS analysis.
  - Dataset emphasizes proper acknowledgement and sharing of usage outcomes.