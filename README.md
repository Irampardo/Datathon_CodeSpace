# CodeSpace Datathon! 
This is a repository to upload files related to the final exercise CodeSpace DataScience + IA Master. 
In this challenge, we will analyze the market performance of a local bakery shop by creating a database with its selling files, track current sales of the best product and deploy a model to predict sales performance

**Languages and Data Science tools**

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![mlflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)


# Description of the analysis: 

## 1. Set up

### 1.1. Create an empty database

The first thing to do will be to create a database of the selling track provided by the bakery shop

#### 1.1.A. Option AWS

1) Create an account in AWS (https://aws.amazon.com/es/rds/) --> 2) Create the bdd in AWS rds (making it public and with no security restriction) --> 3) Install DBeaver (https://dbeaver.io/download/) and connect to the AWS bdd you just created
Note: If you are going to use a CodeSpace, the IP of the CodeSpace will differ from your local computer IP, thus you need to edit a rule to allow Codespace access to AWS. To check your codespace IP run:

```bash
curl -s https://checkip.amazonaws.com
```


#### 1.1.B. Option connection to an already created bbdd

1) Install DBeaver (https://dbeaver.io/download/) and connect to a provided database by a tutor or teacher

### 1.2. Populate the database

The bakery shop provided .xlsx files of the selling track. We will 1) Convert them into .csv in excel (separated by ","), 2) Import those .csv files to our database in DBeaver, and 3) Select connecting variables as "primary key" to connect the tables or dataframes

### 1.3. Create a Github Repository and CodeSpace

#### 1.3.1. Github Repository

- In Github, set up a new repository with its Readme.md, .gitignore and requirements.txt files
- upload to main the .csv files in a folder named as "Data"
- upload accesory notebooks in a folder named as "Notebooks"
- Create a codespace and open this codespace in VSCode locally

#### 1.3.2. Create a branch

In the open CodeSpace in VSCode, create a new branch named as "EDA" where we will perform the first part of the analysis. To set up the environment do:

a) Create a conda environment. Use:

```bash
conda create -n myenv python=3.14

conda activate myenv

```

b) Install required libraries. Use:

```bash
pip install -r requirements.txt
```


## 2. Exploratory Data Analysis

### 2.1. Connection to our database

### 2.2. Processing of the datasets

- 2.2.1. Merging of the datasets
- 2.2.2. Connection to a wheather API

### 2.3. Analysis of the provided variables

- 2.3.1. Analysis of categorical variables and codification
- 2.3.2. Analysis of the numerical variables
- 2.3.3. Outliers Detection
- 2.3.4. Scaling

## 3. Model creation & Evaluation

The idea is to create a model to predict the selling trends of product "3960", so we will do several tests & metrics and use MLflow to track every test

- Test several regression models
- Test several data spliting proportions
- Test several hyperparameters

## 4. Model deployment

Once we have defined the best model, we will register it in MLflow and connect to MLflow using a docker container to deploy our model

## 5. Dashboard creation

Finally, we will create a dashboard in PowerBI that will connect to the created database. The mail goal is that this dashboard will be constantly updated and the prediction model will be showing the expected units to be baked.

