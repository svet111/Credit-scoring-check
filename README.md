### Detailed instructions for installing and configuring the project. 
##### For example:
 ##### Clone the repository: 
###### git clone https://github.com/username/project_name.git 
 ##### Go to the project directory: 
###### cd project_name 
 ##### Install the necessary dependencies: 
###### pip install streamlit
 ##### Run the User Interface: 
###### streamlit run UI.py 
##### Make sure that the current version of sklearn is 1.3.2. Go to the browser and start using it.
### Using
The project can be used to determine creditworthiness.
#### UI.py
Through the streamlit API, the code creates a web page where the user enters data and receives a forecast by clicking on a button, which performs the predict function.
#### input_processing.py
The function in the file preprocesses the data sent by the user before the predict function.
#### one_hot_encoder.joblib
Trained one-hot coding for categorical features.
#### ordinal_encoder.joblib
Ordinal encoding for the Saving accounts.
#### scaler.joblib attribute
Trained standardization of features.
### Solution description
One-hot encoding is applied to categorical features ('Sex', 'Housing', 'Checking account', 'Purpose').
Ordinal encoding has been applied to Saving accounts. When choosing a model, the Random Forest Classifier and the Gradient Boosting Classifier were compared, and hyperparameters were selected for both through GridSearch. The gradient boosting model performed better (roc_auc: 0.764 on the test). Data analysis, training, and model testing are presented in the file Credit_scoring.ipynb.
