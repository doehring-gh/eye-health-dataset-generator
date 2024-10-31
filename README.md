Eye Health Population Dataset Generator

Overview
The Eye Health Population Dataset Generator is a Python-based tool designed to simulate a comprehensive dataset related to eye health examinations for a population of 1,000 individuals. This synthetic dataset can be used for educational purposes, testing data analysis pipelines, or as a placeholder in projects where real-world data is unavailable.

Features
* Synthetic Data Generation: Creates realistic eye health data including demographics and clinical measurements.
* Customisable Parameters: Easily adjust the dataset size or the distribution of specific fields.
* Subset Generation: Automatically generates subsets of the main dataset based on criteria like eye side (OD/OS) and age groups.
* Reproducibility: Utilizes a fixed random seed to ensure consistent results across runs.

Dataset Description
The generated dataset simulates eye health examination records with the following attributes:
* Patient_ID: Unique identifier for each patient.
* Age: Patient's age in years (floating-point for precision).
* Gender: Male or Female.
* Eye: Indicates the examined eye — OD (Right Eye) or OS (Left Eye).
* Refractive_Error: Measured in diopters, simulated based on age-related regression models.
* Intraocular_Pressure: Measured in mmHg, influenced by age.
* Central_Corneal_Thickness: Measured in micrometers (µm), varies with age.
* Pupil_Diameter: Measured in millimeters (mm), affected by age.
* Visual_Acuity_logMAR: Logarithm of the minimum angle of resolution, a measure of visual acuity.
* Astigmatism: Indicates presence (Yes) or absence (No) of astigmatism.
* Exam_Date: Date of the eye examination within the past two years.
* Age_Group: Categorized age groups ranging from Infant to Senior.

Installation
Prerequisites
* Python 3.7 or higher
* pip (Python package installer)
Required Python Libraries
The script relies on the following Python libraries:
* numpy
* pandas

You can install the required libraries using pip:
pip install numpy pandas


Usage

1. Clone the Repository

git clone https://github.com/doehring-gh/eye-health-dataset-generator
cd eye-health-dataset-generator

2. Run the Script
Ensure that you have Python installed and the required libraries are set up. Execute the script using:

python generate_eye_health_dataset.py

This will generate the main dataset and various subsets, saving them as CSV files in the current directory.

3. Output
After running the script, you will find multiple CSV files in your directory, including the main dataset and its subsets.

Output Files
The script generates the following CSV files:
1. Main Dataset
o eye_health_population_dataset.csv: Contains all 1,000 records with comprehensive eye health data.
2. Subsets by Eye Side
o eye_health_population_dataset_OD.csv: Records for the Right Eye (OD).
o eye_health_population_dataset_OS.csv: Records for the Left Eye (OS).
3. Subsets by Age Group
o eye_health_population_dataset_Infant.csv
o eye_health_population_dataset_Child.csv
o eye_health_population_dataset_Teen.csv
o eye_health_population_dataset_Young_Adult.csv
o eye_health_population_dataset_Middle-Aged_Adult.csv
o eye_health_population_dataset_Senior.csv

Each subset contains records filtered based on the specified criterion (Eye side or Age Group).

Data Fields
1. Patient_ID
* Type: Integer
* Description: Unique identifier for each patient (1 to 1000).
2. Age
* Type: Float
* Description: Patient's age in years, ranging from 0 to 80, generated using a continuous uniform distribution.
3. Gender
* Type: Categorical
* Categories: Male, Female
* Description: Patient's gender with an approximate distribution of 48% Male and 52% Female.
4. Eye
* Type: Categorical
* Categories: OD (Right Eye), OS (Left Eye)
* Description: Indicates which eye was examined.
5. Refractive_Error
* Type: Float
* Unit: Diopters (D)
* Description: Simulated refractive error based on age, following a regression model with normal distribution residuals.
6. Intraocular_Pressure
* Type: Float
* Unit: mmHg
* Description: Simulated intraocular pressure based on age, following the equation IOP = 16 + 0.01 * Age with normal residuals (SD=3 mmHg).
7. Central_Corneal_Thickness
* Type: Float
* Unit: Micrometers (µm)
* Description: Simulated central corneal thickness based on age, following the equation CCT = 550 - 0.1 * Age with normal residuals (SD=20 µm).
8. Pupil_Diameter
* Type: Float
* Unit: Millimeters (mm)
* Description: Simulated pupil diameter based on age, following the equation Pupil Diameter = 6 - 0.05 * Age with normal residuals (SD=1 mm), clipped between 1.0 and 8.0 mm.
9. Visual_Acuity_logMAR
* Type: Float
* Unit: logMAR
* Description: Simulated visual acuity based on age, following the equation Visual Acuity = 0.005 * Age with normal residuals (SD=0.1 logMAR), clipped between -0.3 and 0.5 logMAR.
10. Astigmatism
* Type: Categorical
* Categories: Yes, No
* Description: Indicates the presence of astigmatism, with approximately 30% of records marked as "Yes".
11. Exam_Date
* Type: Date
* Description: Randomly generated date of the eye examination within the past two years from the current date.
12. Age_Group
* Type: Categorical (Ordered)
* Categories: Infant, Child, Teen, Young Adult, Middle-Aged Adult, Senior
* Description: Categorized age groups based on the patient's age.

License
This project is licensed under the MIT License.

Contact
For any questions or feedback, please contact:
* Name: Daniela Oehring
* Email: daniela.oehring@plymouth.ac.uk
* GitHub: doehring-gh

Disclaimer: This dataset is synthetically generated for illustrative and educational purposes. It does not represent real patient data.
