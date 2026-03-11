### People in overcrowded households (%) (Z-Score)

**Description:**
This field (identified internally as `ZOvercrowding` in the spatial dataset) represents the standardized score (Z-score) for the level of household overcrowding within a given Lower Super Output Area (LSOA). 

**Vulnerability Context:**
This indicator is a key component of the **Housing Characteristics** domain, which feeds into the **Enhanced Exposure** dimension of the Socio-Spatial Heat Vulnerability Index (SSHVI). 

The core assumption is that overcrowded living conditions and high housing density severely accentuate the impacts of extreme weather events, particularly heatwaves. Dwellings with too many occupants relative to their size tend to get disproportionately hot and lack the necessary space or ventilation for residents to effectively cool down, leading to increased heat stress and higher social vulnerability. 

**Interpretation:**
Because this field is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote an area with a *higher* rate of household overcrowding compared to the national average. This indicates an environment that enhances exposure to extreme heat, translating to **higher social vulnerability**.
*   **Negative values (Low scores):** Denote an area with *lower* rates of overcrowding compared to the average, indicating better living conditions and **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the underlying data used to calculate this standardized score is derived from the Index of Multiple Deprivation (IMD) 2019 (specifically, the Household overcrowding indicator).