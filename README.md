# Amazon Attrition Lens

AI solution 05 of 14 · HR · built for **Amazon (Fulfillment Operations)**

Prepared by **K Bhargav Raju**.

## Problem statement

Employee turnover has increased significantly, creating recruitment costs and operational disruption. Develop an AI system that integrates employee performance, workload, compensation, absenteeism, overtime, engagement and training data to identify organizational factors associated with attrition and recommend evidence-based retention interventions.

## Why Amazon (Fulfillment Operations)

Amazon's fulfillment and delivery workforce has well-documented high turnover, which drives up hiring and training cost and disrupts sites. This tool finds which conditions cause exits and what to change first.

## Algorithm

1. **Integrate HR data**: Performance, workload, pay, absence, overtime, engagement, training
2. **Engineer features**: Overtime level, pay gap to market, months since promotion
3. **Train attrition model**: Logistic regression, 70/30 split
4. **Rank drivers**: Permutation importance on held-out data
5. **Causal check**: Propensity score matching: does heavy overtime cause exits?
6. **Manager hotspots**: Attrition by manager vs company rate
7. **Exit interview themes**: Keyword grouping of exit comments
8. **Interventions**: Simulate policy changes with the model

## Data

2,400 associates across 4 job families and 48 managers, 12 months of HR records (sample data). All figures are illustrative and are not Amazon (Fulfillment Operations)'s actual numbers.

## How to use

Open `index.html` in any web browser. No installation is needed; the whole tool is one self-contained file.

The controls panel lets you change weekly overtime cap, raise for staff >5% under market, cost to replace one associate, and the analysis reruns instantly. "New sample data" generates a fresh dataset.

## AI analyst panel

The "Ask the AI analyst" panel answers questions about the results in plain English through Claude. It works when the page is opened as a Claude artifact on claude.ai. Opened from GitHub, GitHub Pages or a local folder, all the models, charts and controls still run, and the panel shows that it is unavailable.
