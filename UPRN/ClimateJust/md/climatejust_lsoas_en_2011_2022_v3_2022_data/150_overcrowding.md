### Household overcrowding indicator

**Description:**
This field (identified internally as `Overcrowding` in the spatial dataset) represents the raw indicator score for the level of household overcrowding within a given Lower Super Output Area (LSOA). 

**Vulnerability Context:**
This indicator is a core component of the **Housing Characteristics** domain, which feeds into the **Enhanced Exposure** dimension of the socio-spatial vulnerability indices. 

The underlying assumption is that overcrowded living conditions and high housing density severely accentuate the impacts of extreme weather events. During heatwaves, for example, dwellings with too many occupants relative to their size tend to get disproportionately hot and lack the necessary space or ventilation for residents to effectively cool down, leading to increased heat stress and higher social vulnerability. 

**Interpretation:**
Unlike its standardized Z-score counterpart, this field provides the raw indicator value for the neighbourhood:
*   **High values:** Denote an area with a high rate of household overcrowding. This indicates a built environment that enhances exposure to extreme heat and flooding, translating to **higher social vulnerability**.
*   **Low values:** Denote an area with low rates of overcrowding, indicating better living conditions and **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the data used for this indicator is derived from the Index of Multiple Deprivation (IMD) 2019 (specifically, the "Household overcrowding indicator").