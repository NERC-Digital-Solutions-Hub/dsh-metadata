### Lack of domestic gardens (% dwellings without gardens) (Z-Score)

**Description:**
This field (identified internally as `ZLackPrivateGreenspaceHeat` and `ZLackPrivateGreenspaceFlood` in the spatial dataset) represents the standardized score (Z-score) for the percentage of residential dwellings that do not have access to a private domestic garden within a given Lower Super Output Area (LSOA). 

**Vulnerability Context:**
This indicator is a key component of the **Physical Environment** domain within the **Enhanced Exposure** dimension of both the socio-spatial heat and flood vulnerability indices. 

The core assumption behind this metric is that domestic gardens provide vital environmental services that offset the impacts of climate hazards. Gardens offer essential cooling functions during severe heatwaves and act as permeable surfaces that improve water drainage during heavy rainfall. Consequently, neighbourhoods with a high proportion of homes lacking private gardens are more likely to experience accentuated, severe impacts from these extreme weather events.

**Interpretation:**
Because it is presented as a standardized Z-score, it evaluates how a specific neighbourhood's lack of garden space compares to the overall average across England:
*   **Positive values (High scores):** Denote an area with a *higher* percentage of dwellings without gardens compared to the national average. This indicates an environment that accentuates hazard exposure, translating to **higher social vulnerability**.
*   **Negative values (Low scores):** Denote an area with a *lower* percentage of dwellings without gardens (i.e., a higher proportion of homes possess private gardens) compared to the average. This indicates an environment that helps offset hazard exposure, translating to **lower vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the underlying data used to calculate this standardized score is derived from the Office for National Statistics (ONS) Greenspace dataset (Access to public green space in Great Britain).