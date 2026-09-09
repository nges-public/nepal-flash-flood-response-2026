# NGES Volunteer Guide

Welcome to the **NGES Nepal Flash Flood Response 2026** volunteer mapping initiative.

This repository coordinates GIS volunteers supporting rescue, relief and early recovery by producing standardized geospatial datasets across flood-affected districts in Nepal.

---

## Our Mission

To collaboratively create accurate, validated and openly accessible spatial data that supports humanitarian response and informed decision-making.

Current priority datasets include:

- Temporary Holding Centres
  
---

# Getting Started

## Requirements

Before contributing, ensure you have:

- A GitHub account
- Any GIS software (QGIS, ArcGIS, or equivalent) **or Google Earth Pro**
- Basic map interpretation and digitization skills

## Step 1: Claim a Task

1. Open the **Issues** tab.
2. Find an unassigned task.
3. Comment that you would like to take the task.
4. Wait for assignment from an NGES coordinator.

Please work only on assigned municipalities to avoid duplicate mapping.

---

# Mapping Standards

## Coordinate Reference System

All datasets must use:

**EPSG:4326 (WGS 84)**

## Geometry Types

| Dataset | Geometry |
|----------|----------|
| Holding Centres | Point/Polygon |


## Required Attributes

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

Do **not** rename or delete attribute fields.

---

# Data Sources

Prioritize authoritative sources whenever possible.

Preferred sources include:

- Municipal governments
- District Administration Offices
- Official emergency notices
- Satellite imagery 
- OpenStreetMap (reference only)

Always record the source in the attribute table.

---
## Satellite Imagery

Use the following imagery for digitization:

| Priority | Imagery | Use |
|----------|----------|-----|
| ⭐ Primary | Esri World Imagery | Digitizing holding centres  |
| Secondary | Google Earth Pro | Digitizing holding centres  |

**Guidelines**

- Use the most recent imagery available.
- Digitize the building footprint or the centre point when the exact footprint is unclear.
- Verify the location with official municipal information whenever possible.
- Do not digitize temporary tents unless they are confirmed as official holding centres.

# Quality Checklist

Before submitting your work, verify that:

- [ ] Geometry is accurate.
- [ ] No duplicate features exist.
- [ ] Required attributes are completed.
- [ ] CRS is EPSG:4326.

---

# Protecting Sensitive Information

This repository is **public**.

Never upload personally identifiable information (PII).

Do **NOT** include:

- Names of displaced individuals
- Phone numbers
- Citizenship or ID numbers
- Household records
- Medical information

Our objective is to map **facilities and infrastructure**, not people.

---

# Submitting Your Work

1. Create a new branch for your individual task.
2. Save your dataset in the appropriate folder.
3. Commit with a clear message.

Example:

`Add holding centres for Uttargaya Municipality`

4. Open a Pull Request.
5. Wait for validation before merging.

---

# Need Help?

If you encounter uncertainty about a location or attribute:

- Open a GitHub Issue with the **question** label.
- Tag the NGES committee team member.
- Do not guess unknown information—leave the field blank if it cannot be verified.

---

Thank you for contributing your time and expertise to support humanitarian response through open geospatial collaboration.

**Nepal Geomatics Engineering Society (NGES)**  
*Nepal Flash Flood Response 2026*
