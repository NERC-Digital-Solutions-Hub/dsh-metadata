# UK Environmental Change Network (http://www.ecn.ac.uk) Atmospheric Chemistry: Nitrogen Dioxide (AN)

- The ECN NO2 dataset uses passive diffusion tubes deployed for two-week periods to measure NO2 concentrations.
- Data are managed by the ECN Data Centre and ECN-owners, with sponsorship from a consortium of UK government departments and agencies.
- 12 UK sites (Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms) span 1993–2012 (date ranges vary by site).
- Researchers are asked to acknowledge ECN data usage and to send one reprint of any publication citing the data.

## Data Structure and Access

- Data are stored in Oracle with 12 site-specific tables.
  - Tables are named D1AN_xxx or possibly D2AN_xxx, where xxx is the site code.
- Core data fields (example structure):
  - SITECODE, SDATE (sampling date), TUBEID (E = Experimental, B = Blank), FIELDNAME, VALUE.
  - VALUE is usually numeric; some fields may be optional.
- Additional sample-collection metadata exists (e.g., DEPDATE, DEPHOUR, SDATE, SHOUR, SMINS) in the corresponding tables.
- Metadata relationships reference:
  - M_DESC for dataset descriptions
  - M_REFFIELD for field references
- Quality information is integral and included with the dataset; accompanying quality documentation should be used when analyzing the data.

## Data Content and Metadata

- Fieldnames (examples):
  - WEIGHTNO2 (weight of NO2 on the mesh; micrograms)
  - NO2 (NO2 concentration; micrograms/m3)
  - NO2PPB (NO2 concentration; ppb)
  - TDIFF (exposure time; minutes)
  - Q1–Q8 (quality codes; integer)
- Quality Codes:
  - Standard ECN codes cover data availability, sample integrity, environmental/interference factors, and laboratory issues (e.g., 100 = no information available; 101 = no sample/reading taken; 105 = snow in funnel; 501–509 relate to laboratory issues; 513 indicates a calculated value issue; 999 = unusual event with accompanying text).
  - The complete list is provided within the dataset’s quality information.
- Quality codes are assigned by ECN site managers and may be accompanied by explanatory text when codes do not cover a situation.

## Site Coverage and Temporal Range

- 12 sites with explicit site names, coordinates, and date ranges:
  - T01 Drayton; 20-Jan-1993 to 26-Dec-2012
  - T02 Glensaugh; 12-May-1993 to 12-Dec-2012
  - T03 Hillsborough; 02-Feb-1994 to 19-Dec-2012
  - T04 Moor House - Upper Teesdale; 03-Feb-1993 to 24-Dec-2012
  - T05 North Wyke; 21-Jul-1993 to 26-Dec-2012
  - T06 Rothamsted; 03-Feb-1993 to 12-Dec-2012
  - T07 Sourhope; 09-Jun-1993 to 26-Dec-2012
  - T08 Wytham; 03-Feb-1993 to 19-Dec-2012
  - T09 Alice Holt; 11-May-1994 to 27-Dec-2012
  - T10 Porton Down; 06-Jul-1994 to 12-Dec-2012
  - T11 Snowdon (Y Wyddfa); 26-Mar-1997 to 27-Dec-2012
  - T12 Cairngorms; 10-Nov-1999 to 12-Dec-2012
- The dataset emphasizes long-term monitoring with varying coverage by site.

## Usage Guidance and Data Products

- Primary aim is to enable end users to self-serve through data products (e.g., dashboards, pivot tables) and to provide guidance on using these tools.
- Data may be combined across sites and time periods; quality information must be considered when aggregating.
- The documentation notes that the data are best used with accompanying quality metadata to assess reliability and context.

## Acknowledgments and Publication

- Users must acknowledge ECN data usage in publications.
- Please send one reprint of any publication that cites ECN data.