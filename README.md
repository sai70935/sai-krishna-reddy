# sai krishna reddy 
MSDS692_S40_Data Science Practicum
# Project Overview
This project was designed to assist workforce boards in determining the best uses of scarce retraining dollars. I reviewed occupational occupations, employees and workforce numbers, potential job growth, and openings to determine occupations to be considered and possibly pursued for training support.
# Research Question
What jobs do workforce boards need to focus on retraining?
# Data
The project merges ONET occupational data with the BLS employment data. ONET is a description of job activities, skills and working conditions. BLS offers employment statistics, wages, projected employment growth, and projected job openings.

This prepared data set includes 819 occupations, one row of data for each 6-digit occupational code. The projection period the employment workbook provides is 2025–2035. Details of its original release are still to be verified independently.

These are average results for the country as a whole. They are not showing individual workers' work experiences, local employers' demands, actual layoffs or if a specific company has embraced automation.
# Methodology
Developed a task-exposure indicator based on 15 occupational characteristics. I then added it with the employment data to come up with a retraining-priority score, with the following weights:
- Task exposure: 40%
- Workforce size: 30%
- Annual openings: 20%
- Projected employment decline: 10%
These weights are a suggested funding policy and are not the best formula. Tested the different weights to determine the effect on the occupation ranks.

I used K-Means to look for clusters of similar jobs, PCA to create a description of the various occupations, then cosine similarity to find career transition possibilities.

As part of this analysis I compared Ridge regression and Random Forest regression to a mean baseline. These models are based on occupational features and use the BLS's projected growth rates of employment in percentage terms. They don't forecast job losses or assess the impact of automation.
# Main Findings
My proposed priority score was first for customer service and second for bookkeeping. Five weighting policies included bookkeeping, which was always among the top three occupations to be considered for further analysis.

The data provided indicates that there are around 1.53 million bookkeeping jobs, 144,100 projected job openings, and a projected loss of 5.6% in employment opportunities over the next 10 years. Estimated openings are based on projected openings in the year, including replacement openings, but do not represent job postings.

The results confirm the idea of training bookkeeping as a training pilot. But this involves further research on local demand and training viability, as well as partners, and is only the right choice for those choosing to select it before customer service.
# Recommendation
Local variation in demand should be considered before embarking on a small bookkeeping retraining pilot with workforce boards. Opportunities for training range from accounting software, automated check-outs, discrepancy investigation and interpretation of financial information.

Before expanding the program, the board should track the outcomes of employment, retention, and wages. Having a comparison group would help to determine if improvements were due to training or to a larger-scale shift in the labor market.

# Running the Analysis
Open a terminal in the main folder of the repository using Python 3.12.

# Install the necessary packages:
To install the required packages, use the following command: python -m pip install -r requirements.txt

# Limitations
A high task-exposure rating does not imply that an occupation will be eliminated. The exposure indicator and priority weights are based on personal judgment of the researchers and can be affected by other assumptions and assumptions can change the rankings.

The regression models are estimates of published projections of employment growth and not actual employment in the future. Permutation importance was computed on training data, so it should be interpreted with caution.

Career transitions suggested are not final and will be subject to additional education/licensing/training requirements as well as local opportunities. No training pilot has taken place, so this analysis is unable to confirm that the proposed training will make a difference to worker outcomes.
# Reproducibility
The packaged analysis includes 73 code cells that ran without any errors in the sample environment with the provided CSV. Not yet independently tested for installation and execution on other computer.

The archive of O*NET data provided to the project was missing some data. You need a complete archive that can be used to regenerate the data from the sources. Hence, executing the analysis with the supplied prepared CSV is not reproduction of the entire preparation.
# LLM Assistance
When developing questions, I used an LLM as a technical assistance tool to code questions, troubleshoot errors, and interpret analytical approaches. I am still in charge of verifying the results, interpreting the code, and ensuring that the conclusions are consistent with the evidence.
