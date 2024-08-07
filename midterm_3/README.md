# Project: Car Accident Risk Assessment System

## Project Description

As a Data Science specialist at a car-sharing company, I created a system to assess the risk of car accidents on selected routes. The system evaluates the risk level once a driver selects a route, and if the risk is high, it provides warnings and recommendations.

### Objective

The goal was to determine if it's possible to predict accidents based on historical data from one region and to develop a model for assessing driver risk.

### Steps Taken

1. **Data Loading and Exploration**
    - Connected to the database and loaded tables using SQL.
    - Explored the tables to ensure data completeness and identified common keys for linking tables.

2. **Statistical Analysis of Accident Factors**
    - Analyzed monthly accident trends and created visualizations.
    - Identified critical analytical tasks for team members, such as analyzing vehicle damage severity and common accident causes.

3. **Model Development for Risk Assessment**
    - Prepared the dataset based on initial assumptions: selected car-related accidents with significant damage, using data from 2012.
    - Conducted statistical analysis to select relevant factors, such as party type and sobriety level.

4. **Model Selection and Evaluation**
    - Developed multiple models with hyperparameter tuning.
    - Selected the best model based on business-related metrics and created a comparative table of results.

5. **Model Testing and Analysis**
    - Conducted a confusion matrix analysis and plotted precision and recall.
    - Analyzed the importance of key factors influencing accident probability.
    - Conducted additional research on the most important factor, party sobriety, and suggested equipping cars with breathalyzers and cameras.

6. **Conclusion**
    - Summarized the best model and evaluated the feasibility of creating an adequate risk assessment system.
    - Identified additional factors for future data collection to improve the model.

## Tables Used

- **collisions**: General information about accidents with a unique `case_id`.
- **parties**: Information about accident participants with non-unique `case_id` matching the `collisions` table.
- **vehicles**: Information about damaged vehicles with non-unique `case_id` and `party_number` matching the `collisions` and `parties` tables.

## How to Use

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/car-accident-risk-assessment.git
    ```
2. Navigate to the project directory:
    ```bash
    cd car-accident-risk-assessment
    ```
3. Open the Jupyter notebook to explore the analysis and models:
    ```bash
    jupyter notebook notebooks/analysis.ipynb
    ```

## Contact

For any questions or suggestions, feel free to reach out:
- **Email**: [your email]
- **LinkedIn**: [your LinkedIn profile]
