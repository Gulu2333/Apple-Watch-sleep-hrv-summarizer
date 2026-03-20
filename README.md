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

  <h2>Overview</h2>
  <p>
    This script analyzes an Apple Health <code>export.xml</code> file and produces a complete set of
    publication‑ready figures (APA 7th styling) and a structured text report about your sleep and related
    physiological signals. It focuses on sleep stages, heart rate, heart rate variability (HRV), and blood
    oxygen saturation (SpO2) during sleep.
  </p>

  <h2>Main Features</h2>
  <ul>
    <li>Reads and stream‑parses the large Apple Health <code>export.xml</code> file efficiently using an iterative XML parser. [cite: 40]</li>
    <li>Extracts sleep stage records, heart rate, HRV (SDNN), and SpO2 records from Apple Health data. [cite: 1]</li>
    <li>Merges fragmented sleep intervals into full “nights,” filters out short naps, and summarizes valid sleep sessions. [cite: 5, 40]</li>
    <li>Aligns heart rate, HRV, and SpO2 data with sleep stages and with time since sleep onset to study changes across the night. [cite: 6-10, 40]</li>
    <li>Identifies and analyzes sleep stage transitions and their associated physiological changes. [cite: 11-15, 40]</li>
    <li>Bins and smooths physiological data in fixed time windows to create regression curves over the course of sleep. [cite: 20, 40]</li>
    <li>Automatically generates figures for data quality, sleep regression, circadian rhythm, sleep stages, transitions, hypnograms, and stage proportions. [cite: 17-39]</li>
    <li>Applies APA 7th‑style plotting defaults for all exported figures (Arial font, 300 DPI, greyscale). [cite: 40]</li>
    <li>Writes a descriptive analysis report (<code>Analysis_Report.txt</code>) that summarizes key results and references the generated figures. [cite: 1]</li>
  </ul>

  <h2>Input Data Requirements</h2>
  <ul>
    <li>An Apple Health export created on an iPhone or Apple Watch device, saved as <code>export.xml</code>. [cite: 1, 40]</li>
    <li>The file must be a valid XML export from Apple Health; the script checks that the provided path points to an <code>.xml</code> file. [cite: 40]</li>
  </ul>

  <h2>Software Requirements</h2>
  <p>Install these Python packages before running the script:</p>
  <ul>
    <li><code>pandas</code></li>
    <li><code>matplotlib</code></li>
    <li><code>seaborn</code></li>
    <li><code>scipy</code></li>
    <li><code>numpy</code></li>
  </ul>

  <h2>How to Run</h2>
  <ol>
    <li>Open a terminal or command prompt.</li>
    <li>Change directory to the folder containing <code>apple_health_analyzer_2.py</code>.</li>
    <li>Run <code>python apple_health_analyzer_2.py</code>.</li>
    <li>When prompted, provide the path to <code>export.xml</code> (drag‑and‑drop or paste the path) and press Enter.</li>
    <li>Follow the on‑screen prompts for optional date‑range and hypnogram settings, and wait for the analysis to finish.</li>
  </ol>

  <h2>Output</h2>
  <p>All results are saved in an <code>output</code> directory created next to the script. The output includes:</p>
  
  <h3>Report and Data Summary</h3>
  <ul>
      <li><strong>Analysis_Report.txt</strong>: A comprehensive technical summary containing data overviews, descriptive statistics for all metrics, physiological analysis by sleep stage, and correlation test results. [cite: 1-16]</li>
  </ul>

  <h3>Figure Index</h3>
  <ul>
      <li><strong>Figure 1. Record Counts</strong>: Cumulative frequency of extracted records for Heart Rate, HRV, SpO2, and Sleep Stages. [cite: 17]</li>
      <li><strong>Figure 2. Temporal Coverage</strong>: Longitudinal record density illustrating data collection continuity. [cite: 18]</li>
      <li><strong>Figure 3. Value Distributions</strong>: Histograms of physiological metrics featuring interquartile range (IQR) outlier fences. [cite: 19]</li>
      <li><strong>Figure 4. Sleep Session Diagnostics</strong>: Distribution of merged session durations and nocturnal sleep onset frequency. [cite: 4, 19]</li>
      <li><strong>Figure 5. Sleep Physiology Regression</strong>: Longitudinal regression analysis of HR, HRV, and SpO2 relative to hours since sleep onset. [cite: 20]</li>
      <li><strong>Figure 6. HR-HRV Correlation</strong>: Bivariate scatter plot with linear regression modeling. [cite: 21]</li>
      <li><strong>Figure 7. HRV Circadian Rhythm</strong>: 24-hour mean HRV profile depicting hourly physiological variance. [cite: 22]</li>
      <li><strong>Figure 8. HRV Weekly Rhythm</strong>: Mean HRV fluctuations categorized by day of the week. [cite: 23]</li>
      <li><strong>Figure 9. HRV Monthly Rhythm</strong>: Seasonal analysis of mean HRV variations by month. [cite: 24]</li>
      <li><strong>Figure 10. Stage-specific Boxplots</strong>: Comparative distribution of HR and HRV across Awake, REM, Core, and Deep sleep stages. [cite: 25]</li>
      <li><strong>Figure 11. Stage-specific Violin Plots</strong>: Visualization of probability density and distribution morphology for physiological metrics by sleep stage. [cite: 26]</li>
      <li><strong>Figure 12. Transition Heatmap</strong>: Quantification of mean physiological delta (HR and HRV) during sleep stage transitions. [cite: 27]</li>
      <li><strong>Figure 13. Transition Time Course</strong>: Dynamic trajectories of HR and HRV within a 10-minute window of stage boundaries. [cite: 28]</li>
      <li><strong>Figure 14. Single-night Hypnogram Overlay</strong>: Synchronization of nocturnal sleep architecture with continuous HR and HRV tracking. [cite: 29-38]</li>
      <li><strong>Figure 15. Sleep Stage Proportion</strong>: Stacked area chart illustrating the dynamic evolution of sleep stage percentages across the nocturnal period. [cite: 39]</li>
  </ul>

  <h2>Notes</h2>
  <ul>
    <li>The script is intended for personal research and academic‑style reporting, not medical diagnosis or treatment.</li>
    <li>Large <code>export.xml</code> files can take several minutes to parse and analyze. [cite: 40]</li>
    <li>For best results, export a sufficiently long date range from Apple Health so that there are multiple nights and enough data points for statistical significance. [cite: 40]</li>
  </ul>
</body>
</html>
