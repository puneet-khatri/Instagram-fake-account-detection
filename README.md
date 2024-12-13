# Instagram Fake Account Detection

## Project Overview
This project implements a machine learning model to detect fake Instagram accounts using a logistic regression classifier. The model is trained on a dataset with various features that characterize user profiles and outputs whether an account is real or fake.

---

## Dataset Description
The dataset used for this project contains **785 entries** with the following columns:

| Column Name             | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `edge_followed_by`      | Ratio of followers to the total number of users the account follows.       |
| `edge_follow`           | Ratio of accounts followed to the total number of users.                  |
| `username_length`       | Length of the username in characters.                                      |
| `username_has_number`   | Indicates if the username contains numbers (1 = Yes, 0 = No).             |
| `full_name_has_number`  | Indicates if the full name contains numbers (1 = Yes, 0 = No).            |
| `full_name_length`      | Length of the full name in characters.                                     |
| `is_private`            | Indicates if the account is private (1 = Yes, 0 = No).                    |
| `is_joined_recently`    | Indicates if the account was created recently (1 = Yes, 0 = No).          |
| `has_channel`           | Indicates if the account has a channel (1 = Yes, 0 = No).                 |
| `is_business_account`   | Indicates if the account is a business account (1 = Yes, 0 = No).         |
| `has_guides`            | Indicates if the account has published guides (1 = Yes, 0 = No).          |
| `has_external_url`      | Indicates if the account has an external URL in the bio (1 = Yes, 0 = No).|
| `is_fake`               | Target variable indicating if the account is fake (1 = Fake, 0 = Real).   |

All features are preprocessed to ensure compatibility with the machine learning model.

---

## Tools and Libraries
The following Python libraries are used in this project:
- **pandas**: For data manipulation and preprocessing.
- **scikit-learn**: To split the dataset, scale the features, and build the logistic regression model.
- **numpy**: For numerical operations (used implicitly through scikit-learn).
- **StandardScaler**: For feature normalization.
- **LogisticRegression**: The model used for classification.

---

## Workflow
1. **Import Libraries**: Load all necessary Python libraries.
2. **Load Dataset**: Read the dataset from the CSV file (`final-v1.csv`).
3. **Feature and Target Separation**:
   - Features: All columns except `is_fake`.
   - Target: `is_fake` column.
4. **Train-Test Split**: Divide the dataset into training (80%) and testing (20%) sets.
5. **Feature Scaling**: Normalize the data using `StandardScaler` to improve model performance.
6. **Model Training**: Fit a logistic regression model to the training data.
7. **Prediction and Evaluation**:
   - Make predictions on the test set.
   - Evaluate performance using accuracy score.

---

## Results
The model achieved an **accuracy score of 92.99%** on the test set, indicating high reliability in detecting fake accounts.

---

## Usage
1. Clone the repository or download the code files.
2. Install the required libraries:
   ```bash
   pip install pandas scikit-learn
   ```
3. Place the dataset (`final-v1.csv`) in the appropriate directory.
4. Run the script to train the model and evaluate it:
   ```bash
   python instagram_fake_account_detection.py
   ```

---

## Future Enhancements
- Include additional features for better account characterization.
- Experiment with other classification algorithms like Random Forest, SVM, or Gradient Boosting.
- Visualize model performance using confusion matrix and ROC curves.
- Deploy the model in a live application for real-time account validation.

---

## Contributing
Feel free to fork the repository, raise issues, or submit pull requests for any improvements or suggestions.

---

## License
This project is open-source and available under the [MIT License](LICENSE).

---

**Author**: Punit khatri
For questions or feedback, please contact khatripuneet2000@gmail.com.
