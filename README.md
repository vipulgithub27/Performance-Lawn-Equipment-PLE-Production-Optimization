# Performance Lawn Equipment (PLE) Production Optimization

## Overview

Welcome to the Performance Lawn Equipment (PLE) Production Optimization project! This repository contains a detailed analysis and optimization report aimed at maximizing profit from the production of mower and tractor housings. Using Excel Solver, we have formulated and solved a linear programming model to determine the most profitable production strategy within the given constraints.

## Project Summary

Performance Lawn Equipment (PLE) faces the challenge of optimizing its production process to maximize profits from manufacturing mower and tractor housings. The production process involves multiple departments with limited work hours and resource constraints. This project leverages linear programming techniques to identify the optimal production quantities while adhering to these constraints.

## Problem Statement

PLE’s manufacturing facilities produce engine housings for both mowers and tractors through five departments: Stamping, Drilling, Assembly, Painting, and Packaging. The production process has the following constraints:

- **Departmental Hours Available:**
  - Stamping: 200 hours
  - Drilling: 300 hours
  - Assembly: 225 hours
  - Painting: 220 hours
  - Packaging: 100 hours

- **Resource Availability:**
  - Sheet Metal: 1440 square feet
  - Paint: 400 liters

- **Profit Margins:**
  - Mower Housing: €190 per unit
  - Tractor Housing: €260 per unit

**Objective:** Maximize the total profit from the production of mower and tractor housings.

## Methodology

### Step 1: Define the Objective

The goal is to maximize total profit, expressed as:
\[ \text{Total Profit} = 190X_1 + 260X_2 \]
Where:
- \( X_1 \) = Number of mower housings
- \( X_2 \) = Number of tractor housings

### Step 2: Decision Variables

- \( X_1 \): Units of mower housings to produce
- \( X_2 \): Units of tractor housings to produce

### Step 3: Formulate Constraints

**Time Constraints:**
- Stamping: \( 0.2X_1 + 0.3X_2 \leq 200 \)
- Drilling: \( 0.3X_1 + 0.4X_2 \leq 300 \)
- Assembly: \( 0.25X_1 + 0.35X_2 \leq 225 \)
- Painting: \( 0.17X_1 + 0.25X_2 \leq 220 \)
- Packaging: \( 0.05X_1 + 0.1X_2 \leq 100 \)

**Resource Constraints:**
- Sheet Metal: \( 1.6X_1 + 1.7X_2 \leq 1440 \)
- Paint: \( 0.1X_1 + 0.32X_2 \leq 400 \)

**Demand Constraint:**
- \( X_1 \geq 2X_2 \)

### Step 4: Optimize with Excel Solver

The model was solved using Excel Solver to determine the optimal production quantities for maximizing profit.
![image](https://github.com/user-attachments/assets/0b7212df-ef9a-4a62-b943-c95160fb9b3d)

## Results

### Optimal Production Plan
![image](https://github.com/user-attachments/assets/5a7f7162-93d2-4730-89dc-842ce0767b76)

The optimization results indicate:
- **Mower Housings (X₁):** 900 units
- **Tractor Housings (X₂):** 0 units
- **Maximum Profit:** €171,000

**Binding Constraints:**
- **Assembly Department** and **Sheet Metal** constraints are fully utilized with no slack.

**Slack Values:**
- **Painting Department:** 67 hours
- **Packaging Department:** 55 hours
- **Stamping Department:** 20 hours
- **Drilling Department:** 30 hours
- **Paint:** 310 liters

### Sensitivity Analysis
![image](https://github.com/user-attachments/assets/dc5f6e6f-4715-45f6-a375-482999e24842)

- **Current Production Plan:** 900 mowers and 0 tractors is optimal.
- **Reduced Cost:** Increasing tractor production could potentially increase profit, but the current setup is most profitable within the given constraints.
- **Shadow Price for Assembly:** €760 per additional hour, highlighting the value of increasing assembly capacity.

## Improved Model
![image](https://github.com/user-attachments/assets/eea8a3b3-9d83-4b89-a1c2-99798f42fe93)

To further enhance profitability, an improved model was developed by reallocating department hours:
- **Reduced Hours:** Painting and Packaging by 30 hours each.
- **Increased Hours:** Stamping and Assembly by 25 and 35 hours respectively.

This adjustment increased total profit by €23,000, demonstrating a more effective use of available resources.

## How to Access the Full Report

Detailed analysis and Solver formulation are provided in the Excel file `PLE_Production_Optimization.xlsx` located in this repository. This file contains:
- Formulation of the optimization model
- Solver setup and results
- Sensitivity analysis and improved model findings

You can download the file [here](link-to-your-file).

## Insights and Recommendations

1. **Production Focus:** The current optimal strategy is to produce only mower housings. Consider reevaluating if there is potential to include tractor production with adjusted resources.
2. **Resource Utilization:** Utilize slack hours in Painting, Packaging, and other departments to explore additional production opportunities.
3. **Capacity Planning:** Increase assembly capacity to further enhance profitability, as indicated by the high shadow price.


---
This README provides a clear, concise summary of the project, the methodology used, results obtained, and actionable insights, making it easy for stakeholders to understand the value and implications of the analysis.
