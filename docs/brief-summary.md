# Assignment Brief Summary

**Course:** MAICEN-1125
**Modules:** M6U1 & U2 — Individual Parametric Building Script
**Author:** Shane Haines — Group 5
**Tools:** Grasshopper + Rhino.Inside Revit

## Overview

The assignment requires each student to build an individual parametric script in Grasshopper that generates a building massing within a user-defined site plot, and produces native Revit elements via Rhino.Inside Revit. The script must respect a set of planning and geometric constraints, and must report summary data describing the generated building.

## Design Constraints

| Parameter        | Requirement                                  |
|------------------|----------------------------------------------|
| Plot area        | 24,000 m² – 60,000 m²                        |
| Site coverage    | Less than 60% of the plot area               |
| Number of floors | 5 – 50                                       |
| Floor height     | 3 m – 5 m (floor-to-floor)                   |
| Perimeter setback| 2.4 m from the plot boundary                 |

## Required Revit Outputs

The Grasshopper script must produce the following native Revit elements through Rhino.Inside Revit:

1. **Levels** — one Revit Level per floor, positioned using the input floor-to-floor height.
2. **Floors** — Revit Floor elements hosted on each Level, matching the building footprint.
3. **Columns** — structural columns placed on a rationalised grid, spanning the full building height.
4. **Façade** — a panelised façade system (curtain wall or adaptive panels) wrapping the massing.

## Required Summary Data

The script must report:

- Gross Floor Area (GFA)
- Building footprint area
- Site coverage percentage (must be < 60%)
- Total building height
- Floor count
- Column count
- Façade panel count

## Validation

The script should visibly flag when any input combination violates the brief (for example, site coverage ≥ 60%, plot area outside 24,000–60,000 m², floor count outside 5–50, or floor height outside 3–5 m), so the user can adjust parameters before committing geometry to Revit.
