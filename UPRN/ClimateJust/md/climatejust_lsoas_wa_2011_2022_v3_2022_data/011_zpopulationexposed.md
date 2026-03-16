The field **'Population Exposed (Z-Score)'** (internal name `zpopulationexposed`) represents the standardized score for the number of people exposed to flooding within an LSOA.

### Description

This field converts the raw count of exposed people into a Z-score to allow for relative comparison across all Welsh neighbourhoods. A score of zero represents the Welsh average.

* **Assumption:** Positive values denote that more people are potentially exposed than the average Welsh neighbourhood; higher scores represent higher overall exposure risk.
* **Vulnerability Dimension:** This informs the **Population Exposure and Disadvantage** dimension.
* **Caveat:** Z-scores are relative to the specific population distribution of Wales and cannot be used to compare directly with other countries without re-standardization.
* **Data Source:** Standardized calculation derived from the **Population Exposed (Count)**.
