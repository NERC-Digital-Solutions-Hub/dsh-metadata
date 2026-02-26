# WildCrickets01-BasicTraits Description of content

## Overview
- Describes basic information on each adult tagged cricket in the population across key traits.
- Provides attributes suitable for GIS-linked analyses when combined with location data.

## Fields included (attributes)
- Year: Year when the cricket was alive.
- Tag: Two-character code identifying the cricket in video recordings.
- Sex: M or F.
- Emerged: Date the cricket emerged as an adult (may be blank if unknown).
- Tagged: Date when the cricket was first caught and tagged.
- Dead: Date of death, or last observed date if death is not recorded.
- ThoraxWidth: Thorax width measured from a top-down image.
- BodyMass: Mass at the date the cricket was tagged.
- Monitored: Number of days the individual was observed.

## Data quality and handling
- Missing values: Emerged can be blank when unknown; Dead may be blank if death is not recorded.
- Measurements: BodyMass is tied to tagging; Monitored is a derived duration.
- Ensure consistent date formats and units when integrating with other datasets.

## GIS relevance and potential analyses
- Can be linked to spatial data if coordinates/locations are available for each cricket.
- Supports GIS analyses of demographics, growth (ThoraxWidth), body condition (BodyMass), and survival (Dead) over time.
- Useful for map visualizations when filtering by Sex, Year, or Tag.

## Practical considerations for integration
- Use Tag as a stable identifier across datasets.
- Validate date fields and compute derived metrics (e.g., Monitored duration, time since Emerged).
- Align with time-enabled maps by synchronizing dates with capture and observation events.