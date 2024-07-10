# Credit-Card-Fraud-Detection
A 'R' script for identifying fraud transactions using IEEE kaggle dataset and Random Forest Algorithm

# Credit Card Fraud Detection Using IEEE's Kaggle Dataset

This project aims to predict the probability that an online transaction is fraudulent using the IEEE-CIS Fraud Detection Dataset from Kaggle.

## Dataset

The dataset used in this analysis comes from the Kaggle competition, IEEE Fraud Detection-CIS. The data on Kaggle is broken into two files: `identity` and `transaction`, which are joined by `TransactionID`.

### Outcome Variable

- `isFraud`: Binary target variable (0: Legitimate, 1: Fraud)

### Categorical Features

- `ProductCD`: Product code, the product for each transaction.
- `card1` - `card6`: Payment card information, such as card type, card category, issue bank, country, etc.
- `addr1`, `addr2`: Address
- `P_emaildomain`: Purchaser email domain
- `R_emaildomain`: Recipient email domain
- `M1` - `M9`: Match, such as names on card and address, etc.
- `DeviceType`
- `DeviceInfo`
- `id_12` - `id_38`: Identity information – network connection information (IP, ISP, Proxy, etc.) and digital signature (UA/browser/os/version, etc.) associated with transactions.

### Numeric Features

- `TransactionDT`: Timedelta from a given reference datetime (not an actual timestamp).
- `TransactionAMT`: Transaction payment amount in USD.
- `dist1`, `dist2`: Distance
- `C1` - `C14`: Counting, such as how many addresses are found to be associated with the payment card, etc. The actual meaning is masked.
- `D1` - `D15`: Timedelta, such as days between previous transactions, etc.
- `Vxxx`: Vesta engineered rich features, including ranking, counting, and other entity relations.
- `id_01` - `id_11`: Identity information

## Goal of the Project

The main goal of this project is binary classification (i.e., two possible classes: 0 or 1). We will focus on metrics commonly used for binary classifiers, such as Accuracy and ROC.

### AUC (Area Under Receiver Operating Characteristic Curve)

One of the most commonly used metrics to visualize the performance of a binary classifier is the Receiver Operating Characteristic Curve (ROC), and the Area Under Curve (AUC) is the best way to summarize its performance in a single number.

## Project Checklist

1. Data Exploration
2. Data Visualization
3. Data Preprocessing
   - Feature Selection
   - Handling Missing Data
   - Encoding the Data
   - Splitting the Data
4. Model Creation
5. Model Evaluation

## Methods and Analysis

### Data Ingestion

In this stage, we download the data and prepare the dataset to be used in the analysis. The dataset is split into two datasets: `df` and `validation` with 90% and 10% of the original dataset respectively. We take the validation set and put it off to the side, pretending that we have never seen it before.

### Data Preprocessing

Data preprocessing involves various tasks including feature selection, handling missing data, encoding categorical features, and splitting the data into training and validation sets.

### Model Creation

We will create and train a binary classifier model using the preprocessed data.

### Model Evaluation

The model will be evaluated using common metrics for binary classifiers, such as Accuracy and AUC-ROC.

## Running the Project

To run this project, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your_username/your_repository.git
    ```
2. Navigate to the project directory:
    ```bash
    cd your_repository
    ```
3. Install the required packages:
    ```bash
    install.packages(c("dplyr", "ggplot2", "randomForest", "caret", "e1071"))
    ```
4. Run the R script:
    ```r
    Rscript fraud_detection.R
    ```

## References

- [IEEE-CIS Fraud Detection Dataset on Kaggle](https://www.kaggle.com/c/ieee-fraud-detection)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
