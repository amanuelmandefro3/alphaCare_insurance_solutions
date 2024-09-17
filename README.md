# AlphaCare Insurance Solutions - 10 Academy - Week 3

### Author: Amanuel Mandefrow 

## Task 1:
### Git and GitHub

- **Tasks:** 
  - Create a git repository for the week with a good Readme.
  - Git version control.
  - CI/CD with Github Actions.

- **Key Performance Indicators (KPIs):**
  - Dev Environment Setup.
  - Relevant skill in the area demonstrated.

### Project Planning - EDA & Stats

- **Tasks:**
  - Data Understanding.
  - Exploratory Data Analysis (EDA).
  - Statistical thinking.

- **KPIs:**
  - Proactivity to self-learn - sharing references.
  - EDA techniques to understand data and discover insights.
  - Demonstrating Stats understanding by using suitable statistical distributions and plots to provide evidence for actionable insights gained from EDA.

## Task 2:
### Data Version Control (DVC)

- **Tasks:**
  - Install DVC: 
    ```bash
    pip install dvc
    ```
  - Initialize DVC: In your project directory, initialize DVC
    ```bash
    dvc init
    ```
  - Set Up Local Remote Storage:
    - Create a Storage Directory:
      ```bash
      mkdir /path/to/your/local/storage
      ```
    - Add the Storage as a DVC Remote:
      ```bash
      dvc remote add -d localstorage /path/to/your/local/storage
      ```
  - Add Your Data: 
    - Place your datasets into your project directory and use DVC to track them:
      ```bash
      dvc add <data.csv>
      ```
  - Commit Changes to Version Control:
    - Create different versions of the data.
    - Commit the `.dvc` files (which include information about your data files and their versions) to your Git repository:
      ```bash
      git add <data.csv>.dvc
      git commit -m "Track dataset version with DVC"
      ```
  - Push Data to Local Remote:
    ```bash
    dvc push
    ```

## Task 3:
### A/B Hypothesis Testing

- **Hypotheses:**
  - There are no risk differences across provinces.
  - There are no risk differences between zip codes.
  - There are no significant margin (profit) differences between zip codes.
  - There are no significant risk differences between Women and Men.

- **Tasks:**
  1. **Select Metrics:** Choose the key performance indicator (KPI) that will measure the impact of the features being tested.
  2. **Data Segmentation:**
     - Group A (Control Group): Plans without the feature.
     - Group B (Test Group): Plans with the feature.
     - For features with more than two classes, ensure that the two groups selected do not have significant statistical differences on anything other than the feature being tested (client attributes, auto property, and insurance plan type must be statistically equivalent).
  3. **Statistical Testing:**
     - Conduct appropriate tests (e.g., chi-squared for categorical data, t-tests or z-tests for numerical data).
     - Analyze the p-value from the statistical test:
       - If `p_value < 0.05`, reject the null hypothesis, indicating a statistically significant effect.
       - If `p_value >= 0.05`, fail to reject the null hypothesis, indicating no significant impact.
  4. **Analyze and Report:**
     - Document findings and interpret the results within the context of their impact on business strategy and customer experience.

