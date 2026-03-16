The field **'Disadvantage (all potentially exposed, Z-Score)'** (internal name `zdisadvantageexposed`) represents the final flood disadvantage score, taking into account all people living in the floodplain regardless of defenses.

### **Description**
This is a composite measure of **geographic flood disadvantage**, calculated by combining the degree of exposure (total population in the floodplain) with the social vulnerability (SSFVI) of the neighbourhood.

*   **Assumption:** True disadvantage occurs where high social vulnerability and physical exposure to flooding coincide; an area with high social vulnerability but no exposure is not "disadvantaged" in this specific hazard framework.
*   **Vulnerability Dimension:** This is the primary output of the **Population Exposure and Disadvantage** assessment.
*   **Caveat:** This score treats all potentially exposed residents equally, irrespective of whether they are currently protected by defenses.
*   **Data Source:** An equally weighted combination of the **SSFVI** and the **Population Exposed (Z-Score)**.
