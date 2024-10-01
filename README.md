# Predict-Football-Match

This project aims to predict English Premier League (EPL) match outcomes (Win, Loss, Draw) using match data scraped from the fbref. The project is divided into two main components: data scraping and model building.

![ml-epl](epl.jpeg)


## Project Structure
The project consists of the following files:

* **scraping.ipynb:** This Jupyter notebook contains the web scraping code to collect match data, including team statistics and match outcomes.
* **prediction.ipynb:** This Jupyter notebook contains the model-building process where we use machine learning algorithms (like XGBoost) to predict match outcomes based on the scraped data

## Dataset

Open the scraping.ipynb file in JupyterLab or Jupyter Notebook to scrape match data. The data scrapped from [fbref](https://fbref.com/en/). Including match statistics, including team names, goals scored, xG (expected goals), shots, and other relevant match details. Uses libraries like BeautifulSoup and requests.

## Model

- After scraping, the data is cleaned and preprocessed, including converting text into numerical categories and handling missing values.
- Rolling averages applied for key features over a fixed window (3 matches) and create additional features such as venue, day of the week, and referee information.
- Train a classification models and hyperparameter tuning through RandomizedSearchCV and GridSearch.
- Evaluate the model's performance using precision and other metrics to predict whether a team will win, lose, or draw.

## Potential Improvements

* **Data:** Adding more features such as player injuries, team form, head-to-head history, and advanced statistics.
* **Algorithms:** Trying different models (Gradient Boosting, Neural Networks) to see if they improve predictive performance.
* **Tuning:** Further hyperparameter tuning with more advanced techniques like Bayesian Optimization (Optuna).


### Environment

```BASH
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
```
