# Data Analysis Notebooks

This directory contains two Jupyter notebooks showcasing end‑to‑end data analysis workflows: cleaning, exploratory analysis, visualization, and basic inference.

## Quick start

1. **Create a Python 3 environment** and install dependencies:
   ```bash
   pip install -U pandas numpy matplotlib seaborn plotly scipy statsmodels
   ```
2. **Place the required data files** in the expected locations (see “Data requirements” below).
3. **Open the notebooks** in Jupyter or VS Code and run them top‑to‑bottom.

## Files

- `Data_analysis_work_example.ipynb` — general data analysis walkthrough with EDA and simple statistical inference.
- `Alalysis_of_the_telecom_data.ipynb` — telecom customer survey analysis with cleaning, feature parsing, visualization, and inference.

## Data requirements

**Data_analysis_work_example.ipynb** expects the following CSV files (relative paths):
- Data/course_contents.csv
- Data/courses.csv
- Data/progress_phases.csv
- Data/progresses.csv
- Data/students.csv

**Alalysis_of_the_telecom_data.ipynb** expects the following CSV files (relative paths):
- megafon.csv

> Make sure these files exist before running the notebooks. If your data live elsewhere, update the `pd.read_csv(...)` paths accordingly.

## Dependencies

Core libraries detected from the notebooks:
- **Common:** pandas, numpy, matplotlib, seaborn
- **Telecom analysis:** plotly, scipy, statsmodels

Install with:
```bash
pip install -U pandas numpy matplotlib seaborn plotly scipy statsmodels
```

## Notebook overviews

### Data_analysis_work_example.ipynb
**Focus:** EDA on an education/course dataset, workload estimation, temporal trends, and basic inference.

**Sections:**
- # I. Data descripion
- # II. Calculation of the potential load on teachers
- ##### 2.1. Calculation of student growth in each course in each month for each month in the range from March 2016 to July 2019 inclusive
- ##### 2.2 line-graph with the growth of students in each month for each course. 15 charts
- ##### 2.3. line-graph with several lines reflecting the growth of students in each month for each course. 15 lines on the chart.
- ##### 2.4. Number of homework progresses in each month throughout history (each month in the range from March 2016 to July 2019 inclusive) for each course. Take into account that completing homework can flow from one month to another (such tasks must be included in the total number of progress for all months covered by the deadline for completing these tasks)
- #### data frame preparation for merging
- ##### 2.5. Plots
- ##### 2.6. All in one plot
- ##### 2.7. Conclusion
- # III. Identifying problematic modules
- ##### 3.1. Calculate the minimum, maximum, average, median time for completing each module
- ##### 3.2. line-graph with median completion time for each module for each course.
- ##### 3.3. To identify seasonality, calculate the median homework completion time by month (12 months, January-December) for each course.
- ##### 4. line-graph
- ##### 3.5. Conclusion
- ## IV. Conversion calculation
- ##### 4.1. Conversion of students' transition from one module to another in each course.
- ##### Hypotheses
- ##### 4.2. Bar-chart, reflecting the conversion of students from one module to another in each course.
- ##### 4.3. Horizontal bar-chart, reflecting the conversion of students from one module to another in each course. 15 charts.
- ##### 4.4. Conclusion
- # V. Performance metrics

**Imports used:** functools, matplotlib, numpy, pandas, seaborn

---

### Alalysis_of_the_telecom_data.ipynb
**Focus:** Cleaning and analyzing a telecom customer survey. Includes descriptive statistics, interactive charts, and simple statistical tests/regressions.

**Imports used:** matplotlib, numpy, pandas, plotly, re, scipy, seaborn, statsmodels

## How to run

```bash
# Option 1: Jupyter
python -m pip install jupyter
jupyter notebook

# Option 2: VS Code
# Install the "Jupyter" extension and open the .ipynb files directly.
```

## Reproducibility notes

- The notebooks rely on the CSV files listed above; ensure path and encoding are correct.
- Some visualizations use Plotly (interactive). If not needed, you can comment those cells out.
- If you encounter warnings about deprecated APIs or plotting backends, update the packages with `pip install -U ...`.

## Repository structure (suggested)

```
.
├── Data_analysis_work_example.ipynb
├── Alalysis_of_the_telecom_data.ipynb
├── Data/                      # input data for the first notebook
│   ├── course_contents.csv
│   ├── courses.csv
│   ├── progress_phases.csv
│   ├── progresses.csv
│   └── students.csv
└── megafon.csv                # input data for the telecom notebook
```

---

*Tip:* If you prefer a full lockfile, create one after successful runs:
```bash
pip freeze > requirements.txt
```
