Stack Overflow Question Duplicate Detection
This repository contains a project aimed at detecting duplicate questions from a dataset of Stack Overflow questions. The approach leverages text preprocessing, TF-IDF vectorization, and cosine similarity to identify duplicates based on question titles and bodies.

Table of Contents
Features
Requirements   
Usage
Workflow
Results
Contributing
License
Features
Cleans and normalizes text data.
Uses TF-IDF for feature extraction.
Computes cosine similarity to identify duplicates.
Outputs a CSV file containing detected duplicates and their similarity scores.
Requirements
To run this project, you need to have the following Python packages installed:

pandas
numpy
scikit-learn
beautifulsoup4
lxml (for parsing HTML)
You can install the required packages using:

bash
Copy code
pip install pandas numpy scikit-learn beautifulsoup4 lxml
Usage
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/stackoverflow-duplicate-detection.git
cd stackoverflow-duplicate-detection
Place your dataset CSV file in the project directory. Ensure the file structure matches the expected format.

Run the duplicate detection script:

bash
Copy code
python duplicate_detection.py
The detected duplicates will be saved in a file named detected_duplicates.csv.

Workflow
Data Preparation

Load the dataset into a DataFrame.
Inspect for missing values.
Text Preprocessing

Normalize text (lowercasing, removing HTML tags, punctuation).
Clean both the title and body of the questions.
Feature Extraction

Combine cleaned title and body.
Create TF-IDF vectors.
Similarity Calculation

Compute cosine similarity between TF-IDF vectors.
Identifying Duplicates

Set a similarity threshold (e.g., 0.8).
Identify pairs above the threshold.
Reviewing Duplicates

Output a DataFrame containing duplicate IDs and their similarity scores.
Post-processing

Optional: further analyze or visualize duplicates.
Saving Results

Save the results to a CSV file.
Results
After running the script, a CSV file (detected_duplicates.csv) will be generated, containing pairs of duplicate question IDs and their similarity scores.

Contributing
Contributions are welcome! If you have suggestions for improvements or additional features, please create a pull request or open an issue.

License
This project is licensed under the MIT License. See the LICENSE file for details.
