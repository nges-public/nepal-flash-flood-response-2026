# Temporary Holding Centres

This folder contains geospatial data of temporary holding centres established or identified for people evacuated from areas affected by the 2026 Nepal Flash Flood and associated landslides.

The objective is to create a standardized and validated dataset of holding centres that can support rescue, relief distribution, resource planning and humanitarian coordination.

---

## Mapping Objective

Volunteers are requested to identify and map temporary holding centres within the affected areas.

---

## What is a Holding Centre?

For this project, a **temporary holding centre** refers to a location where evacuated or displaced people are temporarily accommodated following the flash flood event.

Examples may include:

- Schools
- Community halls
- Government buildings
- Monasteries or religious facilities
- Temporary shelters
- Other facilities officially designated for temporary accommodation

Only map locations that are being used or have been identified as temporary holding centres for this emergency response.

---

## Data Structure

Each mapped holding centre should contain the following attributes:

| Field | Description | Required |
|---|---|---|
| `hc_id` | Unique holding centre ID | Yes |
| `name` | Name of the holding centre | Yes |
| `district` | District where the centre is located | Yes |
| `municipality` | Municipality where the centre is located | Yes |
| `ward` | Ward number | Yes |
| `building_type` | Type of facility | Yes |
| `estimated_capacity` | Estimated number of people the centre can accommodate | If available |
| `current_population` | Current number of people staying at the centre | If available |
| `status` | Current operational status | Yes |
| `source` | Source of the information | Yes |
| `remarks` | Additional relevant information | Optional |

---

## Geometry

Holding centres should be mapped as **polygon or point features**, with **polygon being the first priority**.

### Polygon — First Priority

Map the **building footprint** of the holding centre as a polygon whenever it can be clearly identified.

- Trace the building footprint as accurately as possible using available imagery.
- If the holding centre occupies a specific building within a larger complex, map only the relevant building.
- Do not include surrounding roads, open spaces, or unrelated buildings.
- Use the most recent and suitable imagery available.

### Point — When Polygon Is Not Possible

Use a point when the building footprint cannot be clearly identified.

- Place the point at the centre of the facility when its location can be clearly identified.
- Use the approximate location when the exact facility location cannot be determined.
- Use the reported location when information is obtained from an authoritative source.

**Mapping priority: Polygon → Point**

Do not create both a polygon and a point for the same holding centre. Do not create multiple points for the same holding centre.

---

## Recommended Imagery

Use the most recent and suitable imagery available for identifying the location of facilities.

Recommended sources:

1. **Esri World Imagery**
2. **Google Earth / Google Earth Pro**
3. Other reliable satellite or aerial imagery where appropriate

Imagery should be used together with available official information wherever possible.

---

## Information Sources

Prioritize authoritative and verifiable sources.

Examples include:

- Local government / municipality
- District Administration Office
- Nepal Government agencies
- Official emergency response updates
- Reliable satellite or aerial imagery

Always record the source in the `source` field.

If information comes from a person or organization, record the organization or source type rather than personal contact details.

---

## Capacity and Population

### Estimated Capacity

Record the maximum number of people that the holding centre is estimated to accommodate.

### Current Population

Record the number of people currently staying at the holding centre at the time the information was collected.

If the information is not available, **leave the field blank**.

Do not make assumptions or estimates unless the source explicitly provides an estimate.

---

## Status

Use one of the following values:

| Status | Description |
|---|---|
| `Active` | Currently being used as a holding centre |
| `Inactive` | Previously used but no longer operating |
| `Planned` | Identified/designated but not yet operational |
| `Unknown` | Status cannot be verified |

---

## Data Quality Requirements

Before submitting your data, make sure:

- [ ] The holding centre is within the assigned municipality.
- [ ] The location is accurate.
- [ ] Duplicate facilities have not been mapped.
- [ ] All required attributes are completed.
- [ ] Capacity and population values are sourced.
- [ ] The data uses the required CRS.
- [ ] The source of information is recorded.
- [ ] No personally identifiable information (PII) is included.
- [ ] The dataset has been checked before submission.

---

## Sensitive Information

This repository is public.

**Do not include personally identifiable or sensitive information about displaced people.**

Do not record:

- Names of displaced people
- Phone numbers
- Citizenship or identification numbers
- Household-level information
- Medical information
- Personal photographs without appropriate authorization

The purpose of this dataset is to map **holding centres and their operational information, not individual evacuees**.

---

## File Format

The preferred format for spatial data is:

**GeoPackage (`.gpkg`)**

Use the following naming convention:

`<district>_<municipality>_holding_centres.gpkg`

Example:

`rasuwa_dhunche_holding_centres.gpkg`

---

## Folder Structure

Organize the data as follows:

```text
01_holding_centres/
│
├── README.md
│
├── data_template/
│   └── holding_centres_template.gpkg
│
├── digitized_layers/
│   ├── rasuwa/
│   ├── nuwakot/
│   ├── dhading/
│   ├── chitwan/
│   ├── gorkha/
├── └── tanahun/
