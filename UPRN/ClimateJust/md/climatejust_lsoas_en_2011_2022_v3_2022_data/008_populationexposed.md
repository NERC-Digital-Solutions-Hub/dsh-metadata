### Population Exposed (Count)

**Description:**
This field represents the estimated count of the population living within a designated flood zone in a given Lower Super Output Area (LSOA), irrespective of whether those areas are protected by existing flood defences. 

**Methodology and Data Source:**
This metric provides a broad, area-based indicator of population exposure rather than a property-level assessment. It is calculated using the following approach:
*   **Hazard Data:** It merges all flood types and return periods, specifically utilizing the Environment Agency's Flood Map for Flood Zones 2 and 3, which account for river, coastal, and surface water flooding.
*   **Population Data:** The flood zones are overlaid with a 10-meter gridded population dataset (OpenPopGrid, based on 2011 population estimates). The population counts within these 10m cells are then attributed to the flood zones and aggregated up to the LSOA level. *(Note: Minor data cleaning was applied to remove spurious counts of fewer than 2 people per 10m cell)*

**Application:**
This field serves as the baseline measure of physical hazard exposure within the dataset. When this exposure count is combined with a neighbourhood's social vulnerability score (the Socio-Spatial Flood Vulnerability Index, or SSFVI), it is used to calculate the overall "flood disadvantage" of the LSOA.