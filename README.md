# Cuisine Prediction API (V4) DOC

## Info
A Cuisine Prediction API (V4) based on Flask/React-Python/SKLearn

## Setup
0. Environment Setup: run `python3 -m venv venv`
1. Activate Venv: run `source venv/bin/activate`
2. Install Dependencies: run `pip install -r requirements.txt`
3. Update Dependencies: run `pip freeze > requirements.txt`
4. VScode Config: Open the launch_info.json and append the content into ./.vscode/launch.json if it is necessary.

## Start
0. Choose the production or developing mode in config.py
1. Run `flask run`
2. Access the progress via Terminal
3. Open Browser with `127.0.0.1:5000/index` URL to see the website homepage
4. Go to `127.0.0.1:5000/predict` URL or click on the Prediction Link to the predict page
5. Type ingredients into the form or choose the random-chose ingredient below the form and click Predict button to see the prediction result.

## Runtime
0. Developing Mode runtime:
- With dataset_developing.csv: ~ 5 mins
- Withpout dataset_developing.csv: ~ 15mins
1. Production Mode runtime:
- With dataset_production.csv: ~ 10 mins
- Without dataset_production.csv: ~ 30 mins

## Dataset
1. Production Dataset:
   - Processing: ~ 39967 Lines
   - Ingredient Menu: 6714 ingredients
   - CSV Size: 1.07GB (Too large, need to be removed before push to GitHub)
2. Developing Dataset:
   - Processing: 400 Lines
   - Ingredient Menu: 1160 ingredients
   - CSV Size: ~ 100MB (If over 100MB, need to be removed before push to GitHub)

## [Future](./DESIGN.md)
0. Integrated with React for better frontend look
1. Explore with more models and tune each model in depth for a better prediction accuracy.
2. Develop more related features with base templates and Deploy it to AWS or GCP to make this ingredients-cuisine service real for public use.

## Thanks
0. Many thanks to Yummly for Original JSON Dataset.
1. CSV Production dataset is oversized for GitHub, so please remove it before push commit.


# DOC Previous to V3
## Start
1. Open 2 Separate Terminal to simulate API and Client and Open the Browser at 127.0.0.1:5000 homepage.
2. Run python yummly_api.py in terminal to establish the web service and Refresh the browser after excutation to see valid ingredients input.
3. Run python client_request.py in ANOTHER terminal to simulate client request and Refresh the browsewr after exutation to see cuisine prediction.
4. Change the ingredients in client_request.py, run python client_request.py and Refresh the browser to view new cuisine prediction.

## Modes
0. Two Modes are available for Machine Learning Pipeline: Align Model parameters with valid dataset V.S. Predict Cuisine on final dataset.
1. Two Modes are available for dataset scale: Smaller size for faster api development V.S. Whole dataset for machine learning tuning/prediction.

## Runtime
0. The program with print request in terminal and terminate itself if Source JSON Data is NOT in the folder, CSV dataset is oversized for GitHub.
1. Program will start to transfer JSON data to CSV data first if it has not been done, which will take about 10 mins with progress info in terminal.
2. More results can refer to terminal and the whole demo results from both terminal and browser as document and photo format are in RESULTS folder.
