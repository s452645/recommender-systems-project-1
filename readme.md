# Recommender Systems - Project 1

Author: Bartłomiej Grochowski

## Project description
The project is a part of the Recommender Systems class (conducted by [Mr. Piotr Zioło](https://github.com/PiotrZiolo)) at the Department of Mathematics and Computer Science, Adam Mickiewicz University.
The goal is to prepare a content-based recommender with the best possible HR@10 result and compare it to those achieved by Amazon recommender.
The data and the code framework was provided beforehand.

## Files
Most of the key code is located in the Jupyter Notebook files:
- `project_1_data_preparation.ipynb`
- `project_1_recommender_and_evaluation.ipynb`

There are also generated HTML files for both of them, containing the results of running the code.

## Dependencies
To run the code on your local machine, the following libraries must be installed:
- Anaconda with Python 3.8
- Dependencies listed in the `environment.yml` file 

The recommended way to prepare an environment is to run the following commands in the project root directory:
1. `conda env create --name your-env-name -f environment.yml`
2. `conda activate your-env-name`

And then, in order to open Jupyter Notebook:
`jupyter notebook`

## Algotithms and results
The final solution after tuning uses Linear Regression CBUI Recommender with 6 negative interactions generated for each positive (`n_neg_per_pos` parameter). The results, compared to the Amazon Recommender:

| Recommender                        | HR@1     | HR@3     | HR@5     | HR@10        | NDCG@1   | NDCG@3   | NDCG@5   | NDCG@10 |
|------------------------------------|----------|----------|----------|--------------|----------|----------|----------|---------|
| Linear Regression CBUI Recommender | 0.042091 | 0.093347 | 0.145282 | **0.228445** | 0.042091 | 0.072030 | 0.092835 | 0.12023 |
| Amazon Recommender                 | 0.037339 | 0.101494 | 0.143245 | **0.215207** | 0.037339 | 0.073816 | 0.091083 | 0.11423 |
