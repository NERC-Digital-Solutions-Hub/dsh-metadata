### Number of flats without gardens (Proxy for high-rise flats) (Z-Score)

**Description:**
This field (identified internally as `ZHighRiseHomes` in the spatial dataset) represents the standardized score (Z-score) for the number of flats or apartments that do not have access to a private domestic garden within a given Lower Super Output Area (LSOA). It is used as a proxy measure for estimating the prevalence of high-rise living (traditionally defined as households with their lowest floor on the 5th floor or above). 

**Vulnerability Context:**
This indicator is a key component of the **Housing characteristics** domain, which feeds into the **Enhanced Exposure** dimension of the Socio-Spatial Heat Vulnerability Index (SSHVI). 

The underlying assumption for this metric is that dwellings situated in the upper levels of tower blocks or multi-storey flats are significantly more likely to overheat and be adversely affected by high temperatures during heatwaves compared to ground-level or alternative types of accommodation. Consequently, a high density of these housing types in a neighbourhood physically accentuates the severity of extreme heat events for its residents.

**Interpretation:**
Because the metric is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote an area with a *higher* number of flats without gardens (indicating more high-rise or upper-floor living) compared to the national average. This points to a built environment that accentuates heat exposure, translating to **higher social vulnerability**.
*   **Negative values (Low scores):** Denote an area with a *lower* number of flats without gardens compared to the average, indicating **lower vulnerability** regarding this specific housing-related heat risk.

**Data Source:**
For the updated 2022 dataset, this indicator is calculated as a derived metric using data from the Office for National Statistics (ONS) "Access to public green space in Great Britain" dataset.