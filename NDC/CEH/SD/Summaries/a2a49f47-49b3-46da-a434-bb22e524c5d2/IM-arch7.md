# IM Protocol

## Overview and purpose
- Purpose: To collect and identify daily collections of macrolepidoptera (butterflies and moths) using a standard light-trap methodology (RIS) and to support long-term analyses of environmental change.
- GIS relevance: Produces spatially explicit and time-stamped data across multiple sites, enabling mapping and temporal trend analyses through RIS and ECN databases. Builds on a national, multi-site light-trap network with a long history of data.

## Data and GIS relevance
- Core data dimensions: 
  - Site Identification Code (unique to each ECN site)
  - Core Measurement Code (e.g., IM for invertebrates – moths)
  - Location Code (sampling location within a site)
  - Sampling Date/time (date and sometimes time for non-daily sampling)
- Taxonomic and count data:
  - Species code, species name, and number caught (units are RIS codes)
  - Data structured to support multi-species tallies per sampling occasion
- Data storage and access:
  - Data stored in the Rothamsted Insect Survey (RIS) database and the ECN database
  - ECN dataset formats documented in the Data Transfer documentation (restricted access)
  - Contact ecnccu@ceh.ac.uk for access to documentation and datasets

## Equipment, location, and sampling approach
- Trap design: Standard RIS light trap with a 200 W clear tungsten lamp, mounted on a stand (~1.5 m total height)
- Power and safety: Mains electricity with protective RCD; lamp on dusk and off at dawn; automatic solar dial time-switch
- Sampling procedure:
  - Daily emptying preferred; if not possible, samples may be accumulated (e.g., weekends)
  - Samples sent to Rothamsted for identification unless local expertise exists
  - For large sites, operate more than one trap if feasible
- Site logistics:
  - Location near laboratories, houses, farms; sheltered by vegetation if possible; ideally >20 m from artificial light sources
  - Site proximity to TSS is noted for protocol context (relevant to GIS site mapping)

## Appendix I: description and daily operation
- Trap configuration: RIS light trap with a collecting jar dosed with ~5 ml tetrachloroethane; safety considerations for handling chemical fumes
- Daily routine (approx. 5 minutes per trap):
  - Check RCD status and reset or replace fuse if tripped
  - Verify GMT time on clock (solar clock adjusts for daylength; do not adjust for local time)
  - Confirm light bulb operation; replace if needed (only 200 W tungsten bulbs)
  - Swap collecting jar and re-dose with tetrachloroethane
  - Record site name and correct date on sample boxes; handle multi-night sampling with appropriate date ranges
- Date conventions:
  - If sampling spans two dates (dusk to dawn), the date to record reflects the date of the trap’s operation period (e.g., 14-15 June 1995)

## Safety and handling
- Tetrachloroethane hazards:
  - Toxic by inhalation and contact; PPE and ventilation required
  - Procedures for spills and skin exposure outlined (ventilated area, gloves, respirator for large spills)
- Electrical safety:
  - Disconnect power before changing bulbs; consult electrician for exposed circuitry; regular RCD testing recommended

## Data specification and recording conventions
- Core dataset fields (essential for each sampling location):
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Sampling Date/time
- Recording fields for results:
  - Species code and species name
  - Number caught (RIS code)
- Operational notes:
  - Record non-operational nights and dates when the trap did not operate
  - Follow Heslop (1964) coding system for data entry

## Notes and references
- Background context:
  - The RIS light-trap network and its long-term data foundation are documented in related methodological and ecological literature (e.g., Taylor 1986; Woiwod et al. works)
- Data management references:
  - Data transfer and formatting guidelines are provided in ECN documentation and are accessible via restricted sites or through ECNCCU contacts

## Endnotes
- This protocol supports GIS-enabled analysis by standardizing spatial identifiers, temporal stamps, and taxon counts, while detailing the data management workflow from field collection to centralized databases.