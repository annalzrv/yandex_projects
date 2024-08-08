# Project: Star Temperature Prediction

## Project Description

This project involves developing a neural network to predict the surface temperature of stars. The task was provided by the observatory "Sky in Your Hands," which is interested in implementing machine learning technologies to predict star temperatures, aiming for higher accuracy and convenience compared to traditional methods like Wien's displacement law, Stefan-Boltzmann law, and spectral analysis.

### Research Objectives:

* Develop a neural network model to predict the absolute temperature on the surface of stars.
* Identify key factors influencing the temperature prediction.
* Evaluate the feasibility of using neural networks for predicting star temperatures.
* Provide recommendations for improving the model, including potential additional features.

### Steps Taken

1. **Data Loading and Exploration**
    - Loaded the dataset from the file `/datasets/6_class.csv`.
    - Conducted exploratory data analysis (EDA) on quantitative and categorical data.
    - Used graphical analysis to draw insights and made necessary corrections.

2. **Data Preparation**
    - Made adjustments based on the EDA results.
    - Categorized the data where necessary.
    - Prepared training and test sets.
    - Scaled quantitative data for better model performance.

3. **Baseline Neural Network Model**
    - Created a class to define the neural network architecture.
    - Selected the number of hidden layers, neurons per layer, and activation functions for hidden and output layers.
    - Trained the neural network and plotted a "Actual vs. Predicted" temperature graph.
    - Analyzed the results.

4. **Model Improvement**
    - Implemented hyperparameter tuning for the neural network, including parameters such as dropout rate and batch size.
    - Maintained the baseline architecture for a fair comparison.
    - Retrained the neural network and evaluated the RMSE metric, ensuring it does not exceed 4500.
    - Presented the results in a table or graph for comparison.

5. **Project Conclusion**
    - Summarized the results for each model type.
    - Compared the baseline and improved models and provided conclusions.

## Entity-Relationship (ER) Description

The dataset includes characteristics of 240 studied stars with the following features:

- **Relative Luminosity (L/Lo)**: Luminosity of the star relative to the Sun.
- **Relative Radius (R/Ro)**: Radius of the star relative to the Sun.
- **Absolute Magnitude (Mv)**: Physical quantity characterizing the brightness of the star.
- **Star Color**: Color of the star (white, red, blue, yellow, yellow-orange, etc.).
- **Star Type**: Type of star.
    - Brown Dwarf (0)
    - Red Dwarf (1)
    - White Dwarf (2)
    - Main Sequence Stars (3)
    - Supergiant (4)
    - Hypergiant (5)
- **Absolute Temperature (T(K))**: Surface temperature of the star in Kelvin.

### Solution Algorithm

**Step 1: Load Source Data**
Load the source data from the file `/datasets/6_class.csv`.

**Step 2: Exploratory Data Analysis**
Conduct exploratory data analysis on both quantitative and categorical data. Use graphical analysis and draw conclusions.

**Step 3: Data Preparation for Modeling**
Make necessary adjustments based on EDA results. Categorize and scale the data, then prepare training and test sets.

**Step 4: Build a Baseline Neural Network Model**
Create a class for the neural network architecture. Experiment with different combinations of hidden layers, neurons, and activation functions. Train the model, and plot the "Actual vs. Predicted" graph for temperature.

**Step 5: Improve the Network**
Implement hyperparameter tuning, focusing on parameters such as dropout rate and batch size. Retain the baseline architecture for comparison. Train the model, and ensure the RMSE metric does not exceed 4500. Present results in a table or graph.

**Step 6: Project Conclusions**
Briefly describe the results for each model type and compare the baseline and improved models. Draw conclusions based on the comparison.

## Tables Description

The dataset used in this project includes the following columns:

- `L/Lo`: Relative Luminosity
- `R/Ro`: Relative Radius
- `Mv`: Absolute Magnitude
- `Star Color`: Color of the star
- `Star Type`: Type of star (numeric values corresponding to star types)
- `T(K)`: Absolute Temperature in Kelvin

By following this structured approach, the project aims to leverage machine learning to predict star temperatures accurately and efficiently.
