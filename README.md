# Data Science Coursework

Python notebooks exploring statistics, simulation, hypothesis testing, and Apache Spark in Databricks.

Originally developed for a data science course at the University of Mississippi. This collection includes assignment prompts, provided teaching examples, and my submitted responses and code. It is organized as coursework, with descriptive filenames and saved outputs.

## Notebooks

| Notebook | Topics |
|---|---|
| [Statistics and PySpark Fundamentals](02_statistics_and_pyspark.ipynb) | Descriptive statistics, probability, outliers, histograms, NumPy timing, Titanic DataFrame operations, and Delta storage. |
| [Sampling and Distributions](03_sampling_and_distributions.ipynb) | Plot interpretation, measurement bias, covariance, correlation, Gaussian probabilities, and simulated sampling distributions. |
| [Confidence Intervals, Skewness, and Bootstrap](04_confidence_intervals_and_bootstrap.ipynb) | Gaussian confidence intervals, skewness calculations, simulation, and bootstrap intervals. |
| [Hypothesis Tests and Spark Query Plans](05_hypothesis_tests_and_spark_plans.ipynb) | Correlation tests, proportion comparisons, and Spark logical/physical plans, lazy evaluation, grouping, and shuffles. |
| [ANOVA, Chi-Square, and Complexity](07_anova_chi_square_and_complexity.ipynb) | Permutation ANOVA, chi-square association testing, and written complexity analysis of distributed Bloom filters. |

The Olist analysis from HW6 is published separately: [Olist E-commerce Analysis](https://github.com/faridabelal/olist-ecommerce-analysis). The final exam worksheet is excluded.

## Tools

Python, Databricks, PySpark, NumPy, pandas, SciPy, Matplotlib, and Delta Lake. Individual notebooks use subsets of these tools. Some cells rely on Databricks-provided `spark`, `dbutils`, `display`, or `displayHTML`.

## Viewing and running

Open a notebook on GitHub to read the code, written explanations, and embedded outputs. To rerun, import it into Databricks, provide its supporting files, check its file paths, and run cells in order. Package/runtime versions were not recorded in the source exports, so these notebooks do not claim a pinned reproducible environment.

| Notebook | Supporting files |
|---|---|
| HW2 | `part7_samples1.csv`, `part7_samples2.csv`, Titanic `train.csv` |
| HW3 | Prompt figures: `histo.png`, `contour.png`, `boxplot.png`, and correlation figure(s); simulation code creates its own data |
| HW4 | `prob1.csv`, `prob4.csv` |
| HW5 | `lagado_breakfast_data.csv`, Titanic `train.csv` |
| HW7 | `debugging_snacks.csv` |

Supporting CSVs and original prompt images were not included in the uploads and are not bundled. Use your course materials for the course-specific data. HW2, HW5, and HW7 refer to `/Volumes/workspace/default/files/`; change these paths to your own volume. HW4 uses relative CSV paths, so place those files in its working directory or update the paths.

The source notebooks identify the [course repository](https://github.com/dosirrah/CSCI443_26S_AdvancedDataScience) and [Kaggle Titanic competition](https://www.kaggle.com/c/titanic) as data sources. These are source references retained from the coursework; availability and redistribution permissions have not been independently verified for this package.

## Review notes

- Saved outputs were preserved. No saved error outputs were found, and code cells pass Python syntax checks after one indentation fix in HW2. The package was not rerun end to end and is not a complete correctness audit of the written answers.
- HW3's absent prompt figures are marked explicitly instead of displaying broken image links. Its saved simulation plots remain available.
- HW2's saved histogram uses probability density despite its relative-frequency label; an adjacent note explains the distinction.
- HW4 includes notes distinguishing a small-sample t interval from the normal approximation, and explaining why two fixed-interval loops do not estimate repeated-sampling coverage. Original calculations remain visible as coursework.
- HW7's explanation of permutation assumptions and its largest chi-square contribution were corrected. A note explains the randomized p-value adjustment without changing the original saved outputs.
- HW7's Bloom-filter section is written complexity analysis, not an implemented or benchmarked distributed system.

Some cells are computationally expensive. HW4 includes nested bootstrap simulations, and HW7 uses 10,000 permutations. Inspect the loops before rerunning.
