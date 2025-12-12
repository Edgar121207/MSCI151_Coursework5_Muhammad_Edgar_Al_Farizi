# MSCI151_Coursework5_Muhammad_Edgar_Al_Farizi

Barista Staffing Optimization Models
This repository contains a Google Colab notebook demonstrating various optimization models for barista scheduling. The models aim to find optimal staffing schedules based on different objectives and constraints, including cost minimization, fairness in workload distribution, and skill coverage.

Table of Contents
Introduction
Prerequisites
Getting Started
Running in Google Colab
Running Locally
Model Descriptions
Understanding the Output
Customization
Contributing
License
Introduction
This project utilizes Mixed-Integer Linear Programming (MILP) with the PuLP library in Python to optimize barista schedules for a hypothetical coffee shop. It explores five different scenarios:

To run this notebook, you will need:

Python 3.x
pulp library
pandas library
seaborn library
matplotlib library
Getting Started
Running in Google Colab
Open the Notebook: Click on the Colab badge (or navigate directly to the notebook file in Google Colab).
Save a Copy: Go to File > Save a copy in Drive to create an editable version of the notebook.
Install Dependencies: Run the first code cell that contains !pip install pulp (if not already executed).
Run All Cells: Go to Runtime > Run all. The notebook will execute all models, generate visualizations, and print summaries.
Running Locally
Clone the Repository:
git clone <repository-url>
cd <repository-name>
Install Dependencies:
pip install pulp pandas seaborn matplotlib
Open in Jupyter:
jupyter notebook
Then, navigate to and open the .ipynb file.
Run All Cells: Execute all cells sequentially within the Jupyter environment.
Model Descriptions
The notebook is structured with distinct sections for data preparation, model definitions, and individual scenario analyses. Each model has its own build_ and solve_ function:

Data Preparation: Defines baristas, days, blocks, costs, availability, employment types, minimum weekly hours, skill data, etc.
build_staffing_model: Base function for setting up common constraints (coverage, availability, block caps, weekly minimums).
solve_baseline: Solves the primary cost minimization problem.
solve_close_at_19: Solves Scenario A by modifying allow_blocks.
solve_pt_min16: Solves Scenario B by modifying minWeekly requirements.
build_fairness_model & solve_fairness: Implements and solves the fairness objective with a budget cap.
build_skill_model & solve_skill: Implements and solves the skill coverage requirements.
Understanding the Output
After running all cells, the notebook will generate:

Summaries for Each Model: Text outputs detailing solver status, total weekly cost, and weekly hours for each barista.
Detailed Daily Schedules: Tables showing barista assignments per block for each day.
Heatmaps: Visual representations of the schedules, showing assigned baristas per day and block for the baseline, Scenario A, and Fairness/Skill variants.
Quick Cost Summary: A pandas DataFrame summarizing the total weekly costs for all models, followed by a bar chart visualization of these costs.
Comprehensive Recommendation Report: A detailed markdown report summarizing the findings, insights, and actionable recommendations derived from comparing all models.
Customization
Users can modify the initial parameters in the 'Data Preparation' section 

Contributing
Feel free to fork this repository, contribute improvements, or suggest new scenarios for optimization.
