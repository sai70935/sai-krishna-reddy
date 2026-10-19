# sai krishna reddy 
MSDS692_S40_Data Science Practicum
Workforce Retraining for Occupations Exposed to Automation is a priority.
Project Overview
This project came about because I wanted to assist workforce boards in determining where to invest precious retraining dollars. I examined occupational characteristics, employment in each occupation, projected changes in employment, and projected annual job openings. My interest was to pinpoint occupations for greater scrutiny and potential for a small training pilot.
Research Question
Based on exposure to the tasks, number of workforce, job prospects, and number of openings per year, what occupations should workforce boards prioritize for retraining?
Data
The ONET occupational data was matched with BLS employment information. ONET is a description of job activities, skills, and working conditions. BLS offers employment figures, wages, growth projections and job openings.

The dataset contains 819 occupation rows, representing one row of data per 6 digit code. The employment workbook that is supplied contains projection columns for 2025-2035.

Data limitation: These are national occupational averages. They don't reveal layoffs, demand of local employers, or if a specific company has adopted automation. The details of the original release of the employment workbook require independent verification.
Methodology
The first step in creating an exposure indicator was to develop a list of 15 occupational characteristics. I then merged exposure data with job information and I computed a retraining-priority score:
- Task exposure: 40%
- Workforce size: 30%
- Annual openings: 20%
- Projected decline: 10%
The following weights are suggested policy options. To determine if the rankings changed, I tried out various weights.

I also looked into occupational patterns using K-Means as well as cosine similarity for determining possible career transition options using PCA. In a separate analysis, I compared the results of Ridge and Random Forest regression to a mean baseline to estimate BLS projected employment growth.
Main Findings
Bookkeeping was the second most important according to my proposed priority score and remained in the top three of the five weighting policies. Based on the provided information, the number of bookkeeping job postings is around 1.44 lakh annually, with a projected job loss of 5.6%, and 1.53 lakh workers are engaged in bookkeeping activities.

The proposed formula ranked customer service representatives No. 1. Bookkeeping is, therefore not just a career to pursue, but one strong alternative to the pilot career.
Recommendation
It is a good idea to see what the needs are in your area and possibly a small trial of a bookkeeping training program. Training may be on digital accounting software, checking automated working out, investigating workings and interpreting financial information.

Before expanding the program, the board should assess the impacts of employment, retention, and wage outcomes.
Repository Files
- analysis.ipynb — the final analysis notebook.
The prepared data is stored in the following file: data/eda_merged_occupations.csv
- The supplied employment workbook data/raw/occupation.xlsx.
data/README.md — information about the data and preparation steps.
- scripts/prepare_data.py — script for preparing the data.
- scripts/run_notebook.py — script for running the notebooks.
- requirements.txt — Python packages that are required.
Running the Analysis
Open a terminal window in the main folder of the repository, using Python 3.12.

Install necessary packages:
Python -m pip install -r requirements.txt

Run the notebook:
python scripts/run_notebook.py

It can be opened in JupyterLab too:
jupyter lab

Open analysis.ipynb, click on the right python kernel and run the cells sequentially from top to bottom.
Limitations
Don't assume that a high exposure score will mean a job will be lost. Scoring is a judgement process and can vary from one country to another.

The regression models provide an estimate of future employment as projected by the BLS. The feature importance was computed from the training data so is to be interpreted with caution. Further checks are also needed for possible career transitions, including education and licensing requirements, and opportunities within the locality.

This project does not have a training pilot in place to determine if the proposed training will lead to workers' better outcomes.
Reproducibility
A set of 73 code cells was included in the packaged analysis and none of them were encountered errors during the execution using the provided pre-packaged CSV in the provided environment. It has not yet been verified to be a clean installation on another computer.

The original archive is incomplete and a complete archive is needed to rebuild the data set. The repository describes this and details the difference from running the prepared-data analysis versus reconstructing the entire pipeline.
LLM Assistance
I relied on an LLM to assist with coding, problem-solving and the comprehension of technical topics. I am still in charge of verifying the results, describing the procedures, and communicating the nature of what the analysis can and cannot tell.
