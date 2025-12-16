# Football Player & Ball Detection – Data Annotation Project

## Project Overview

This project focuses on **data annotation and dataset preparation** for football match images using the **YOLO (You Only Look Once) annotation format**. The dataset contains images annotated with bounding boxes for detecting **football players** and the **football**.

The main objective of this project is to **understand, validate, analyze, and organize YOLO-formatted annotations**, making the dataset ready for use in object detection models. **No machine learning model training was performed**, as the primary goal is data annotation quality and analysis.

## Project Objectives

* Understand YOLO annotation format
* Organize and clean the dataset structure
* Validate annotation quality using visualization
* Perform exploratory analysis on annotations
* Prepare a model-ready dataset (without training)

## Dataset Description

* **Source:** Kaggle – Football YOLOv8 Dataset
* **Data Type:** Images with YOLO annotations
* **Annotation Format:** YOLO (normalized bounding boxes)

### Classes

| Class ID | Label    |
| -------- | -------- |
| 0        | Player   |
| 1        | Football |

### YOLO Annotation Format

Each label file contains:

```
<class_id> <x_center> <y_center> <width> <height>
```

All values are **normalized between 0 and 1** relative to image width and height.

## Dataset Structure (After Cleaning)

Initially, image and label files were mixed in a single folder. As part of the data annotation process, the dataset was cleaned and reorganized into the following structure:

```
football_yolo/
│
├── images/
│   ├── img_001.jpg
│   ├── img_002.jpg
│
├── labels/
│   ├── img_001.txt
│   ├── img_002.txt
│
└── data.yaml
```

## Tools & Technologies Used

* **Python**
* **OpenCV** – annotation visualization
* **Matplotlib** – data visualization
* **Kaggle Notebook** – experimentation environment
* **YOLO Format** – object detection annotation standard

## Annotation Validation

To ensure annotation quality, bounding boxes were **visually verified** by overlaying them on images using OpenCV. This step helped confirm:

* Correct object localization
* Proper class labeling
* Accurate bounding box sizes

This validation ensures the dataset is reliable for downstream object detection tasks.

## Challenges Identified

* **Class imbalance** (players >> football)
* **Small object detection** for football
* Mixed dataset structure requiring manual reorganization

## Future Improvements

* Apply data augmentation techniques
* Add train/validation/test split
* Train and evaluate a YOLOv8 object detection model
* Improve annotation consistency for small objects

## Key Takeaways

* Gained hands-on experience with YOLO data annotation format
* Learned dataset cleaning and validation techniques
* Performed annotation-focused exploratory data analysis
* Prepared a clean, model-ready object detection dataset

## Conclusion

This project demonstrates a **complete data annotation workflow**, including dataset cleaning, annotation validation, and analysis. Although no machine learning model was trained, the dataset is fully prepared and suitable for training object detection models such as YOLOv8.
