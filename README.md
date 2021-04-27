# Mask_RCNN-for-COVID-Chest-X-Rays
Detect the pneumonia (infection) in the Covid patients using Chest X Rays and also determine the severity of infection.

**Problem Statement**

To identify pneumonia location and determine the severity of pneumonia using deep learning network on chest X-ray images

**Proposed Solution**

The purposed solution is to track the pneumonia location accurately and show the percentage of the severity. This can guide doctors, radiologist to perform more accurate diagnosis on patients to save time and improve on consistency of treatment.

With Deep learning techniques like Mask RCNN, X-ray images can be more accurately and efficiently diagnose the disease by understanding the severity and type with pattern recognition. 

In the current model, data set used with X-ray images are of following types
(a) Pneumonia
(b) No Pneumonia & not normal
(c) normal

**Workflow of Project:**

1. Collection of data from Open source platforms such as Kaggle RSNA pneumonia detection challenge

2. Data pre-processing: Converting dicom (.dcm) images to .png for input to the backbone network, Arranging data into class wise folders for better access

3. Train the backbone network to classify images into two classes i.e. Pneumonia and Normal

4. Use the trained model weights along with Mask RCNN for detecting the regions of abnormalities in lungs due to pneumonia / COVID19.

5. Desired output: The % of severity, bounding box and mask for affected area

**Evaluation metrics:**

The evaluation metric considered for stage one i.e. classification is Accuracy. Test Metrics used for stage two i.e. segmentation is mean Average Precision (mAP). 

Exploratory Data Analysis

**Dataset** used for building the model is from a Kaggle competition – RSNA Pneumonia Detection Challenge.

**Classification:**

The data available was highly imbalanced, images of COVID patients were very less since it was the beginning of the pandemic and not much data was available. We considered a part of the data in the ratio 55:25:20 among the three classes namely: Pnemonia, not pneumonia & not normal, Normal. For ease of modeling, the data is redistributed into two labels (i.e., Pneumonia, Normal), converting the problem into binary classification.

**Segmentation:** 

Images used for segmentation was provided with a metadata csv file containing following columns: Index(unknown), patientID, class, x, y, height, width, Target.
 patientID: Unique ID provided to each user, not required for our problem statement
 Class: Indicating Lung opacity, No Opacity not normal and Normal
 x, y: Bounding box coordinates
 height, width: Used to draw bounding box.
 Target: Binary value column indicating Pneumonia or not Pneumonia

After the initial procession of data, convert images to .png, separating them into class wise folders.

_Data augmentation_ is performed due to lack of data to increase the amount of data the model sees and trains on. Augmentation improves accuracy of model significantly.

[capstone_poster.pdf](https://github.com/vach-aiml/Mask_RCNN-for-COVID-Chest-X-Rays/files/6386787/capstone_poster.pdf)


Narayana Darapaneni
Director - AIML
Great Learning/Northwestern University
Illinois, USA
darapaneni@gmail.com

Vachaspathi Madabhushanam
Student - AIML
Great Learning
Hyderabad, India
vachaspathi1234@gmail.com

Aravind Kumar Adhi
Student - AIML
Great Learning
Hyderabad, India
aravind.adhi@gmail.com
 
D.Krishnaprashanth
Student - AIML
Great Learning
Hyderabad, India
prashanthdharanikota@gmail.com

Shweta Ranjane
Student - AIML
Great Learning
Hyderabad, India
ranjaneshweta22@gmail.com

Anvesh Reddy Paduri
Research Assistant – AIML
Great Learning
Hyderabad, India
anwesh@greatlearning.in 
 
M Harichandan Reddy
Student - AIML
Great Learning
Hyderabad, India
harichandan25@gmail.com

Uday Shankar Pallavajula Satya
Student - AIML
Great Learning
Hyderabad, India
Udayshankar.p@dell.com
