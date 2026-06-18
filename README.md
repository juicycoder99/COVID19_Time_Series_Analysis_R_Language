# Programming Languages for Data Analysis (CS504) — Assignment 2

Coursework for **Programming Languages for Data Analysis (CS504)**, Department of Computer Science,
Bishop's University.

## COVID-19 analysis translated from Python to R

The assignment provides a complete Python (pandas / scikit-learn) analysis of the Johns Hopkins
CSSE global confirmed-cases series and asks for the **equivalent R code of the entire work**.

The R solution is in [`Assignment_2_R.ipynb`](Assignment_2_R.ipynb) (Jupyter, R kernel).

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
# open Assignment_2_R.ipynb with a Jupyter R kernel (IRkernel), or run the code in RStudio
```

## Files

| File | Description |
|------|-------------|
| `Assignment_2_R.ipynb` | R solution (the deliverable) |
| `Assignement_2_student.pdf` | Assignment description with the original Python work |
| `time_series_covid19_confirmed_global.csv` | Source dataset (JHU CSSE) |
