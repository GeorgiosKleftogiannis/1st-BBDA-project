📥 1. Extract – Retrieving the Raw Data

The first step of our ETL pipeline focuses on extracting the raw dataset from its source.
For this project, our team selected a publicly available dataset from Kaggle, which we downloaded locally and loaded into our Python environment for further processing. This dataset was used to train a deep learning model designed to predict car prices based on various vehicle characteristics.

**Data Source**
* Platform: Kaggle
* Dataset Type: CSV file
* Dataset's Name: train_data
* Description: The dataset contains raw information about cars, including model specifications, prices, and additional attributes.
* Purpose: Serve as the input data for our ETL practice pipeline.

**Extraction Process**
1. The dataset was manually downloaded from Kaggle.
2. Using pandas, we loaded the CSV file into a DataFrame inside a Jupyter Notebook.
3. We performed an initial inspection to verify the structure and contents of the dataset.

**Outcome**
* The raw dataset was successfully imported into a DataFrame.
* The team confirmed column names, data types, and initial quality issues.
* This DataFrame served as the starting point for the Transform step of the ETL pipeline.