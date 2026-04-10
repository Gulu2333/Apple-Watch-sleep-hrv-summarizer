<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Apple Health Sleep &amp; Physiology Analyzer – Description and Usage</title>
</head>
<body>
  <h1>Apple Health Sleep &amp; Physiology Analyzer – Description and Usage</h1>

  <img src="demo.png"
       alt="Example Apple Health sleep analysis figure"
       style="max-width: 100%; height: auto;">

  # Apple Health Sleep & HRV Analyzer

This script analyzes an Apple Health `export.xml` file to produce a complete set of publication-ready figures (APA 7th styling) and a structured technical report. It specifically focuses on the interplay between sleep stages and physiological signals like Heart Rate (HR), Heart Rate Variability (HRV), and Blood Oxygen (SpO2).

## Core Features

* **Efficient Parsing:** Stream-parses large Apple Health XML files using iterative logic to minimize memory usage.
* **Data Alignment:** Merges fragmented sleep intervals into complete sessions and aligns them with high-frequency HR, HRV (SDNN), and SpO2 records.
* **Advanced Physiology Analysis:** Analyzes physiological shifts during sleep stage transitions and calculates regression curves relative to sleep onset.
* **Academic Standards:** Automatically applies APA 7th-style plotting (Arial font, 300 DPI, greyscale) for all exported visuals.

## Comprehensive Figure Index

The analyzer generates a complete suite of **15 publication-ready figures** included in the output:

1.  **Figure 1. Record Counts:** Cumulative frequency of extracted records for Heart Rate, HRV, SpO2, and Sleep Stages.
2.  **Figure 2. Temporal Coverage:** Longitudinal record density illustrating data collection continuity over time.
3.  **Figure 3. Value Distributions:** Histograms of physiological metrics featuring interquartile range (IQR) outlier fences.
4.  **Figure 4. Sleep Session Diagnostics:** Distribution of merged session durations and nocturnal sleep onset frequency.
5.  **Figure 5. Sleep Physiology Regression:** Longitudinal regression analysis of HR, HRV, and SpO2 relative to hours since sleep onset.
6.  **Figure 6. HR-HRV Correlation:** Bivariate scatter plot with linear regression modeling.
7.  **Figure 7. HRV Circadian Rhythm:** 24-hour mean HRV profile depicting hourly physiological variance.
8.  **Figure 8. HRV Weekly Rhythm:** Mean HRV fluctuations categorized by day of the week.
9.  **Figure 9. HRV Monthly Rhythm:** Seasonal analysis of mean HRV variations by month.
10. **Figure 10. Stage-specific Boxplots:** Comparative distribution of HR and HRV across Awake, REM, Core, and Deep sleep stages.
11. **Figure 11. Stage-specific Violin Plots:** Visualization of probability density and distribution morphology for physiological metrics by sleep stage.
12. **Figure 12. Transition Heatmap:** Quantification of mean physiological delta (HR and HRV) during sleep stage transitions.
13. **Figure 13. Transition Time Course:** Dynamic trajectories of HR and HRV within a 10-minute window of stage boundaries.
14. **Figure 14. Single-night Hypnogram Overlay:** Synchronization of nocturnal sleep architecture with continuous HR and HRV tracking.
15. **Figure 15. Sleep Stage Proportion:** Stacked area chart illustrating the dynamic evolution of sleep stage percentages across the nocturnal period.

## Output Files

All results are saved in an `output` directory:
* **Analysis_Report.txt:** A comprehensive summary containing data overviews, descriptive statistics, and correlation test results.
* **Figures/**: A folder containing all 15 high-resolution images listed above.

## How to Use

1.  **Input:** Provide your Apple Health `export.xml` file.
2.  **Run:** Execute the `.exe` (for Windows) or the Python script (requires `pandas`, `matplotlib`, `seaborn`, `scipy`, and `numpy`).
3.  **Process:** The script will filter short naps, merge sleep sessions, and perform statistical binnings automatically.

---
*Disclaimer: This tool is intended for personal research and academic reporting, not for medical diagnosis or treatment.*

