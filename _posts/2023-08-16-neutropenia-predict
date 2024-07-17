---
layout: post
title: "Predicting deaths and hospitalization days in patients with neutropenia on MIMIC-IV using AI"
categories: []
tags: []
description:
---

In this post, we aim to leverage the data collected from the Medical Information Mart for Intensive Care (MIMIC-IV) version 4, a repository managed by the MIT Laboratory for Computational Physiology, which houses medical data for research purposes. This dataset, presented in [1], consists of patient information from the Beth Israel Deaconess Medical Center (BIDMC). Before accessing the dataset, ethical guidelines were followed as guided by the [CITI Program course on Data or Specimens Only Research](https://physionet.org/about/citi-course/) and the data usage was approved by the course instructor André Santanchè at the post-graduate discipline of Data Science and Visualization in Health at [Unicamp](https://www.unicamp.br/unicamp/). Our objective is to develop classification models for predicting mortality in neutropenic patients without cancer and regression models for predicting hospitalization days for patients with or without cancer.

<br>

### Wait. What is neutropenia and why it is relevant?

Neutropenia is one of the most concerning complications of chemotherapy and its prediction remains difficult [2] and this is when machine learning comes into place. If we can model this problem to early detect the possibility of dying and staying for a long time at the hospital based on the exams we can apply AI to a critical disease and guide clinical treatment decisions [3].

Important Statement: It is important to emphasize that although the problem was initially presented by a medical professional, the final results have not been reviewed by medical experts. Our team comprises computer science students and our primary aim is to showcase the application of data science tools to this issue. As such, this work serves as an illustrative example of how data science techniques can be applied to address challenges in the medical domain. It’s important to note that while our findings are presented here, no definitive medical conclusions should be drawn from this study.

<br>

### Data Preparation Steps

Firstly, the dataset has been preprocessed and filtered to focus on patients with neutropenia, with steps documented that can be seen at this [link](https://datasci4health.github.io/home/data/mimic/neutropenia/).

After that, 10 steps were taken, the following being described:

1. Removed rows with unidentified values in the ‘race’ column and rows with marital status ‘N.’
2. Merged admission and diagnosis data using the Pandas library based on the hadm id.
3. Created a new column indicating cancer diagnosis from the presence of “malignant neoplasm” in the diagnosis title. Added columns for related diagnoses based on expert insights and literature [4,5,6]. Removed duplicate rows.
4. Filtered the dataset to include only the percentage of neutrophil count (item id 515256).
5. Merged lab events and item descriptions based on the item id.
6. Filtered the data to retain only relevant rows for the chosen lab test.
7. Created new features by calculating mean, median, count, max and min values of exam results per admission. Removed duplicate rows.
8. Merged admission, diagnosis and lab events data into a consolidated dataset.
9. Removed undesired columns, checked for missing values, created columns for patient survival, hospitalization days and ensure data integrity.
10. Conducted exploratory data analysis with visualizations to validate data treatment and gain insights into hospitalization days and neutrophil count distribution for patients with and without cancer.

<br>

### Exploratory Data Analysis

Exploratory Data Analysis (EDA) is a crucial step in the data science process that involves visualizing and summarizing the dataset to gain valuable insights. During EDA, we examined various visualizations, including histograms and missing value distributions, to understand the data’s characteristics and identify potential patterns or trends. These visualizations validate the data’s integrity and allow us to make informed decisions for building predictive models and drawing meaningful conclusions about patient outcomes in cancer cases.

<img src="https://raw.githubusercontent.com/" width="500px" height="auto">




