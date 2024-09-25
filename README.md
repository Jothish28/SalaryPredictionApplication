# Salary Prediction Application using Machine Learning and Streamlit

## Project Description
This project aims to predict the salaries of employees based on various factors like country, years of education, and education level. The model is trained using data from the Stack Overflow Developer Survey, which provides a comprehensive dataset of global developer salaries and related information. The application has been developed using Streamlit for an intuitive user interface that allows users to input relevant details and receive real-time salary predictions.

## Key Features
- Predict salaries using machine learning algorithms.
- User-friendly interface built with Streamlit.
- Visualizations to understand data distributions.
- Real-time salary prediction based on user inputs.

## Project Workflow and Key Steps
1. **Data Preprocessing**
   - The raw dataset from the Stack Overflow Developer Survey was preprocessed to ensure consistency and usability.
   - Handled missing values by removing rows where crucial data was absent and performed necessary transformations to prepare the dataset for model training.

2. **Data Cleaning**
   - Cleaned the dataset by removing irrelevant columns that do not contribute to salary prediction (e.g., redundant or unrelated survey fields).
   - Standardized and formatted the data to maintain uniformity across all records, ensuring accurate model training.

3. **Outlier Identification and Removal**
   - Implemented boxplots to visually detect outliers in the salary data. Instead of replacing these outliers with average or mean values, they were entirely removed to avoid skewing the model’s predictions, resulting in more reliable outputs.

4. **Label Encoding**
   - As the dataset contains categorical variables (such as country and education level), label encoding was applied to convert these categorical values into numerical ones, making the data compatible with machine learning algorithms.

5. **Model Training**
   - Multiple regression models were trained, including:
     - Linear Regression
     - Decision Tree Regressor
     - Random Forest Regressor
   - A Grid Search (GV Search) was employed to fine-tune the hyperparameters of these models to maximize their performance.

6. **Model Evaluation**
   - Each model's performance was evaluated using:
     - **Mean Squared Error (MSE)**: This metric quantifies the average squared difference between the predicted and actual salaries, with a lower value indicating a better-performing model.
     - **Mean Absolute Error (MAE)**: This metric measures the average magnitude of errors in the predictions without considering their direction.
   - After evaluation, the best-performing model was selected based on the lowest MSE.

7. **Data Visualization**
   - Integrated various visualizations in the Streamlit application to enhance user understanding of the dataset:
     - **Pie Chart**: Displays the number of data entries from different countries, giving insights into the distribution of responses.
     - **Bar Chart**: Shows the mean salary based on country, allowing users to compare salary averages across different nations.
     - **Line Chart**: Illustrates the mean salary based on experience, providing a visual representation of how salary tends to increase with more experience.

8. **Implementation in Streamlit**
   - The final machine learning model was integrated into a Streamlit web application, allowing users to input features such as country, education level, and years of education.
   - The application then predicts the user's expected salary in real-time, providing a user-friendly interface for easy interaction.

## Installation Instructions
To set up the project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/SalaryPredictionApplication.git
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd SalaryPredictionApplication
   ```

3. **Install Required Packages**:
   Make sure you have Python installed, then create a virtual environment and install the required packages:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

4. **Run the Streamlit Application**:
   Start the Streamlit server to launch the application:
   ```bash
   streamlit run app.py
   ```
   This will open a new tab in your web browser displaying the Salary Prediction Application.

5. **Input Features**:
   Enter the required features such as country, years of education, and education level in the application to get salary predictions.

## **Contributing**
If you would like to contribute to this project, please fork the repository and submit a pull request with your changes.
