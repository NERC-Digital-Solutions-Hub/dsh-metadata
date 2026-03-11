### People lacking easy GP access (%) (Z-Score)

**Description:**
This field (identified internally as `ZPeopleLackGPAccess` in the spatial dataset) represents the standardized score (Z-score) for the percentage of the population that lacks easy access to a General Practitioner (GP) within a given Lower Super Output Area (LSOA). 

**Vulnerability Context:**
This indicator is a key component of the "GP Access" domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial vulnerability indices. 

The core assumption behind this metric is that communities with higher proportions of people lacking easy access to primary medical care are more socially vulnerable. During and after extreme weather events—such as heatwaves or floods—individuals may suffer from severe health impacts (like heat stress) and require rapid medical assistance. A lack of easy access to a GP significantly hinders a community's capacity to access this vital help and successfully recover.

**Interpretation:**
Because this field is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote areas with a *higher* percentage of people lacking easy GP access compared to the national average. This indicates poorer access to medical support and translates to **higher social vulnerability**.
*   **Negative values (Low scores):** Denote areas with a *lower* percentage of people lacking easy access compared to the average. This indicates better, more reliable access to primary medical care and, therefore, **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data used to calculate this standardized score is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0505: Travel time, destination and origin indicators for GPs by mode of travel).