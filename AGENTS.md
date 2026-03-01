# AI Coding Agent Instructions (AGENTS.md)

## Project Overview
**Project:** Strombecker 1/32 Scale Track Designer (HTML/JS)
**Goal:** A browser-based tool for designing layouts using vintage Strombecker track specifications.

## Fundamental Geometry (The "Rules")
These specifications are non-negotiable for the track logic to remain accurate:
- **Track Brand:** Vintage Strombecker (1/32 Scale).
- **Straight Section (S):** Exactly **12.125 inches**.
- **Curved Section (L/R):** Standard curve is **60 degrees** (6 pieces = full circle).
- **Outside Diameter:** **28 inches**.
- **Track Width:** **7 inches** total.
- **Lane Spacing:** **3.5 inches** between slot centers.
- **Special Piece (X):** Lane Crossover (Swaps Lane 1 and Lane 2).

## Technical Implementation Logic
- **Coordinate Tracking:** Track must calculate end position `(x, y)` and exit `angle` based on the starting state.
- **Lane Calculation:**
  - **Inside Lane Radius:** 12.25 inches.
  - **Outside Lane Radius:** 15.75 inches.
- **Crossover Logic:** When an 'X' piece is added, the "Red" and "Blue" lane identity must swap for all following pieces.

## Agent Behavior Guidelines
1. **Consistency:** Do not change the fundamental geometry constants unless explicitly requested.
2. **Code Delivery:** Always provide the **entire updated HTML file** in your response to prevent copy-paste errors and ensure the script/style blocks remain intact.
3. **Reset Awareness:** If the code breaks or produces unintended visual glitches, revert to the logic found in the last stable commit before attempting a fix.
