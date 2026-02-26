# IB Protocol

## Aim
- Monitor the abundance of butterflies using transect methods from the Butterfly Monitoring Scheme (BMS).
- Leverage ~15 years of prior data for comparability and to relate butterfly counts to vegetation and climate (long-term monitoring context).

## Rationale
- Butterflies are relatively easy to identify and respond quickly to vegetation quality and abundance.
- Existing national scheme provides a strong background; prior analyses show relationships between butterfly numbers, flight phenology, and climate.

## Method and Location
- Use fixed transect routes at each site, following established instructions; routes reflect site representativeness and may follow existing paths or boundaries.
- Transect length typically 1–2 km, walkable in 30–90 minutes.
- Each transect is divided into up to 15 sections with varying habitat/management; routes should be marked to ensure consistency across sampling occasions.
- Record habitat types and abundant plants, with emphasis on butterfly food plants (e.g., nettles, violets) and nectar sources; changes in habitat are logged to aid interpretation.
- Recording occurs weekly during 1 April–29 September.

## Recording Conditions and Procedure
- Recording window: 10:45–15:45 BST; temperature thresholds apply (≤17°C for northern/uphill sites; otherwise acceptable if not raining with sufficient sunshine).
- More than one recorder can be used to manage peak season workload.
- Transect is walked at an even pace; observers count butterflies seen within a 5 m x 5 m x 5 m imaginary box in each section.
- Start time, end-of-transect temperature, percentage sunshine, and wind speed are recorded; sunshine is tracked section-by-section as the transect progresses.
- Typical effort: 0.5–1.5 hours per transect, across 26 weeks.

## Data Collection, Parameters, and Schema
- Core identifiers (must be included in all datasets):
  - Site Identification Code (e.g., T05)
  - Core Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Sampling Date/Time
- Core measurement: Invertebrates – butterflies (IB Protocol)
- Weekly variables (1 April–29 September):
  - Recording date/time; start time
  - Temperature at end of recording
  - Percentage sunshine (units: %)
  - Wind speed at end of recording (Beaufort scale)
- For each transect section:
  - Transect section number
  - Species code and species name
  - Number seen
  - Habitat description (numeric code 1–15) and habitat description precision
  - BMS code and common name
  - Count
  - BMS method (coding conventional to BMS)
- Recording forms: Standard BMS recording form available from the Butterfly Monitoring Scheme (BMS), organized via the Biological Records Centre.
- Data conventions: adhere to BMS coding system; habitat descriptions should be concise and descriptive to aid interpretation, focusing on key plant associations rather than exhaustive plant inventories.

## Data Transfer, Access, and Provenance
- Data transfer documentation exists for ECN datasets (refer to restricted-access Site Managers’ extranet; ECNCCU Data Transfer documentation).
- For access to documentation or data transfer details, contact ecnccu@ceh.ac.uk.

## Notes on Interpretation
- Habitat descriptions serve interpretive purposes; the aim is not exhaustive quantitative plant abundance data but context for results.
- The protocol emphasizes comparability with long-running datasets and the ability to analyze relationships with climate and vegetation changes over time.

## References
- Hall, M.L. 1981. Butterfly Monitoring Scheme. Instructions for independent recorders.
- Pollard, E. 1988. Temperature, rainfall and butterfly numbers.
- Pollard, E. 1991. Changes in flight period of the hedge brown butterfly during range expansion.
- Pollard, E., Hall, M.L. & Bibby, T.J. 1986. Monitoring the abundance of butterflies.
- Thomas, J.A. 1991. Rare species conservation: case studies of European butterflies.