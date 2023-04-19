# ibm_recommendation_engine
Code for the "Recommendations with IBM" project of the Udacity Data Science Nanodegree course

The task in this project is to build a recommendation engine for actual data from the IBM Watson Studio platform. The data contains several articles, their entire content as well as summaries and headlines. It also contains a set of users and data about which articles in the dataset they interacted with.

In the notebook, a recommendation engine is implemented that uses collaborative filtering/user-user based recommendation methods as well as content-based recommendation methods for entirely new users. For the latter, recommendations are made based on popular "topics" in our articles, where for the topic modelling a hybrid approach is chosen based on Latend Dirichlet Allocation (LDA) and on keywords from a large language model (LLM), in our case GPT-3.

The main code is contained within the `Recommendations_with_IBM.ipynb` jupyter notebook.

# Recommended software stack

The following `python` packages are required for running the `Recommendations_with_IBM.ipynb` jupyter notebook:

- pandas
- numpy
- matplotlib
- justext
- transformers
- nltk
- scikit-learn
- gensim
- ipykernel

In case you want to run the GPT-3 part of the notebook using your own openAI API key (as opposed to using my pre-computed results), you also need to install the `openai` python library:

```
pip install openai
```

We also include a `requirements.txt` file that can be used to install the above software packages (except for `openai`) and which has been successfully tested inside a `python` virtual environment. To install the required software packages this way in a new virtual environment, run the following commands on your local machine (from within the directory of this project's repository):

```
python -m venv ibm_rec_env
source ibm_rec_env/bin/activate
pip install -r requirements.txt
python -m ipykernel install --user --name=ibm_rec_env
```

This creates (and activates) a new virtual `python` environment called `ibm_rec_env` that can be used to run the code in the main jupyter notebook. It also adds the environment to the kernels available in your local jupyter installation, such that it should be available to choose inside your jupyter notebooks.