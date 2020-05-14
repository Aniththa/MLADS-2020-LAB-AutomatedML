# MLADS 2020 LAB: Building a machine learning model using Automated Machine Learning in Azure ML
The content below is a guide for a self-paced lab to understand the E2E Automated Machine Learning capabilities both through the Python code experience and UI no-code experience. 

# Key Words
- Automated ML, Azure Machine Learning, Hyperparameter tuning, Python, JupyerLab, No-code UI

# Table of Contents
1. [Prerequisites](#prereqs)
1. [Automated ML Introduction](#introduction)
1. [The studio Introduction](#studio)
1. [Setup a Compute Instances](#compute)
1. [Train in JupyertLab](#train)
1. [Documentation](#documentation)
1. [Running using python command](#pythoncommand)
1. [Troubleshooting](#troubleshooting)

<a name="prereqs"></a>
# Prerequisites
draft-- have an azure account, create a workspace through the portal

# Lab agenda
* Introduction to automated ML
* The studio and model authoring experiences
* Creating a compute instance
* Running a python code automated ML experiment
* Understanding forecasting parameters and concepts
* Train, evaluate, and deploy your model
* Easily perform these steps again in a no-code experience

<a name="introduction"></a>
# Automated ML introduction
Automated machine learning (automated ML) builds high quality machine learning models for you by automating model and hyperparameter selection. Bring a labelled dataset that you want to build a model for, automated ML will give you a high quality machine learning model that you can use for predictions.

If you are new to Data Science, automated ML will help you get jumpstarted by simplifying machine learning model building. It abstracts you from needing to perform model selection, hyperparameter selection and in one step creates a high quality trained model for you to use.

If you are an experienced data scientist, automated ML will help increase your productivity by intelligently performing the model and hyperparameter selection for your training and generates high quality models much quicker than manually specifying several combinations of the parameters and running training jobs. Automated ML provides visibility and access to all the training jobs and the performance characteristics of the models to help you further tune the pipeline if you desire.

<a name="studio"></a>
## The studio and automated ML authoring experience
Azure ML has a suite of authoring experiences in a user-interface format in [the studio](https://ml.azure.com). 

1. Visit [ml.azure.com](https://ml.azure.com)
2. Select your `directory`, `subscription`, and `workspace`

Automated ML is supported by three execution environments:
* Compute Instances
* Local Conda environment
* Azure Databricks 

<a name="compute"></a>
## Setup using Compute Instances - Jupyter based notebooks from a Azure Virtual Machine
In this lab we will be focusing on the Compute Instance environment.

1. On the left hand panel under the `Manage` section, click on `Compute`
2. Click `+ New` to create a new compute. *It will take a couple minutes for this compute to to spin-up.*
3. When the compute `Status` is `Running`, select the `JupyertLab` Application URI.

<a name="compute"></a>
## Run the lab on JupyterLab
In this part of the lab we will be covering a python code 
