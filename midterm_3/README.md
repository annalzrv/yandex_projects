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

## Entity-Relationship (ER) Description

The database consists of four main tables: **case_ids**, **vehicles**, **collisions**, and **parties**. Below is the ER diagram and a detailed description of each table and their relationships:

![ER Diagram](https://pictures.s3.yandex.net/resources/1.7_2880border_1_1654004672.png)

### Tables

- **case_ids**
    - `case_id` (text): Unique identifier for each case.
    - `Case_id` (text): Alternative identifier for the case.

- **vehicles**
    - `id` (integer): Unique identifier for each vehicle entry.
    - `case_id` (text): Foreign key referencing the `case_id` in the **case_ids** table.
    - `party_number` (integer): Identifier for the party involved in the accident.
    - `vehicle_type` (text): Type of vehicle.
    - `vehicle_transmission` (text): Transmission type of the vehicle.
    - `vehicle_age` (integer): Age of the vehicle.

- **collisions**
    - `case_id` (text): Unique identifier for each collision, linked to **case_ids**.
    - `county_city_location` (text): Location of the collision.
    - `county_location` (text): Detailed location within the county.
    - `distance` (real): Distance covered.
    - `direction` (text): Direction of travel.
    - `intersection` (integer): Indicates if the collision occurred at an intersection.
    - `weather_1` (text): Weather conditions at the time of the collision.
    - `location_type` (text): Type of location (urban, rural, etc.).
    - `collision_damage` (text): Extent of the damage.
    - `party_count` (integer): Number of parties involved.
    - `primary_collision_factor` (text): Main factor contributing to the collision.
    - `pcf_violation_category` (text): Violation category.
    - `type_of_collision` (text): Type of collision (rear-end, side-impact, etc.).
    - `motor_vehicle_involved_with` (text): Other vehicles involved.
    - `road_surface` (text): Condition of the road surface.
    - `road_condition_1` (text): Additional road condition details.
    - `lighting` (text): Lighting conditions at the time of the collision.
    - `control_device` (text): Traffic control devices in use.
    - `collision_date` (date): Date of the collision.
    - `collision_time` (time): Time of the collision.

- **parties**
    - `id` (integer): Unique identifier for each party entry.
    - `case_id` (text): Foreign key referencing the `case_id` in the **collisions** table.
    - `party_number` (integer): Identifier for the party involved in the accident.
    - `party_type` (text): Type of party (driver, pedestrian, etc.).
    - `at_fault` (integer): Indicates if the party was at fault.
    - `insurance_premium` (integer): Insurance premium amount.
    - `party_sobriety` (text): Sobriety level of the party.
    - `party_drug_physical` (text): Drug or physical condition of the party.
    - `cellphone_in_use` (integer): Indicates if a cellphone was in use during the collision.

### Relationships

- **case_ids** to **vehicles**: One-to-many relationship through `case_id`.
- **case_ids** to **collisions**: One-to-one relationship through `case_id`.
- **collisions** to **parties**: One-to-many relationship through `case_id`.
