### 1. Evacuation Percentage Map

Hurricane Ida, New York — Evacuation rate by ZIP code: https://vaidehiraipat.github.io/Visualizing-evacuation-displacement-and-inflow/maps/ida_ny_ZIPlevel_maps/ny_zip_evacuation_rate.html

The **Evacuation Percentage Map** shows the share of users from each affected origin county who temporarily moved away from their established pre-disaster home during or immediately after the disaster.

The evacuation percentage is calculated as:

```math
\text{Evacuation Percentage}
=
\frac{\text{Evacuated users}}
{\text{Users in the pre-disaster cohort}}
\times 100
```

---

### 2. Displacement Map: Disaster vs. Comparable Non-Disaster Period

Hurricane Ida, New York — Destination rate by ZIP code: https://vaidehiraipat.github.io/Visualizing-evacuation-displacement-and-inflow/maps/ida_ny_ZIPlevel_maps/ny_zip_destination_rate.html

A user is classified as displaced when their later HOME is located in a different county from their pre-disaster HOME.

For each origin-destination pair:

```math
\text{Displacement Rate}_{od}
=
\frac{\text{Users moving from origin }o\text{ to destination }d}
{\text{All users from origin }o\text{ with a valid later HOME}}
\times 100
```

Same-county stayers are included in the denominator but are not shown as displacement flows.

The disaster-period displacement pattern is displayed alongside the **comparable non-disaster period**, calculated using the same HOME-based methodology.

---

### 3. Destination Inflow Percentage Map

Hurricane Ida, New York — Inflow by ZIP code: https://vaidehiraipat.github.io/Visualizing-evacuation-displacement-and-inflow/maps/ida_ny_ZIPlevel_maps/ny_zip_inflow.html 

The **Destination Inflow Percentage Map** shows which counties received displaced users.

For each destination county:

```math
\text{Inflow Percentage}_{d}
=
\frac{\text{Displaced users arriving in destination }d}
{\text{Cuebiq HOME users in destination }d\text{ during the pre-period}}
\times 100
```

The map is colored by the disaster-period inflow percentage.

Hover information reports the disaster-period inflow, comparable non-disaster-period inflow, and the difference between the two.

#### Excess inflow

For each destination ZIP $z$, excess inflow is the difference between its inflow rate in a post-IDA month $t$ (September or October 2021) and its July 2021 (Non-IDA month) inflow rate, measured in **percentage points**.
https://vaidehiraipat.github.io/Visualizing-evacuation-displacement-and-inflow/maps/ida_ny_ZIPlevel_maps/ny_zip_excess_inflow.html

$$
\Delta I_{z,t}
= I_{z,t} - I_{z,\mathrm{July}}
= 100 \times \frac{A_{z,t} - A_{z,\mathrm{July}}}{N_{z,\mathrm{August}}}
$$

---

### 4. Inflow-Distance Plot

The **Inflow-Distance Plot** examines how destination inflow changes with distance from the disaster-affected region.

For each destination county, distance is measured from its centroid to the **nearest affected origin-county centroid** using great-circle distance.

Excess inflow is defined as:

```math
\text{Excess Inflow}_{d}
=
\text{Inflow Percentage}_{d,\text{disaster}}
-
\text{Inflow Percentage}_{d,\text{non-disaster}}
```

Destination counties are grouped into distance bands, and the plot reports the median excess inflow with **95% bootstrap confidence intervals**.

<img width="960" height="407" alt="NIH_NY_IDA_ZCTA" src="https://github.com/user-attachments/assets/768f2945-fc7a-4014-8e5e-49aeb3d8ee83" />
