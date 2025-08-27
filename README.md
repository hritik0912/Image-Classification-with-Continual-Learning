# Machine Learning Mini-Project 2: Image Classification with Continual Learning

This project tackles a two-part image classification challenge using the CIFAR-10 dataset, focusing on continual learning scenarios where the data distribution changes over time. The primary method used is a "Learning with Prototypes" (LwP) classifier.

---

## 📝 Project Overview

This project is a submission for the "CS771 - Intro to ML" course. It involves training and evaluating an LwP classifier on a sequence of 20 datasets derived from CIFAR-10.

* **Task 1:** Train a classifier on 10 datasets with similar data distributions.
* **Task 2:** Adapt and train the classifier on another 10 datasets, each with a different data distribution.

The project also includes a literature review component, for which the team analyzed the paper "Deja vu: Continual model generalization for unseen domains."

---

## 🗂️ Repository Structure

* `report_group46.pdf`: The detailed project report, outlining the methodology, results, and analysis.
* `TASK_1.ipynb`: Jupyter Notebook for the implementation of Task 1.
* `TASK_2.ipynb`: Jupyter Notebook for the implementation of Task 2.
* `Mini_Project2_Trails.ipynb`: An exploratory notebook used for testing different feature extraction models and LwP classifier variations.

---

## ⚙️ Dependencies

Before running the notebooks, make sure you have the following libraries installed:

* **Core Libraries:**
    * `torch`
    * `torchvision`
    * `numpy`
    * `tqdm`
    * `sklearn`
    * `PIL`
    * `timm`

You can install these dependencies using pip:
```bash
pip install torch torchvision numpy tqdm scikit-learn pillow timm
```

---

## 🚀 Getting Started

To get started with this project, follow these steps:

### 1. **Clone the Repository**

First, clone this repository to your local machine:
```bash
git clone <repository-url>
```

### 2. **Download the Dataset**

The dataset for this project can be downloaded from the following URL:
[https://tinyurl.com/cs771-mp2-data](https://tinyurl.com/cs771-mp2-data)

### 3. **Running the Notebooks**

The project is divided into two main parts, each with its own Jupyter Notebook.

* **For Task 1:**
    * Open and run the `TASK_1.ipynb` notebook. This will train the LwP classifier on the first 10 datasets and generate an accuracy matrix for the models' performance.

* **For Task 2:**
    * Open and run the `TASK_2.ipynb` notebook. This will continue the training process on the next 10 datasets with varying distributions and evaluate the models' ability to adapt.

* **Exploratory Notebook:**
    * The `Mini_Project2_Trails.ipynb` notebook can be used to understand the initial experiments and model selection process.

---

## 📈 Results

The project's final results, including the accuracy matrices for both tasks and a confusion matrix for the final model, are detailed in the `report_group46.pdf` file. The key findings from the report are:

* **Best Feature Extractor:** ViT-Base, with an accuracy of **84.68%**.
* **Task 1 Approach:** A combination of "LWP Hard" and "LWP Soft" methods with Mahalanobis distance.
* **Task 2 Approach:** A combination of "$T^2PL$ & RandMix," achieving an accuracy of **81.7%** with the final model.

For more details on the implementation and results, please refer to the full report and the Jupyter Notebooks.
