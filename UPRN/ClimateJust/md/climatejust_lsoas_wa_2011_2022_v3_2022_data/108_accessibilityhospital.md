The field **'Mean distance to nearest A&E Hospital (km)'** (internal name `accessibilityhospital`) represents the linear distance from a neighbourhood's centroid to the nearest hospital with an Accident and Emergency (A&E) department.

### **Description**
This metric is used to evaluate secondary medical access, which is vital for recovering from severe heat-related emergencies (e.g., heatstroke). Large distances to hospitals identify "medical deserts" where recovery from heat stress may be dangerously delayed.

*   **Assumption:** neighbourhoods located further from emergency medical facilities are more socially vulnerable because residents face greater physical barriers to obtaining critical care.
*   **Vulnerability Dimension:** This indicator informs the **Ability to Recover** dimension.
*   **Caveat:** Linear (Euclidean) distance is an estimate and does not reflect actual travel times on the road network.
*   **Data Source:** Derived from **hospital location data** and **population weighted centroids**.
