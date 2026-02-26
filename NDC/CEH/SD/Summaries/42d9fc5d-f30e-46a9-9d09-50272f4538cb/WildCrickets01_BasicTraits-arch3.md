# WildCrickets01-BasicTraits Description of content

- Overview: This file includes basic information on each adult tagged individual in the population for a set of traits, enabling individual-level monitoring and subsequent analyses of population dynamics.

- Data fields and meanings:
  - Year: The year when the cricket was alive.
  - Tag: The two-character code used to identify the cricket in the video recordings; read from a plastic tag attached to the cricket’s pronotum.
  - Sex: The sex of the cricket (Male or Female).
  - Emerged: The date when the cricket emerged as an adult; may be empty if unknown.
  - Tagged: The date when the cricket was caught for the first time and tagged.
  - Dead: The date when the cricket died, or the last time it was observed if death is not recorded.
  - ThoraxWidth: The width of the thorax, measured from a picture taken from above.
  - BodyMass: The mass of the cricket on the date when it was tagged.
  - Monitored: The number of days this individual cricket has been under observation.

- Data collection and measurement methods:
  - Identification: Each cricket carries a plastic tag read from video recordings to assign the Tag code.
  - Morphometrics: ThoraxWidth is obtained from measurements on a top-down image.
  - Mass: BodyMass is recorded at the tagging date.
  - Temporal data: Emerged, Tagged, and Dead dates provide life-stage timing and survival information.
  - Monitoring effort: Monitored indicates the duration of continuous observation for each individual.

- Data quality and handling notes:
  - Emerged may be left empty if the emergence date is unknown.
  - Dead may be empty if death was not recorded, with the last observation serving as a proxy.
  - The dataset relies on accurate tagging, image-based measurements, and timely recording of dates.

- Purpose for monitoring frameworks:
  - Facilitates individual- and population-level monitoring of life history traits, growth, and survival.
  - Supports alignment of identity, timing, and physical measurements across the study period.
  - Provides a basis for linking observational effort (Monitored) to analyses of data completeness and reliability.