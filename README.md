# grasshopper-parametric-individual

M6U1 & U2 Individual Parametric Building Script — Grasshopper and Rhino.Inside Revit | MAICEN-1125 Shane Haines Group 5

## Project Description

This project is an individual parametric building script developed in Grasshopper and linked to Revit via Rhino.Inside Revit. The script takes a user-defined site plot and a set of massing parameters, generates a parametric building envelope, and drives native Revit elements (Levels, Floors, Columns, and Façade panels) directly from Grasshopper.

The goal is to explore early-stage massing and feasibility studies where geometric logic in Grasshopper produces BIM-ready outputs in Revit, along with summary data used to validate the design against the assignment brief constraints.

## What the Script Does

- Reads a closed site plot curve and derives buildable area from a 2.4 m perimeter setback.
- Generates a building footprint constrained to a maximum site coverage of 60%.
- Extrudes the footprint into a multi-storey mass based on floor count and floor-to-floor height.
- Creates Revit Levels, Floors, structural Columns on a rationalised grid, and a Façade panel system.
- Outputs summary data (GFA, site coverage %, floor count, building height, panel count) for reporting.

## Inputs

- Site plot curve (closed polyline, 24,000–60,000 m²).
- Number of floors (5–50).
- Floor-to-floor height (3–5 m).
- Perimeter setback (default 2.4 m).
- Site coverage target (≤ 60%).
- Structural column grid spacing.
- Façade panel module dimensions.

## Outputs

- **Revit Levels** — one per floor, named and elevated per input height.
- **Revit Floors** — floor slabs generated on each Level.
- **Revit Columns** — structural columns placed on the grid, spanning all Levels.
- **Revit Façade** — panelised curtain wall / adaptive component system.
- **Summary data** — GFA, footprint area, site coverage, building height, element counts.

## Software Requirements

- Rhino 8
- Grasshopper (bundled with Rhino 8)
- Rhino.Inside Revit (latest stable release)
- Autodesk Revit 2024 or 2025

## Assignment Brief Summary

Design a parametric building script that produces a valid massing and BIM model within the following constraints:

- Plot area: 24,000–60,000 m²
- Site coverage: < 60%
- Floors: 5–50
- Floor height: 3–5 m
- Perimeter setback: 2.4 m
- Required Revit outputs: Levels, Floors, Columns, Façade
- Required reporting: summary data for the generated building

See [docs/brief-summary.md](docs/brief-summary.md) for the full brief summary.

## Folder Structure

```
grasshopper-parametric-individual/
├── README.md               # This file
├── grasshopper/            # Grasshopper definitions (.gh / .ghx)
├── screenshots/            # Renders, diagrams, and captured outputs
└── docs/                   # Supporting documentation
    └── brief-summary.md    # Assignment brief summary
```
