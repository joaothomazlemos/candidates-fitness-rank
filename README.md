
## Project description

Background:


As a talent-sourcing company for tech roles, our challenge is pinpointing top candidates. We seek to automate and optimize our manual processes by developing a machine learning-powered pipeline. Our approach involves keyword-driven searches, like "full-stack software engineer," and manual reviews, where starring a candidate signifies their ideal fit for a role. Based on this feedback, we aim to dynamically re-rank candidates, ensuring the best matches rise to the top. This innovative strategy streamlines our operations, saving time and enhancing our ability to identify and place exceptional candidates in technology companies.

## Data Description:

The data comes from our sourcing efforts. We removed any field that could reveal personal details and gave a unique identifier for each candidate.

Attributes:
id : unique identifier for candidate (numeric)

job_title : job title for candidate (text)

location : geographical location for candidate (text)

connections: number of connections candidate has, 500+ means over 500 (text)

Output (desired target):
fit - how fit the candidate is for the role? (numeric, probability between 0-1)

Keywords: “Aspiring human resources” or “seeking human resources”



## Goal

Predict how fit the candidate is based on their available information (variable fit)

## Methodology
In the course of this project, an NLP model was implemented to assess candidates based on job position keywords. The approach involved testing various embedding models, starting from simple methods like a bag of words and progressing to advanced techniques such as transfer learning with BERT. The evaluation process aimed to achieve a similarity cosine exceeding 81% for identifying the most suitable candidates.

## Conclusion
The successful implementation of the NLP model showcased the effectiveness of employing diverse embedding techniques. From basic bag-of-words models to sophisticated BERT transfer learning, the approach yielded a substantial similarity cosine, surpassing 81%. This outcome underscores the model's capability in accurately ranking candidates based on job position keywords, offering a valuable tool for efficient and informed candidate selection.



#### Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------


