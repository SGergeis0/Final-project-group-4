# Project Topic: Identifying Music Genres (classification)

Project Title: Music Genre Prediction Using Machine Learning

Project Files and How to Run Them

1. ETL.ipynb - Extract, Transform, Load (ETL) Process

Purpose: This notebook cleans and prepares the dataset for machine learning.

How to Run:

	•	Open the notebook in Jupyter or any notebook environment.
	•	Run each cell in sequence.

What Each Cell Does:

	•	Cell 1-3: Imports necessary libraries such as pandas for data manipulation.
	•	Cell 4: Loads the spotify_songs_nogenre.csv dataset.
	•	Cells 5-7: Handles missing values and drops unnecessary columns.
	•	Cell 8: Transforms the data by normalizing numerical features (e.g., tempo, energy), ensuring they are ready for machine learning algorithms.
	•	Final Cell: Saves the cleaned and transformed dataset for use in subsequent notebooks.

Outcome: The data is now clean and ready for analysis and modeling in the next steps.

2. PCA_Clustering.ipynb - Principal Component Analysis (PCA) and Clustering

Purpose: This notebook reduces the dataset’s complexity using PCA and clusters similar songs together based on their features.

How to Run:

	•	After running the ETL.ipynb, open this notebook and execute it step-by-step.

What Each Cell Does:

	•	Cell 1-2: Imports required libraries such as scikit-learn for PCA and clustering.
	•	Cell 3: Loads the cleaned dataset from ETL.ipynb.
	•	Cells 4-5: Applies Principal Component Analysis (PCA) to reduce the number of features, making the data easier to visualize and process.
	•	Cell 6: Clusters the songs using KMeans, grouping them based on their similarity.
	•	Cells 7-9: Visualizes the PCA results in a 2D plot and shows the clusters.

Outcome: The dimensionality is reduced, and songs are grouped into clusters for further analysis.

3. Deploying_machine.ipynb - Model Deployment and Evaluation

Purpose: This notebook tests and evaluates different machine learning models to predict music genres.

How to Run:

	•	Make sure the PCA and clustering are completed from the previous notebook.
	•	Open this notebook and execute the cells in sequence.

What Each Cell Does:

	•	Cell 1-2: Imports necessary machine learning libraries like RandomForestClassifier from scikit-learn.
	•	Cell 3: Loads the PCA-processed dataset.
	•	Cells 4-5: Splits the data into training and testing sets.
	•	Cells 6-8: Tests multiple machine learning models such as Random Forest and SVM to determine which model performs best.
	•	Final Cell: Outputs the model accuracy and saves the model for use in predictions.

Outcome: A trained model is saved, ready to predict genres with a high level of accuracy.

4. predict_genre_solution.ipynb - Final Prediction Using Random Forest

Purpose: This notebook provides the final solution, predicting genres using the best-performing model (Random Forest).

How to Run:

	•	This notebook is the last step. Ensure that the Deploying_machine.ipynb is fully run, and the trained model is available.
	•	Open the notebook and run the cells step-by-step.

What Each Cell Does:

	•	Cell 1: Loads the trained Random Forest model saved from Deploying_machine.ipynb.
	•	Cell 2: Loads a new dataset (or the same cleaned data) to make genre predictions.
	•	Cells 3-4: Uses the trained model to predict the genres for the songs in the dataset.
	•	Final Cell: Outputs the predictions, showing which genre each song is classified as.

Outcome: This notebook provides the final genre predictions for a given dataset.

Project Workflow Recap

	1.	Run ETL.ipynb to clean and prepare the dataset.
	2.	Run PCA_Clustering.ipynb to reduce the data’s complexity and group similar songs.
	3.	Run Deploying_machine.ipynb to train different machine learning models and find the best one.
	4.	Run predict_genre_solution.ipynb to use the final model and predict genres for new songs.

By following this workflow, you will be able to replicate the entire process from data cleaning to genre prediction.
