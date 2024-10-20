# Enhancing Reliability in Electrical Grids: A Hybrid Machine Learning Approach for Electrical Faults Classification

This repository contains the code, data, and models used in the research project **"Enhancing Reliability in Electrical Grids: A Hybrid Machine Learning Approach for Electrical Faults Classification."** The goal of this project is to improve the classification of electrical faults in transmission lines by applying hybrid machine learning models.

## Project Overview

Transmission lines are critical to electrical grids, ensuring the efficient transfer of electricity across vast areas. However, various faults can occur, which need accurate identification for quick resolution. This research investigates multiple machine learning algorithms and ensemble techniques to develop a robust fault classification system, including hybrid models combining Random Forest, Decision Tree, KNN, Naive Bayes, and others.

## Hybrid Machine Learning Models Used

The project implements and compares several hybrid models, including:

- **Model-1**: Random Forest (RF) + Decision Tree (DT)
- **Model-2**: Random Forest (RF) + KNN
- **Model-3**: Naive Bayes (NB) + Decision Tree (DT)
- **Model-4**: KNN + Naive Bayes (NB)
- **Model-5**: Random Forest (RF) + Naive Bayes (NB)

Each model has been designed to exploit the strengths of individual algorithms, enhancing the accuracy and reliability of fault classification.

## About Dataset

### Context
The transmission line is a critical component of the power system, tasked with transmitting electricity from generation sources to the distribution network. As power demand and grid complexity have increased, ensuring the reliable operation of transmission lines has become essential. Transmission lines, part of interconnected grids, are susceptible to disturbances and electrical faults. Fault detection, classification, and response in the shortest possible time are vital for maintaining grid stability and avoiding power outages.

Transmission line faults must be identified and classified accurately to trigger protection equipment that isolates the fault and safeguards the rest of the power system. Modern approaches use pattern recognition technologies, such as Artificial Neural Networks (ANNs), to distinguish between healthy and faulty system states, and between different types of faults. ANNs are particularly effective due to their robustness, noise tolerance, and ability to generalize across different operating conditions.

This dataset models various electrical transmission system faults and aims to classify them using machine learning approaches, including ANN-based algorithms. The data has been simulated to reflect different fault types in a transmission system, providing a foundation for developing and evaluating fault classification models.

### Dataset Overview (`classData.csv`)
The `classData.csv` file contains labeled data to classify different types of faults that may occur in a three-phase electrical transmission system. It includes both input measurements and fault labels for supervised learning.

#### Inputs
The input features represent electrical currents and voltages for the three phases (A, B, and C):
- `Ia`, `Ib`, `Ic`: Current in phases A, B, and C
- `Va`, `Vb`, `Vc`: Voltage in phases A, B, and C

#### Outputs (Fault Types)
The output labels indicate the type of fault using a combination of binary indicators for Ground (G), Phase A (A), Phase B (B), and Phase C (C):

- **[0 0 0 0]**: No Fault
- **[1 0 0 1]**: LG Fault (Between Phase A and Ground)
- **[0 0 1 1]**: LL Fault (Between Phase A and Phase B)
- **[1 0 1 1]**: LLG Fault (Between Phases A, B, and Ground)
- **[0 1 1 1]**: LLL Fault (Between all three phases)
- **[1 1 1 1]**: LLLG Fault (Three-phase symmetrical fault with Ground)

### Examples:

Here are a few examples from the dataset showing how inputs are mapped to fault types:

- **[0 0 0 0]**: No Fault
- **[1 0 0 1]**: LG Fault (Between Phase A and Ground)
- **[0 0 1 1]**: LL Fault (Between Phase A and Phase B)
- **[1 0 1 1]**: LLG Fault (Between Phases A, B, and Ground)
- **[0 1 1 1]**: LLL Fault (Between all three phases)
- **[1 1 1 1]**: LLLG Fault (Three-phase symmetrical fault)

This dataset provides a basis for building a machine learning model to predict the type of fault based on the current and voltage measurements in the transmission system.

## How to Use the Code

### Prerequisites

- Python 3.x
- Required libraries:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `matplotlib`
  - `seaborn`


