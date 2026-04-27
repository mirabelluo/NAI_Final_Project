# AI Humor in Jokes - Data Analysis Notebook

## Overview
This Jupyter Notebook processes and analyzes survey data to compare how humans and Large Language Models (LLMs) perceive and identify humor. It automates the collection of AI responses, compares them to human baselines, and generates visualizations.

The code performs:
* Environment Setup: Initializes connections to OpenAI, Anthropic, and Google Gemini APIs.
* Data Collection: Prompts each model with the questions in a JSON file 30 times. 
* Data Processing: Parses API responses, cleans data, and merges data.
* Statistical Analysis: Calculates evaluation metrics to be used for visualization.
* Visualization: Generates various plots to answer our research question.

## Dependencies
To run this notebook, you will need to install Python and the following libraries:

Standard Library Modules:
* os
* json
* re
* time

Third-Party Packages:
* numpy
* pandas
* scipy
* scikit-learn
* matplotlib
* seaborn
* python-dotenv
* openai
* anthropic
* google-genai

## Configuration and External Files
To successfully execute the data collection and analysis steps, the working directory must contain:

1. Environment Variables: A `.env` file containing your active API keys:
   - OPENAI_API_KEY
   - ANTHROPIC_API_KEY
   - GEMINI_API_KEY

2. Input Data:
   - stimuli.json: Contains the 24 text items (jokes) and their ground truth sources.
   - NIAI_Responses - Form Responses 1.csv: Contains the raw human baseline survey data.
