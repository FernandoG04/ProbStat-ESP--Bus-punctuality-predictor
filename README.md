# Predicting the Punctuality of Montreal's Bus Network

## Overview

This repository contains assets related to the Program Comprehensive Assessment project (ESP) submitted to Ivan T. Ivanov for the Probability and Statistics 201-HTH-05 course. The project explores and applies multiple linear regression (MLR) techniques for constructing predictive models. In this repository, you will find Jupyter Notebooks that constitute the research, as well as their corresponding datasets and other related media assets. The project aims to predict the punctuality of buses in the STM network in the City of Montreal, employing a MLR model based on predetermined variables. Please refer to the following documentation for instructions on the use of this repository.

## Table of Contents

- [Getting Started](#getting-started)
- [Notebooks](#notebooks)
    - [0. Abstract](#0-abstract)
    - [1. Introduction](#1-introduction)
    - [2. Theory](#2-theory)
        - [2.1 Multiple linear regression](#21-multiple-linear-regression)
        - [2.2 Least squares estimation of the parameters](#22-least-squares-estimation-of-the-parameters)
        - [2.3 Estimation of the error term](#23-estimation-of-the-error-term)
        - [2.4 Tests for the significance of the regression](#24-tests-for-the-significance-of-the-regression)
        - [2.5 Model building](#25-model-building)
    - [3. Model](#3-model)
        - [3.1 Data Preparation](#31-data-preparation)
            - [3.1.1 Bus](#311-bus)
            - [3.1.2 Weather](#312-weather)
            - [3.1.3 Traffic](#313-traffic)
        - [3.2 Building the model](#32-building-the-model)
            - [3.2.1 MLR with weather](#321-mlr-with-weather)
            - [3.2.2 MLR with traffic](#322-mlr-with-traffic)
    - [4. Conclusions](#4-conclusions)
    - [5. References](#5-references)
- [Datasets](#datasets)
- [Media](#media)

## Getting Started
To explore this projects, you can either:

1. **Read on GitHub:**  
    You can read the entire project on GitHub by navigating to the ["notebooks" section](#notebooks) or the ["notebooks" directory](/Notebooks clicking on the notebook you wish to view.

2. **Run Locally:**  
    Clone this repository:
    ```bash
    git clone https://github.com/FernandoG04/ProbStat-ESP--Bus-punctuality-predictor.git
    ```

## Notebooks

### [0. Abstract](/Notebooks/0_Abstract.ipynb)
This notebook provides an overview of the project.

### [1. Introduction](/Notebooks/1_Introduction.ipynb)
This notebook introduces the context and objectives of this project.

### 2. Theory
These notebooks introduce the theoretical background of the project.

- ### [2.1 Multiple linear regression](/Notebooks/2_1_Multiple_linear_regresion.ipynb)
- ### [2.2 Least squares estimation of the parameters](/Notebooks/2_2_Least_square.ipynb)
- ### [2.3 Estimation of the error term](/Notebooks/2_3_Error_term.ipynb)
- ### [2.4 Tests for the significance of the regression](/Notebooks/2_4_Significance.ipynb)
- ### [2.5 Model building](/Notebooks/2_5_Model_building.ipynb)

### 3. Model
These notebooks present the model building process, including data preparation, variable selection, and final model building.

- ### 3.1 Data Preparation
    - #### [3.1.1 Bus](/Notebooks/3_1_1_Bus.ipynb)
    - #### [3.1.2 Weather](/Notebooks/3_1_2_Weather.ipynb)
    - #### [3.1.3 Traffic](/Notebooks/3_1_3_Traffic.ipynb)

- ### 3.2 Building the model
    - #### [3.2.1 MLR with weather](/Notebooks/3_2_1_MLR_bus_weather.ipynb)
    - #### [3.2.2 MLR with traffic](/Notebooks/3_2_2_MLR_bus_traffic.ipynb)

### [4. Conclusions](/Notebooks/4_Conclusions.ipynb)
This notebook summarizes the findings of the project and provides conclusions.

### [5. References](/Notebooks/5_References.ipynb)
This notebook lists the references used in the project.

## Datasets

This section provides details about the datasets used this research project.

### List of Datasets (to be updated)

1. **STM Bus Dataset**: 
   - **Description:** Dataset containing bus-related data.
   - **Source:** This data was provided by the STM under the terms of the *Act respecting access to documents held by public bodies and the protection of personal information (R.S.Q., chapter A-2.1)*. [Click for more information.](https://www.stm.info/en/about/corporate-governance/access-information)
   - **Format:** CSV

2. **Weather Dataset**
   - **Description:** Dataset containing weather-related data.
   - **Source:** This data was retrieved from Environment and Climate Change Canada and is searchable on [their site](https://climate.weather.gc.ca/historical_data/search_historic_data_e.html). The method of retrieving the data is described in the ["Weather data"](/Notebooks/3_1_2_Weather.ipynb) notebook.
   - **Format:** CSV



3. **Traffic Dataset**
   - **Description:** Dataset containing traffic-related data.
   - **Source:** This dataset was retrieved from the open data site of the City of Montreal. [Click for more information](https://donnees.montreal.ca/) (French)
   - **Format:** CSV


## Media (to be updated)