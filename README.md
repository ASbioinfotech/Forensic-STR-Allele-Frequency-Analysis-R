# Forensic STR Allele Frequency Analysis Using R

## Project Overview

This project performs forensic STR allele frequency analysis using real European population STR data in R. STR, or Short Tandem Repeat, markers are widely used in forensic genetics for DNA profiling, human identification, kinship analysis, and missing person investigations.

The main objective of this project is to analyze STR allele frequency data, evaluate marker diversity, identify common alleles, and calculate expected heterozygosity for forensic STR markers.

This project demonstrates how population-level STR frequency data can be used to understand the informativeness of forensic DNA markers.

---

## Data Source

The data used in this project was accessed using the `norSTR` R package.

Dataset used:

**europeDB**

This dataset contains STR allele frequency information from European population data.

---

## Objectives

The objectives of this project are:

- Load real STR allele frequency data using R.
- Clean and structure the European STR database.
- Convert STR allele frequency data into a structured dataframe.
- Perform marker-wise allele frequency analysis.
- Identify the most common allele for each STR marker.
- Calculate the number of observed alleles per STR marker.
- Calculate expected heterozygosity.
- Generate visualizations for STR marker diversity and informativeness.
- Export results as CSV files.
- Generate a forensic-style summary report.

---

## Tools and Libraries Used

- R
- norSTR
- dplyr
- ggplot2
- readr
- tidyr

---

## Repository Structure

```text
Forensic-STR-Allele-Frequency-Analysis-R/
│
├── README.md
├── Forensic_STR_Analysis.R
│
├── data/
│   └── europe_STR_allele_frequency_data.csv
│
├── results/
│   ├── STR_marker_summary.csv
│   ├── most_common_STR_alleles.csv
│   └── STR_expected_heterozygosity.csv
│
├── figures/
│   ├── top_15_common_STR_alleles_europe.png
│   ├── STR_marker_diversity_europe.png
│   └── STR_expected_heterozygosity_europe.png
│
└── reports/
    └── forensic_STR_analysis_report.txt
```

---

## Workflow

The project follows this workflow:

1. Create project folders.
2. Install and load required R packages.
3. Load the European STR allele frequency database using `norSTR`.
4. Inspect the dataset structure.
5. Convert the STR database into a clean dataframe.
6. Save cleaned allele frequency data.
7. Generate marker-wise summary statistics.
8. Identify the most common allele for each STR marker.
9. Calculate expected heterozygosity.
10. Generate visualization plots.
11. Export analysis results.
12. Generate a forensic-style summary report.

---

## Analysis Performed

The European STR database was converted into a clean dataframe containing:

- Population
- STR marker
- Allele
- Frequency

After cleaning the data, the following analyses were performed:

- Marker-wise allele summary
- Most common allele identification
- Number of observed alleles per marker
- Expected heterozygosity calculation
- Visualization of STR marker diversity
- Visualization of STR marker informativeness
- Automated forensic-style report generation

---

## Results and Interpretation

The analysis was performed using the European STR allele frequency database available in the `norSTR` R package. The dataset was cleaned and converted into a structured table containing STR marker names, allele values, and allele frequencies.

### Marker Diversity

The marker diversity analysis showed that different STR markers have different numbers of observed alleles.

Markers with a higher number of observed alleles show greater genetic variation in the population. In forensic genetics, such markers are considered more informative because they provide more variation between individuals.

In this analysis, **SE33** showed strong allele diversity, meaning it has many observed alleles in the European STR dataset.

### Most Common STR Alleles

The analysis identified the most common allele for each STR marker.

Alleles with higher frequency are more commonly found in the population. These common alleles help describe the allele distribution of the population, but very common alleles may provide less individual discrimination compared to rare alleles.

This result shows how STR allele frequency data can be used to understand population-level DNA variation.

### Expected Heterozygosity

Expected heterozygosity was calculated for each STR marker.

Expected heterozygosity represents the probability that two randomly selected alleles from a population are different.

A higher expected heterozygosity value means:

- Higher genetic diversity
- Better marker informativeness
- Greater ability to distinguish between individuals

In this analysis, **SE33** showed the highest expected heterozygosity value of approximately **0.946**. This suggests that SE33 is one of the most informative STR markers in the European dataset.

Other highly informative STR markers included:

- **Penta E**
- **D1S1656**
- **D12S391**
- **D7S3048**
- **D18S51**

These markers showed high heterozygosity values, meaning they have strong genetic variability in the population.

### Overall Result Interpretation

The results show that STR markers are not equally informative. Some markers have higher allele diversity and higher expected heterozygosity than others.

Markers such as **SE33, Penta E, D1S1656, D12S391, D7S3048, and D18S51** may be more useful in forensic population analysis because they show greater genetic variation.

Overall, this project demonstrates how real STR allele frequency data can be used to evaluate forensic marker informativeness using R.

---

## Visualizations

This project generated three main visual outputs:

### 1. Top 15 Highest-Frequency STR Alleles

This plot shows the highest-frequency STR alleles observed in the European STR database.

Higher allele frequency means that the allele is more commonly found in the population.

This visualization helps identify which STR alleles are most frequent in the dataset.

### 2. STR Marker Diversity

This plot shows the number of observed alleles for each STR marker.

Markers with a higher number of alleles show greater genetic variation. These markers may be more informative in forensic identification because they provide more variation between individuals.

### 3. Expected Heterozygosity

This plot shows the expected heterozygosity values for STR markers.

In this analysis, **SE33** showed the highest expected heterozygosity, suggesting that it is one of the most informative STR markers in this European STR dataset.

---

## Output Files

### Cleaned STR Allele Frequency Data

**data/europe_STR_allele_frequency_data.csv**

This file contains the cleaned STR allele frequency data extracted from the European STR database.

Columns include:

- Population
- Marker
- Allele
- Frequency

---

### Marker Summary

**results/STR_marker_summary.csv**

This file contains marker-wise summary statistics.

Columns include:

- Marker
- Number of Alleles
- Maximum Frequency
- Minimum Frequency
- Mean Frequency

---

### Most Common STR Alleles

**results/most_common_STR_alleles.csv**

This file contains the most common allele identified for each STR marker.

---

### Expected Heterozygosity

**results/STR_expected_heterozygosity.csv**

This file contains expected heterozygosity values for STR markers.

Expected heterozygosity helps evaluate how informative a marker may be for forensic identification.

---

### Figures

The generated figures are stored in the `figures/` folder:

- `top_15_common_STR_alleles_europe.png`
- `STR_marker_diversity_europe.png`
- `STR_expected_heterozygosity_europe.png`

---

### Forensic Summary Report

**reports/forensic_STR_analysis_report.txt**

This file contains an automatically generated forensic-style summary report describing:

- Data source
- Analysis performed
- Total STR markers analyzed
- Total allele records analyzed
- Most informative marker
- Interpretation
- Limitations

---

## Real-Life Relevance

STR allele frequency analysis is important in forensic genetics. It helps in understanding how common or rare STR alleles are in a population.

This type of analysis supports concepts used in:

- DNA profiling
- Human identification
- Missing person identification
- Kinship analysis
- Population genetics
- Forensic marker evaluation
- Random match probability concepts

In real forensic casework, STR allele frequencies are used to estimate how common or rare a DNA profile may be in a population.

This project demonstrates the computational and statistical foundation behind forensic DNA marker evaluation.

---

## How to Run This Project

1. Download or clone this repository.
2. Open the R script file in RStudio.
3. Install the required R packages.
4. Run the script step by step.
5. The script will load the STR database, clean the data, perform analysis, generate plots, and export result files.

Main script:

**Forensic_STR_Analysis.R**

---

## Example Code

```r
library(norSTR)
library(dplyr)
library(ggplot2)
library(readr)
library(tidyr)

data(europeDB)
```

The `europeDB` dataset was used as the main STR allele frequency dataset for this project.

---

## Skills Demonstrated

This project demonstrates skills in:

- R programming
- Forensic genetics
- STR allele frequency analysis
- Population genetics
- Data cleaning
- Data transformation
- Statistical analysis
- Expected heterozygosity calculation
- Data visualization
- CSV result export
- Automated report generation
- GitHub project documentation

---

## Importance of This Project

Forensic STR analysis is an important part of forensic DNA profiling. STR allele frequency databases help forensic scientists understand how common or rare specific alleles are within a population.

This project demonstrates how computational methods can be used to analyze forensic STR data and evaluate marker informativeness.

It also shows the connection between bioinformatics, forensic genetics, statistics, and real-world DNA analysis.

---

## Limitations

This project is for educational and portfolio purposes only.

It uses public STR allele frequency data and simplified statistical analysis.

This project should not be used for real forensic casework, legal decisions, or clinical interpretation without validated forensic laboratory methods and expert review.

---

## Future Work

Future improvements may include:

- Comparing STR allele frequencies across different populations.
- Adding African, East Asian, South American, and West Asian STR databases.
- Calculating random match probability.
- Performing simulated DNA profile comparison.
- Adding parent-child compatibility analysis.
- Creating an interactive dashboard using Shiny.
- Adding more forensic statistical measures.
- Comparing forensic marker informativeness across regions.

---

## Conclusion

This project demonstrates a forensic STR allele frequency analysis workflow using R and real European STR population data. The analysis included data extraction, cleaning, marker-wise summary, most common allele identification, expected heterozygosity calculation, visualization, and automated report generation.

The results showed that STR markers differ in allele diversity and informativeness. Markers such as SE33, Penta E, D1S1656, D12S391, D7S3048, and D18S51 showed high expected heterozygosity values, suggesting strong forensic relevance in population-based STR marker analysis.

Overall, this project highlights the use of R programming, forensic genetics, population data analysis, and visualization in understanding STR marker informativeness.

---

## License

This project is licensed under the MIT License.

---

## Author

**Anushka Singh**
