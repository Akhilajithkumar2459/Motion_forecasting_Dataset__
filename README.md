# Indian Road Motion Forecasting Dataset (Lite Version)

## 1. Overview

The **Indian Road Motion Forecasting Dataset (Lite Version)** is a curated subset designed to support research on **trajectory prediction and motion forecasting of heterogeneous road users in unstructured Indian traffic environments**. The dataset contains annotated image frames extracted from traffic videos along with object-level annotations for multiple road users.

Indian traffic scenes are typically complex and highly dynamic due to the interaction between different road users such as vehicles, cyclists, and pedestrians. This dataset captures these interactions and provides annotated data that can be used to develop and evaluate **motion prediction and trajectory forecasting models**.

The dataset supports research in the following areas:

- Motion forecasting of road users  
- Trajectory prediction in unstructured traffic environments  
- Multi-agent interaction modeling  
- Autonomous driving perception systems  
- Behavior-aware trajectory prediction  

---

## 2. Dataset Structure

The dataset is organized as follows:
Dataset/
│
├── images/
│ ├── frame_000001.jpg
│ ├── frame_000002.jpg
│ ├── frame_000003.jpg
│ └── ...
│
├── labels/
│ ├── frame_000001.txt
│ ├── frame_000002.txt
│ ├── frame_000003.txt
│ └── ...
│
└── metadata/
└── dataset_info.txt


### images/

Contains RGB image frames extracted from traffic videos captured in Indian urban traffic environments.

### labels/

Contains annotation files corresponding to each image frame in **YOLO format**.

### metadata/

Contains additional information related to the dataset such as class descriptions and annotation details.

---

## 3. Annotation Format

Annotations are provided in **YOLO object detection format**, where each line in a label file represents one object instance in the image.

### YOLO Annotation Format
<class_id> <x_center> <y_center> <width> <height>

Where:

- **class_id** – Integer identifier for the object class  
- **x_center** – Normalized x-coordinate of the bounding box center  
- **y_center** – Normalized y-coordinate of the bounding box center  
- **width** – Normalized width of the bounding box  
- **height** – Normalized height of the bounding box  

All coordinates are **normalized between 0 and 1** relative to the image dimensions.

---

## 4. Object Classes

The dataset includes annotations for the following classes of road users:

| Class ID | Class Name |
|--------|--------|
| 0 | Vehicle |
| 1 | Cyclist |
| 2 | Pedestrian |

These classes represent the most common road users encountered in Indian traffic scenes.

---

## 5. Intended Tasks

The dataset can be used for several computer vision and autonomous driving tasks, including:

- Object detection of heterogeneous road users  
- Multi-agent trajectory prediction  
- Motion forecasting in unstructured traffic scenes  
- Interaction modeling between road users  
- Autonomous driving perception research  

The dataset can also serve as input for **trajectory extraction pipelines used in motion forecasting frameworks**.

---

## 6. Data Collection and Preprocessing

The dataset was constructed using the following pipeline:

1. Traffic videos were collected from **urban Indian road environments**.
2. Videos were converted into **frame-level RGB images**.
3. Road users were annotated using a **semi-automatic annotation process**.
4. All annotations were manually verified for quality and accuracy.
5. The annotations were exported into **YOLO format** for compatibility with modern object detection frameworks.

---

## 7. Usage Notes

- Bounding box coordinates are provided in **normalized YOLO format**.
- Each label file corresponds to a single image frame.
- Frames may contain **multiple road users across different classes**.
- The dataset can be used for both **object detection and trajectory-based research**.

---

## 8. Ethical Considerations

The dataset was collected from **public road environments** where individuals appear as part of normal traffic activity.

No personally identifiable information is intentionally included in the dataset. The dataset is intended strictly for **academic research purposes** in computer vision and autonomous driving.

---

## 9. Limitations

- This dataset represents a **Lite Version** of a larger dataset used in the research study.
- Only bounding box annotations are provided.
- Environmental metadata such as **weather conditions, lighting variations, and time of day** are not explicitly labeled.
- The dataset may not represent all possible traffic scenarios.

---

## 10. License

This dataset is released **for academic research purposes only**.

Commercial use, redistribution, or modification for commercial applications is **not permitted without permission from the authors**.

---

