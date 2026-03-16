The field **'Disadvantage (all potentially undefended, Z-Score)'** (internal name `zdisadvantageundefended`) represents the final flood disadvantage score specifically for populations living in undefended areas.

### **Description**
This metric targets the most severe form of geographic flood disadvantage, where high social vulnerability coincides with residents who have no structural flood defenses.

*   **Assumption:** Disadvantage is most acute in neighbourhoods with high SSFVI scores and large populations living in undefended flood zones.
*   **Vulnerability Dimension:** This informs the **Population Exposure and Disadvantage** dimension.
*   **Caveat:** A null value typically indicates that either the neighbourhood is not exposed or the entire exposed population is protected by defenses.
*   **Data Source:** An equally weighted combination of the **SSFVI** and the **Exposed Population Undefended (Z-Score)**.
