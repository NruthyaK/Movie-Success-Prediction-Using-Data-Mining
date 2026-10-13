# 🎬 Movie Success Prediction Using Data Mining

A machine learning classification project that explores how movie success can be predicted using pre-release movie characteristics.

## 📌 Project Overview

Can we predict whether a movie will be a **Hit, Average, or Flop before its release?**

This project explores that question using data mining and classification algorithms in **WEKA Explorer**.

During the project, I realized that attributes such as box-office revenue and audience ratings are only available after a movie is released. Since the goal was to explore pre-release prediction, I redesigned the dataset to focus on movie production, planning, and release-related attributes instead.

The project demonstrates data preprocessing, decision tree classification, model evaluation, and comparison of multiple machine learning algorithms.

## 🎯 Objectives

- Explore the importance of selecting relevant attributes for a prediction problem.
- Prepare a dataset containing pre-release movie characteristics.
- Classify movies into Hit, Average, and Flop categories.
- Implement multiple classification algorithms using WEKA.
- Compare model performance using accuracy, precision, recall, F-measure, Kappa statistics, and confusion matrices.
- Understand the limitations of model evaluation using synthetic data.

## 📂 Dataset Information

The project uses a **synthetically generated dataset** containing:

- **Instances:** 300
- **Attributes:** 19 total
- **Input attributes:** 18
- **Target attribute:** `success`
- **Target classes:** Hit, Average, Flop

The dataset is provided in ARFF and CSV formats.

### Attributes

| Category | Attributes |
|---|---|
| Financial | `budget_millions`, `marketing_budget_millions` |
| Movie details | `duration_minutes`, `genre`, `certification`, `primary_language` |
| Production | `director_previous_films`, `lead_cast_count`, `production_company_tier`, `production_days` |
| Release planning | `release_season`, `holiday_release`, `competition_level`, `distribution_type`, `international_release` |
| Movie background | `is_sequel`, `is_franchise`, `source_material` |
| Target | `success` |

Box-office revenue, critic ratings, audience ratings, review scores, popularity scores, and social media attributes are excluded from the final dataset.

### ⚠️ Dataset Disclaimer

The dataset and target labels are synthetic and were generated for educational experimentation. They are not real IMDb records or verified movie-industry outcomes. The classification results demonstrate the workflow on simulated data and should not be interpreted as real-world prediction accuracy.

## 🛠️ Tools and Technologies

- **WEKA Explorer** — data preprocessing and classification
- **ARFF** — dataset format for WEKA
- **CSV** — spreadsheet-compatible dataset format
- **Machine Learning** — supervised classification
- **10-fold cross-validation** — model evaluation

## 🤖 Algorithms Implemented

The following classifiers were evaluated:

1. **J48 Decision Tree** — generates interpretable classification rules.
2. **Naive Bayes** — uses probabilities to classify instances.
3. **Random Forest** — combines multiple decision trees.
4. **IBk (k-Nearest Neighbors)** — classifies instances based on nearby examples.
5. **ZeroR** — provides a baseline by predicting the majority class.

## 📊 Experimental Results

The classifiers were evaluated using 10-fold cross-validation on the same 300-instance dataset.

| Algorithm | Accuracy |
|---|---:|
| J48 Decision Tree | 73.00% |
| Naive Bayes | 72.00% |
| Random Forest | 71.33% |
| IBk (kNN) | 54.33% |
| ZeroR baseline | 54.00% |

**Best observed result:** J48 achieved 73.00% accuracy in this experiment.

J48 also produced an interpretable decision tree, making it useful for examining how the selected attributes contribute to the model's classifications.

These results are specific to the synthetic dataset and the classifier configurations used.

## ⚙️ How to Run the Project

### Requirements

- WEKA installed on your computer
- The dataset file `MovieSuccessPrediction_Preprocessed_300.arff`

### Steps

1. Clone or download this repository.
2. Open **WEKA Explorer**.
3. Navigate to the **Preprocess** tab.
4. Click **Open file** and select the ARFF dataset.
5. Verify that the dataset contains 300 instances and 19 attributes.
6. Navigate to the **Classify** tab.
7. Set the class attribute to `success`.
8. Select a classifier, such as `trees → J48`.
9. Choose **10-fold cross-validation**.
10. Click **Start** to run the experiment.
11. Examine the accuracy, detailed class-wise metrics, confusion matrix, and decision tree.
12. Repeat with Naive Bayes, Random Forest, IBk, and ZeroR to compare performance.

## 📈 Evaluation Metrics

The project uses several evaluation measures:

- **Accuracy:** proportion of correctly classified instances.
- **Precision:** proportion of correct predictions among instances predicted to belong to a class.
- **Recall:** proportion of actual instances of a class correctly identified.
- **F-measure:** combines precision and recall.
- **Kappa statistic:** measures agreement adjusted for chance.
- **Confusion matrix:** shows correct and incorrect predictions for each class.

## 💡 Key Learnings

Through this project, I learned that:

- Selecting attributes that match the prediction objective is essential.
- Information available before release must be distinguished from information available only afterward.
- Different classification algorithms can perform differently on the same dataset.
- Accuracy alone does not provide a complete picture of model performance.
- Confusion matrices and class-wise metrics help identify where a model struggles.
- Data science is an iterative process involving problem definition, data preparation, experimentation, and evaluation.

## 🚧 Limitations and Future Work

### Current limitations

- The dataset is synthetic rather than collected from actual movie releases.
- The success labels are generated using predefined rules, which influence the classification results.
- The observed accuracy does not establish how well the model predicts real-world movie success.

### Future improvements

- Collect real movie data from documented, appropriate sources.
- Define Hit, Average, and Flop using an explicit, independently verifiable criterion.
- Evaluate the model on real movies using only information available before release.
- Compare additional algorithms and tune their parameters.
- Examine class-wise performance and improve the identification of less accurately predicted classes.

## 👤 Project Context

This project was developed as an academic learning exercise to explore data mining, classification algorithms, and model evaluation using WEKA.

The main takeaway was that building a useful prediction system begins with defining the problem correctly and choosing relevant data—not simply selecting a machine learning algorithm.

---

**If you find this project useful, feel free to explore the dataset and experiment with the classifiers.**