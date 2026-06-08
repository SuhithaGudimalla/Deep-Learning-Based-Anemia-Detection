# Deep Learning-Based Anemia Detection Using Palm Images and Red Blood Cell Morphology Classification

## Overview

Anemia is a common blood disorder characterized by a reduced number of healthy red blood cells or insufficient hemoglobin levels. Early detection is important for timely diagnosis and treatment.

This project proposes a two-stage deep learning framework for anemia detection using both palm images and red blood cell (RBC) images. The system first performs anemia screening using palm images and then conducts detailed RBC analysis to detect anemia and classify abnormal RBC morphologies associated with different blood disorders.

---

## Objectives

* Detect anemia using palm images through deep learning.
* Detect anemia using microscopic RBC images.
* Identify abnormal RBC morphologies.
* Associate detected RBC morphologies with possible blood-related diseases.
* Provide an automated and non-invasive anemia screening solution.

---

# Datasets Used

## 1. Palm Dataset for Anemia Detection

Dataset Link:

https://www.kaggle.com/datasets/shreyacgosavi/palm-dataset-anemia

Description:

* Contains palm images of anemic and non-anemic individuals.
* Used for non-invasive anemia detection.
* The model learns color and redness variations present in the palm region.

---

## 2. AneRBC Dataset

Dataset Link:

https://www.kaggle.com/datasets/jocelyndumlao/anerbc-anemia-diagnosis-using-rbc-images

Description:

* Contains microscopic images of red blood cells.
* Includes healthy and anemic RBC samples.
* Used for anemia classification and morphology analysis.

---

# System Architecture

The complete system consists of three major modules.

## Module 1: Palm-Based Anemia Detection

### Process

1. Input palm image.
2. Image preprocessing and normalization.
3. Deep learning model extracts color-related features.
4. The model analyzes palm redness and color distribution.
5. Classification into:

   * Anemic
   * Non-Anemic

### Why Palm Images?

Anemic individuals often exhibit reduced redness in the palm due to lower hemoglobin concentration. Deep learning models learn these visual patterns automatically and use them for classification.

### Result

Palm-Based Anemia Detection Accuracy:

95%


<img width="364" height="454" alt="image" src="https://github.com/user-attachments/assets/d76e2e8c-fdc2-4da5-badb-788faadd2a78" />


---

## Module 2: Phase 1 - RBC-Based Anemia Detection

### Process

1. Input microscopic RBC image.
2. Image preprocessing.
3. RBC feature extraction using deep learning.
4. Classification into:

   * Anemic
   * Non-Anemic

### Purpose

This phase confirms anemia using RBC characteristics and microscopic cell appearance.

### Result

RBC Anemia Detection Accuracy:

89%

---

## Module 3: Phase 2 - RBC Morphology Classification

### Process

1. RBC image identified as abnormal.
2. Morphological characteristics are analyzed.
3. Deep learning model classifies RBC morphology.
4. Disease associations are generated based on detected morphology.

### Morphologies Identified

* Microcytic RBCs
* Macrocytic RBCs
* Elliptocytes
* Target Cells
* Normocytic Variations


<img width="492" height="813" alt="image" src="https://github.com/user-attachments/assets/af2cf175-4eb3-4a6f-b87d-125293d94e82" />



### Possible Disease Associations

| Morphology            | Possible Disease          |
| --------------------- | ------------------------- |
| Microcytic RBCs       | Iron Deficiency Anemia    |
| Macrocytic RBCs       | Vitamin B12 Deficiency    |
| Elliptocytes          | Hereditary Elliptocytosis |
| Target Cells          | Thalassemia               |
| Normocytic Variations | Mild Blood Disorders      |

### Result

RBC Morphology Classification Accuracy:

86%

---

# Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* OpenCV
* Matplotlib
* Google Colab

---

# Model Workflow

Step 1:
Palm Image → Anemia Detection

If anemia is suspected:

Step 2:
RBC Image → Phase 1 Anemia Classification

If abnormal RBCs are detected:

Step 3:
Phase 2 Morphology Classification

Output:

* Anemia Status
* RBC Morphology Type
* Possible Disease Association

---

# Results Summary

| Module                                | Accuracy |
| ------------------------------------- | -------- |
| Palm-Based Anemia Detection           | 95%      |
| Phase 1 RBC Anemia Detection          | 89%      |
| Phase 2 RBC Morphology Classification | 86%      |

---

# Future Improvements

* Integration with mobile healthcare applications.
* Real-time clinical decision support.
* Expansion to additional blood disorders.
* Multi-class disease prediction using larger datasets.
* Deployment as a web and mobile application.

---

# Conclusion

This project demonstrates the effectiveness of deep learning for anemia screening using both palm and red blood cell images. The proposed framework combines non-invasive palm-based detection with detailed RBC morphology analysis, providing a comprehensive approach for anemia diagnosis and blood disorder assessment.

