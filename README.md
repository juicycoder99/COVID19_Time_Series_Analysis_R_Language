# COVID-19 Time-Series Analysis in R

End-to-end R analysis of the Johns Hopkins CSSE global confirmed-cases series, covering daily case
computation, province-level correlation, and PCA-based dimensionality reduction.

## What the notebook does

1. Load the global confirmed-cases data.
2. Keep China's rows and drop `Country/Region`, `Lat`, `Long`.
3. Compute daily confirmed cases per province (difference of consecutive cumulative days).
4. Transpose so provinces are columns and days are rows.
5. Plot the daily cases for every province, then again with the Hubei outlier removed.
6. Show the Pearson correlation between provinces as an annotated heatmap (`pheatmap`).
7. Sort and list the most correlated province pairs.
8. Run **PCA** (`prcomp`), report the explained / cumulative variance and ratios, and scatter the
   data using the first three principal components (`scatterplot3d`) and two of them.

R packages used: `pheatmap`, `scatterplot3d` (plus base R for everything else).

## Running it

```r
install.packages(c("pheatmap", "scatterplot3d"))
# open covid19_time_series_analysis_r.ipynb with a Jupyter R kernel (IRkernel), or run the code in RStudio
```

## Files

| File | Description |
|------|-------------|
| `covid19_time_series_analysis_r.ipynb` | Full implementation and analysis (R) |
| `PROJECT_BRIEF.pdf` | Project brief (goals, objectives, outcomes) |
| `time_series_covid19_confirmed_global.csv` | Source dataset (JHU CSSE) |
