# The dataset:

- Scope and purpose
  - Dataset of prey items for common guillemot Uria aalge and razorbill Alca torda observed during the 2017 breeding season.
  - Sites: East Caithness Special Protection Area (SPA), Buchan Ness to Collieston Coast SPA, and Isle of May National Nature Reserve (NNR) off the east coast of Scotland.
  - Aligns with long-running diet monitoring methods standardised since 1987 as part of the Isle of May Long-Term Study (IMLOTS) and UK Seabird Monitoring Programme.

- Spatial coverage
  - Precise site coordinates provided for each location:
    - East Caithness SPA: 58°12´42'N, 03°27´53'W
    - Buchan Ness to Collieston Coast SPA: 57°23´07'N, 01°52´09'W
    - Isle of May NNR: 56°10´57'N, 02°33´17'W
  - Data suitable for GIS mapping of prey distribution by colony and over time.

- Temporal coverage
  - Field observation windows:
    - East Caithness and Buchan Ness to Collieston Coast: two-hour watches from 04:00–22:00 within the breeding season (June–July 2017 ranges specified).
    - Isle of May: dawn to dusk watches on two dates in June 2017.
  - Opportunistic observations recorded within the same general date ranges.

- Field measurements and data collection
  - For both species, prey items observed in the bill of breeding adults returning to feed chicks (and display for guillemot).
  - Guillemot data (during watches):
    - Variables recorded: time of arrival, prey species, prey size (and size category). For opportunistic observations, only prey size and time of arrival not recorded.
    - Prey are mainly lesser sandeel or clupeids; clupeids include sprat and herring, indistinguishable in the field; all such fish classified as clupeids in the dataset.
    - Prey size categorized into five classes: very small, small, medium, large, very large, guided by adult bill length.
    - When feeding to chick, prey may be obscured; items presented are presumed eaten; some size/species classifications may be incomplete.
    - Number of prey items not typically recorded; however, a single prey item is typical during chick provisioning (display events observed).
  - Razorbill data (during watches):
    - Variables recorded: time of arrival, prey species, prey size, prey number.
    - Opportunistic observations: only prey size and prey number recorded.
    - Prey size categories and clupeid limitation as for guillemot.
    - Multiple fish per bill observed during provisioning to chicks.

- Data structure, coding, and interpretation
  - Prey assigned to one of five size classes based on bill length guidance.
  - Fish from breeding ledges used to estimate lengths within size categories; gadoids limited in number and not used for precise size estimates due to small representation.
  - Prey species identification is robust for common items but not always species-level, especially within clupeids (sprat vs herring).
  - Data aggregated and interpreted with the understanding that some observations may not capture exact species or counts.

- Data management and quality control
  - Field data collected by trained staff using notebooks and field data sheets; transcribed to spreadsheets after verification.
  - All data and notations archived at CEH Edinburgh; notebooks and sheets preserved.
  - Databases quality controlled at the source; outputs and reports vetted to meet contractual deliverables.
  - Encouragement of publishing non-confidential findings in peer-reviewed literature with customer approval and acknowledgement.

- Output and context
  - Methods and protocols align with established standardised seabird diet assessment practices since 1987.
  - The dataset supports assessments of prey composition, diet diversity, and possible shifts in prey communities (noted in related literature).
  - Data suitable for integration across sites to analyze spatial and temporal trends in seabird diet for policy, conservation planning, and research.

- Key methodological notes and references
  - Core methods and size categorization are consistent with previous work (Harris & Wanless; Daunt et al.; Thaxter et al.; Wilson et al.).
  - Previous diet studies at Isle of May and Buchan Ness to Collieston Coast SPA contextualize the current data (1980s–2010s).

- Practical GIS considerations
  - Spatially explicit with exact colony coordinates and time-stamped observations.
  - Supports mapping of prey species distribution by site and date, assessment of seasonal dietary shifts, and correlation with environmental factors (e.g., prey availability, fisheries closures).
  - Data completeness varies by species (more complete for recorded prey items during watches; opportunistic observations provide partial data).