# MLADS 2020 LAB: Building a machine learning model using Automated Machine Learning in Azure ML
The content below is a guide for a self-paced lab to understand the E2E Automated Machine Learning capabilities both through the Python code experience and UI no-code experience. 

While it's not required, a basic understanding of Azure Machine Learning will be helpful for understanding the solution. The following resources can help introduce you to AML:

1. [Azure Machine Learning Overview](https://azure.microsoft.com/services/machine-learning/)
2. [What is automated machine learning?](https://docs.microsoft.com/azure/machine-learning/concept-automated-ml)
3. [Automated ML Sample Notebooks on Github](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/automated-machine-learning)

# Key Words
- Automated ML, Azure Machine Learning, Hyperparameter tuning, Python, JupyerLab, No-code UI

# Table of Contents
1. [Prerequisites](#prereqs)
1. [Automated ML Introduction](#introduction)
1. [The studio Introduction](#studio)
1. [Lab Part 1. Train a regression model using the Automated ML UI](#automlUI)
1. [Setup a Compute Instances](#compute)
1. [Lab Part 2. Train a classification model using Automated ML in JupyertLab](#train)
1. [Next Steps](#complete)

<a name="prereqs"></a>
# Prerequisites
All you need is access to an [Azure subscription](https://azure.microsoft.com/free/) and an [Azure Machine Learning Workspace](https://docs.microsoft.com/azure/machine-learning/how-to-manage-workspace) that you'll create below.

### [Create a workspace](https://docs.microsoft.com/en-us/azure/machine-learning/tutorial-1st-experiment-sdk-setup#create-a-workspace)
An Azure Machine Learning workspace is a foundational resource in the cloud that you use to experiment, train, and deploy machine learning models. It ties your Azure subscription and resource group to an easily consumed object in the service.

You create a workspace via the Azure portal, a web-based console for managing your Azure resources.

1. Sign in to [Azure portal](https://portal.azure.com/) by using the credentials for your Azure subscription.

1. In the upper-left corner of Azure portal, select **+ Create a resource**.

    ![Create a new resource](images/create-workspace.gif)

1. Use the search bar to find **Machine Learning**.

1. Select **Machine Learning**.

1. In the **Machine Learning** pane, select **Create** to begin.

1. Provide the following information to configure your new workspace:

   Field|Description 
   ---|---
   Workspace name |Enter a unique name that identifies your workspace. In this example, we use **docs-ws**. Names must be unique across the resource group. Use a name that's easy to recall and to differentiate from workspaces created by others.  
   Subscription |Select the Azure subscription that you want to use.
   Resource group | Use an existing resource group in your subscription or enter a name to create a new resource group. A resource group holds related resources for an Azure solution. In this example, we use **docs-aml**. 
   Location | Select the location closest to your users and the data resources to create your workspace.
   Workspace edition | Select **Basic** as the workspace type for this tutorial. The workspace type (Basic & Enterprise) determines the features to which you’ll have access and pricing. Everything in this tutorial can be performed with either a Basic or Enterprise workspace.

1. After you are finished configuring the workspace, select **Review + Create**. 

   When the process is finished, a deployment success message appears. 
 
 1. To view the new workspace, select **Go to resource**.


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
