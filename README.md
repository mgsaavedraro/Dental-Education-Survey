# Dental Education Survey Analysis

## Overview

This repository contains the analysis of a survey conducted to assess various aspects of dental education. The study focuses on understanding the factors that influence dental education practices from the perspectives of both students and educators. The data and analysis aim to provide valuable insights into the effectiveness and challenges faced in dental education programs.

## Data Description

The dataset includes responses from dental students and faculty members from various dental schools. The main data points include:

- **Demographics**: Information about the participants, such as age, gender, and education level.
- **Academic performance**: Data related to academic achievement, satisfaction, and challenges.
- **Survey responses**: Feedback on the dental education process, the curriculum, teaching methodologies, and resources.

### Data Collection

The survey was conducted across several dental institutions and included a comprehensive set of questions. It aims to assess:

- Satisfaction with the current dental education program
- Perceived challenges in dental education
- The role of practical experience in student learning
- The adequacy of the curriculum and teaching methods

## Analysis Overview

The analysis uses several statistical methods to process the survey data, focusing primarily on multivariate techniques. Key methods applied include:

1. **Principal Component Analysis (PCA)**:
   - Used to reduce the dimensionality of the data and identify the most important factors affecting dental education.

2. **Multiple Factor Analysis (MFA)**:
   - MFA was employed to analyze and interpret relationships between different sets of data (e.g., student feedback, performance metrics, etc.).

3. **Statistical Tests**:
   - Various tests (e.g., ANOVA, regression analysis) were performed to identify significant differences and correlations in the data.

4. **Visualization**:
   - Visualizations such as biplots, scree plots, and bar charts were generated to represent the findings clearly.

## Getting Started

To get started with the project locally, follow these instructions:

### Prerequisites

Before running the analysis, ensure that you have the following installed:

- **R**: Version 4.0 or higher
- **RStudio**: To work with RMarkdown files
- **Required R Packages**: 
   - `ggplot2`, `factoextra`, `dplyr`, `tidyverse`, `rmarkdown`, `FactoMineR`, and other related packages.

Install the required R packages using the following command:

```R
install.packages(c("ggplot2", "factoextra", "dplyr", "tidyverse", "rmarkdown", "FactoMineR"))
