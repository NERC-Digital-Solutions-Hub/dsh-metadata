# Background The NERC Soil Biodiversity Thematic Programme

- The NERC Soil Biodiversity Thematic Programme (established in 1999) focused on intensive study of a large field experiment at Sourhope (Scottish Borders) to understand soil biodiversity, its functional roles in ecological processes, and changes in aboveground productivity, species composition, and diversity.
- Twenty-four research projects were funded to study soil structure, soil processes (e.g., carbon and nitrogen cycles), and the roles of micro-, meso-, and macro-fauna and flora.
- Primary aim: align understanding of soil biota with their ecological roles, enabling integrated insights into soil biodiversity and ecosystem function.

- Data stewardship context:
  - Datasets are historical field measurements with specific sampling protocols and taxonomic references.
  - Data are intended for discovery and reuse, with documentation linking to published handbooks and flora references.

- Documentation and provenance:
  - Methods and data are anchored to the Sourhope Field Data Handbook (2003) and Stace (1997).
  - Supporting information available via the EIDC catalogue; additional data from 2000 may be provided separately.

## Sampling methods

- Baseline vegetation survey (1998):
  - Timing: 27 July–7 August 1998.
  - Method: 50 x 50 cm point quadrats within randomly selected subplots; 25 points per quadrat.
  - Data: presence/absence with potential abundance records; records include species observed at each point down to the soil surface.
  - Subplot selection: five subplots per main plot (A–F) across five blocks (1–5).

- Point quadrat data (2000–2002):
  - Method: per-year sampling using a 0.5 m^2 cell within each sub-plot; grid of 100 holes; a pin dropped through 25 holes per sampling event.
  - Data: record of each occasion a species is touched by the pin; later years included bryophyte species-level identification (2002).
  - Investigators: S. Buckland, W. Walker, G. Burt-Smith.

## Data structure

- Baseline vegetation (1998): P2109_BOTANICAL_SURVEY_BASELINE_1998.csv
  - MEAS_LOC_ID, BLOCK, MAIN_PLOT, SUB_PLOT
  - BASE_DATE: date of baseline sampling
  - SPECIES_CODE, SPECIES_NAME (Stace, 1997)
  - ABUNDANCE: total hits by sub-plot

- Point quadrat data (2000–2002): P2109_BOTANICAL_SURVEY_2000_2002.csv
  - YEAR, SAMPLE_DATE
  - BLOCK, MAIN_PLOT, SUB_PLOT
  - TREATMENT_NO, TREATMENT (soil treatment details)
  - SPECIES, SPECIES_COUNT (total hits by sub-plot)

- Metadata and references:
  - Reference framework: Scott et al., 2003 (Sourhope Field Data Handbook 2003)
  - Taxonomic reference: Stace, 1997 (New flora of the British Isles)

## Data quality and governance

- Quality control:
  - Numeric range checks, data formatting conformity, and logical integrity checks applied to datasets.

- Legal and responsibility notes:
  - NERC does not warrant the accuracy of the data and disclaims liability for any use of the data.
  - Data are provided with no guarantee of fitness for a particular purpose; users should assess suitability for their applications.

- Availability and provenance:
  - Data are available via the EIDC catalogue record.
  - Additional 2000 data are noted as part of ongoing or separate data provision.

## Documentation and provenance

- The datasets are anchored in published field methods and flora references, ensuring traceability to documented protocols.
- Original field team and data collection context are identified (e.g., Buckland, Walker, Burt-Smith).
- Links to supporting information and data handbooks reinforce data provenance and reuse potential.