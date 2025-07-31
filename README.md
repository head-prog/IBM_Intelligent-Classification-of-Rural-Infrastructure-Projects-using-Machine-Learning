
# Intelligent Classification of Rural Infrastructure Projects Using Machine Learning

## Project Summary

This project addresses a significant challenge in rural infrastructure planning in India: accurately classifying projects under the correct phase of the **Pradhan Mantri Gram Sadak Yojana (PMGSY)** scheme. These schemes include PMGSY-I, PMGSY-II, PMGSY-III, and RCPLWEA, each with different objectives and requirements.

Manual classification of projects is inefficient, error-prone, and not scalable. To overcome this, a machine learning-based system was developed to automate classification using physical and financial project data. The solution leverages IBM Watson AutoAI and Watson Machine Learning to build, evaluate, and deploy the model in a cloud-based environment.

---

## Problem Statement

The PMGSY program has undergone multiple revisions, and classifying thousands of rural infrastructure projects under the correct version is essential for government bodies, planners, and policy analysts. These classifications impact budgeting, monitoring, and long-term analysis. Manual tagging is not only labor-intensive but also inconsistent.

The goal of this project was to develop a machine learning model that classifies road and bridge projects into the correct PMGSY scheme using structured data inputs.

---

## Objectives

* Automate the classification of infrastructure projects into relevant PMGSY schemes.
* Improve accuracy and consistency of classifications.
* Deploy the model for real-time and batch predictions using cloud services.
* Enable easy integration with future smart governance systems.

---

## Data Collection and Preprocessing

### Data Source

The dataset was obtained from [AI Kosh](https://aikosh.indiaai.gov.in), a government portal that provides open data related to public infrastructure. The data included:

* State and district names
* Sanctioned cost
* Length of sanctioned and completed road works
* Number of sanctioned and completed road works
* Total expenditure

### Preprocessing Steps

* Handled missing values and standardized data entries.
* Encoded categorical columns like state and district names.
* Engineered new features such as:

  * Cost per kilometer
  * Completion ratio

The dataset was balanced to ensure fair representation of all PMGSY schemes.

---

## Machine Learning Approach

### Model Selection

The classification task was handled using **AutoAI** within **IBM Watson Studio**, which automatically evaluated several machine learning models, including:

* Random Forest
* Gradient Boosting
* Logistic Regression

The model with the best performance was selected based on accuracy and F1-score. Random Forest emerged as the most suitable model for this use case.

### Input Features Used for Training

* `STATE_NAME`
* `DISTRICT_NAME`
* `NO_OF_ROAD_WORK_SANCTIONED`
* `LENGTH_OF_ROAD_WORK_SANCTIONED`
* `COST_OF_WORKS_SANCTIONED`
* `EXPENDITURE_OCCURED`
* `NO_OF_ROAD_WORKS_COMPLETED`
* `LENGTH_OF_ROAD_WORK_COMPLETED`

---

## System Development and Deployment

### Tools and Platforms

* IBM Cloud Lite
* IBM Watson Studio
* IBM Watson Machine Learning
* IBM Object Storage

### Development Workflow

1. **Data Upload**: The dataset was uploaded to IBM Cloud Object Storage.
2. **Model Training**: AutoAI handled data cleaning, feature engineering, and model selection.
3. **Evaluation**: Model performance was assessed using metrics like accuracy, precision, recall, and F1-score.
4. **Deployment**: The best-performing model was deployed as a REST API using IBM Watson Machine Learning.
5. **User Interface**: An intuitive front-end was created using IBM watsonx.ai Studio, allowing users to input new data and receive predictions in both JSON and table formats.

---

## Results and Performance

The final model demonstrated strong classification capability, with the following metrics:

* **Overall Accuracy**: 90.3%
* **Precision (macro average)**: 89.7%
* **Recall (macro average)**: 90.1%
* **F1-score (macro average)**: 89.9%

These results indicate that the system can reliably replace manual classification for a majority of cases.

---

## Key Achievements

* Successfully automated the classification process for rural infrastructure projects.
* Achieved over 90 percent accuracy in categorizing projects into correct PMGSY schemes.
* Reduced the potential for human error and inconsistencies.
* Enabled real-time and batch predictions through a deployed REST API.
* Supported transparent, data-driven decision-making in rural infrastructure planning.

---

## Future Enhancements

The current system can be further improved and expanded in the following ways:

### Model Improvements

* Include additional features like project duration, terrain type, or contractor information.
* Incorporate geographic data to support location-aware predictions.
* Enable active learning for continuous model retraining as new project data becomes available.

### System Integration

* Integrate the API with government dashboards or public portals.
* Allow bulk upload of project records for institutional users.
* Generate custom reports for auditors and planners.

### Scalability

* Extend the classification model to other government schemes (e.g., AMRUT, NRLM).
* Support multilingual interfaces to cater to local authorities across regions.

---

## References

* AI Kosh PMGSY Dataset: [https://aikosh.indiaai.gov.in](https://aikosh.indiaai.gov.in)
* IBM Watson Studio: [https://www.ibm.com/cloud/watson-studio](https://www.ibm.com/cloud/watson-studio)
* Scikit-learn Documentation: [https://scikit-learn.org](https://scikit-learn.org)

---

## Author

**Vraj Sondagar**
B.Tech in Computer Science Engineering
ITM SLS Baroda University


