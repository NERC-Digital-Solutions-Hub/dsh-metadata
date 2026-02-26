# IB Protocol

## Aim
- Monitor butterfly abundance using transect methods from the Butterfly Monitoring Scheme (BMS).
- Leverage a well-established background (approx. 15 years) for comparison with ECN data; build on evidence linking butterfly numbers with climate and vegetation changes.

## Rationale
- Butterflies are easy to identify and respond rapidly to changes in vegetation abundance and quality.
- Prior analyses show shifts in distribution and phenology, and relationships between abundance and climate.

## Location and transect design
- A fixed transect route is established at each site to be representative of the ECN site, often along existing paths or boundaries and spanning different management regimes.
- Transect length: usually 1–2 km, able to be walked in 30–90 minutes; may be marked to ensure consistency across visits.
- The route is divided into up to 15 sections (sampling strata) with recorded habitat types and abundant plants; nearby management activities are also noted.
- Data collection is designed for repeatability and comparability over time and across sites.

## Data collection method
- Recording occurs weekly from 1 April to 29 September, 10:45–15:45 BST (adjustments based on temperature and sun conditions).
- Temperature constraints: recording preferred at 13–17°C with at least 60% sunshine; if above 17°C, recording may occur in any conditions provided it is not raining; northern upland sites have a maximum of 15°C.
- Multiple recorders can be used to handle peak activity periods or provide coverage.
- The transect is walked at a steady pace; butterflies seen flying within or passing through a 5 m × 5 m × 5 m imaginary box are recorded by species for each section.
- Start time, temperature, percentage sunshine (section-by-section), and wind speed are recorded at the end of the transect; temperature/conditions are noted as required.

## Data structure and core variables
- Core identifiers (for all datasets):
  - Site Identification Code (e.g., T05)
  - Core Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Sampling Date/time (including time when sampling occurs)
- Core measurement: invertebrates — butterflies (IB Protocol)
- Weekly variables recorded (April 1 – September 29):
  - Recording date/time, start time
  - Temperature at end of recording, percentage sunshine, wind speed
  - Units and precision noted (BST, °C, Beaufort scale, etc.)
- For each transect section:
  - Transect section number
  - Species code, species name, number seen
  - Habitat description (numeric code 1–15)
  - BMS code, common name
  - Recording method (BMS)
  - Habitat descriptions and plant context (qualitative notes on prominent food plants and nectar sources)
- Additional data quality/format notes:
  - Precision of recording (per variable)
  - Standardized coding and habitat descriptions per BMS handbook
  - Emphasis on descriptive habitat context to aid interpretation rather than exhaustive plant quantification

## Recording forms and standards
- A standard BMS recording form is used, available from the Butterfly Monitoring Scheme (BMS) via the Biological Records Centre, ITE Monks Wood.
- Coding follows the standard BMS conventions.
- Habitat descriptions should be concise and help interpretation (e.g., noting key butterfly food plants and nectar sources); full plant quantification is not required due to time constraints.

## Time commitment and duration
- Each transect: approximately 0.5–1.5 hours per visit.
- Frequency: weekly over 26 weeks (April 1 to September 29).

## Access, data transfer, and documentation
- Data submission is guided by the ECN Data Transfer documentation for ECN dataset formats (restricted access via the Site Managers’ extranet).
- Data management includes a centralized process for coordinating core measurements across sites, with contact details provided for access (ecnccu@ceh.ac.uk).

## References and background
- Based on the national Butterfly Monitoring Scheme (Hall 1981; Pollard, Hall & Bibby 1986) and subsequent analyses (Pollard 1988; Pollard 1991; Thomas 1991).
- Provides continuity with existing long-term data and established methodologies for comparability and trend analysis.

## Implications for Data Leaders
- Leverage the long-running BMS framework to ensure data continuity, quality, and comparability with national datasets.
- Maintain clear metadata, consistent identifiers, and standardized habitat coding to support cross-site analyses and policy-relevant insights.
- Facilitate data access through documented transfer protocols and restricted-access documentation for governance and security.
- Align transect design and sampling schedules with organizational data strategy to enable integration with broader ecological monitoring efforts and data-informed decision-making.