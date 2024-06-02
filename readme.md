<div align="center">

# [Building Robust AML Models: Advanced Techniques for Effective Transaction Monitoring](https://github.com/ds-souvik/Threshold-Tuning-for-Anti-Money-Laundering-AML-Scenario/blob/main/Building%20Robust%20AML%20Models%20Advanced%20Techniques%20for%20Effective%20Transaction%20Monitoring.pptx)

</div>

Welcome to the **Building Robust AML Models** repository! This project showcases a comprehensive approach to optimizing Anti-Money Laundering (AML) transaction monitoring for the scenario: **Large Value Deposits.** The project describes the market standard tuning methodologies, explains the inefficiencies of these methodologies to tackle the generation of False Negatives (Not detecting all Suspicious alerts) and how the scenarios and tuning methodologies should be optimized for developing robust AML Compliance Models. The repository is structured to provide valuable insights for technical recruiters, interviewers, and anyone interested in data science, finance, and AML compliance.

## Explore the Project
You can explore the project and its components in the following ways:
1. [**Project Presentation**](https://github.com/ds-souvik/Threshold-Tuning-for-Anti-Money-Laundering-AML-Scenario/raw/main/Building%20Robust%20AML%20Models%20Advanced%20Techniques%20for%20Effective%20Transaction%20Monitoring.pptx): A comprehensive presentation that covers the problem statement, methodology, results, key insights, and action items from the analysis. This presentation is ideal for understanding the project's scope and impact.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Key Steps and Methodology](#key-steps-and-methodology)
- [Key Findings](#key-findings)
- [Conclusion](#conclusion)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Skills and Expertise](#skills-and-expertise)
- [Contact](#contact)

## Overview
In this project, I have applied advanced statistical techniques to optimize AML transaction monitoring for large value deposits. The objective was to develop a market-standard solution for the scenario: Large Value Deposits that enhances the detection of suspicious activities while minimizing false positives, reflecting the stringent compliance requirements of financial institutions.

### Purpose
The primary goal of this project is to demonstrate my ability to interpret and analyze data to make informed financial crimes decisions. By tuning the monitoring thresholds effectively, I aim to maximize the detection of true suspicious activities, reduce generation of False Negatives and reduce operational costs associated with false positives.

### Relevance
This project showcases a methodology that is widely used in the banking sector. But this method is inefficient due to large number of False Positives, and presence of False Negatives. I’ve learnt from my experiences how to develop efficient AML models - Rule-based and ML-based (Segment the customers, products etc.) models. I play an instrumental role in bridging the gap between the inefficient market standard and building a state-of-the-art in-house AML models. This presentation underscores my readiness to contribute to Morgan Stanley’s Global Financial Crimes team by leveraging my skills in data analysis and AML transaction monitoring.

## Project Structure
1. **Data:**
   - `accounts.csv`: Contains account-level information, including the target variable `IS_FRAUD`.
   - `transactions.csv`: Contains transaction-level details such as sender and receiver account IDs, transaction amount (`TX_AMOUNT`), and timestamps.

2. **Output Files:**
   - `DQ_report_account_data.xls`: Data Quality Report for the account data.
   - `DQ_report_transactions_data.xls`: Data Quality Report for the transaction data.
   - `threshold_summary_file.xls`: Summary file containing threshold values and corresponding evaluation metrics for each percentile.

3. **Scripts and Notebooks:**
   - `AML_Tuning.ipynb`: Jupyter Notebook containing the detailed scripts for data processing, parameter tuning, and evaluation.
   - `dq_report.py`: Python script used to generate the Data Quality Report.

4. **Presentation:**
   - `Building Robust AML Models Advanced Techniques for Effective Transaction Monitoring.pptx`: PowerPoint presentation summarizing the project, findings, and recommendations.

## Key Steps and Methodology
### 1. Data Quality Report (DQ Report)
- Generated a comprehensive Data Quality Report for both the account and transaction datasets.
- Analyzed missing values, unique values, data types, and distribution of numerical variables to identify outliers and skewness.

### 2. Parameter Tuning
- Focused on the `DEPOSIT_AMT` parameter due to its critical role in identifying large value transactions.
- Generated a threshold summary file encompassing percentile distributions from 1 to 99, with calculated thresholds and corresponding evaluation metrics for each percentile.

### 3. Threshold Evaluation Metrics
- Evaluated multiple metrics to determine the optimal threshold for `DEPOSIT_AMT`:
  - **True Positive Rate (Recall)**
  - **False Positive Rate**
  - **Precision**
  - **F1 Score**
  - **Youden’s J Statistics**

### 4. Optimum Threshold Selection
- Determined the best threshold using Youden's J Statistic and F1 Score.
- Visualized confusion matrices to compare the effectiveness of each threshold on both training and test datasets.
- Identified that using recall as the evaluation metric minimizes false negatives, a crucial factor in AML monitoring.

### 5. Methodology Optimization
- Optimized the tuning methodology using recall to ensure maximum detection of suspicious activities.
- Applied the identified thresholds to both training and test datasets to validate their effectiveness.

## Key Findings
- **J Statistics**: Balances sensitivity and specificity but may not always prioritize the highest recall.
- **F1 Score**: Balances precision and recall, providing a comprehensive view of performance.
- **Recall**: Maximizes detection of suspicious activities but may lead to a higher number of false positives.

## Conclusion
This project demonstrates my expertise in developing and tuning AML models, both rule-based and machine learning-based. By leveraging advanced data analysis techniques, I have optimized transaction monitoring for large value deposits, ensuring high detection efficiency while minimizing operational costs. Different scenario designs, tuning methodologies, and metrics must be used and should be tailor-made according to each use case, bank product, etc. Additionally, building a good post-detection solution is crucial to further reduce false positives. I have the skillsets to achieve all this.

## How to Use

1. **Clone the repository**:
    ```sh
    git clone https://github.com/ds-souvik/Threshold-Tuning-for-Anti-Money-Laundering-AML-Scenario.git
    cd Threshold-Tuning-for-Anti-Money-Laundering-AML-Scenario
    ```

2. **Set up the environment**:
    - Ensure you have Python and Jupyter Notebook installed. You can use the following commands to set up a virtual environment:
    ```sh
    python -m venv aml_env
    source aml_env/bin/activate  # On Windows use `aml_env\Scripts\activate`
    pip install -r requirements.txt
    ```

3. **Run the Jupyter Notebook**:
    ```sh
    jupyter notebook AML_Tuning.ipynb
    ```

4. **Generate Data Quality Reports**:
    - Execute the `dq_report.py` script to generate data quality reports for the account and transaction datasets:
    ```sh
    python dq_report.py
    ```

5. **Explore the Output Files**:
    - Review the generated data quality reports and threshold summary file in the `Output_files` directory.

6. **Analyze and Visualize Results**:
    - Follow the steps in the Jupyter Notebook to analyze and visualize the results of the parameter tuning and threshold evaluation metrics.

7. **Review the Presentation**:
    - Open `Building Robust AML Models Advanced Techniques for Effective Transaction Monitoring.pptx` to understand the project summary, methodology, and findings.

8. **Customize and Extend**:
    - Modify the scripts and notebook as needed to adapt the methodology to different AML scenarios or datasets.