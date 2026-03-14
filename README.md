Indian Road Motion Forecasting Dataset (Lite Version)
1. Overview

The Indian Road Motion Forecasting Dataset (Lite Version) is a curated subset designed to support research on trajectory prediction and motion forecasting of heterogeneous road users in unstructured Indian traffic environments. The dataset contains annotated frames extracted from traffic videos along with object-level annotations for different road users.

The dataset captures the complexity of real-world Indian traffic, including interactions between multiple road users such as vehicles, cyclists, and pedestrians. It is particularly useful for studying multi-agent motion forecasting in environments where traffic behavior is less structured compared to Western road systems.

This dataset enables research in the following areas:

Motion forecasting of road users

Trajectory prediction in unstructured traffic

Multi-agent interaction modeling

Autonomous driving perception systems

Behavior-aware trajectory prediction

2. Dataset Structure

The dataset is organized as follows:

Dataset/
│
├── images/
│   ├── frame_000001.jpg
│   ├── frame_000002.jpg
│   ├── frame_000003.jpg
│   └── ...
│
├── labels/
│   ├── frame_000001.txt
│   ├── frame_000002.txt
│   ├── frame_000003.txt
│   └── ...
│
└── metadata/
    └── dataset_info.txt
images/

Contains RGB image frames extracted from traffic videos captured in Indian urban environments.

labels/

Contains object annotations in YOLO format corresponding to each image frame.

metadata/

Contains additional dataset information such as class labels, frame statistics, and annotation descriptions.

3. Annotation Format

Annotations follow the YOLO object detection format, where each line in the label file corresponds to one object instance in the image.

YOLO Annotation Format
<class_id> <x_center> <y_center> <width> <height>

Where:

class_id – Integer representing the object class

x_center – Normalized x-coordinate of the bounding box center

y_center – Normalized y-coordinate of the bounding box center

width – Normalized bounding box width

height – Normalized bounding box height

All coordinates are normalized between 0 and 1 relative to image dimensions.

4. Object Classes

The dataset includes annotations for the following road user classes:

Class ID	Class Name
0	Vehicle
1	Cyclist
2	Pedestrian

These classes represent the most common road users encountered in urban Indian traffic scenes.

5. Intended Tasks

The dataset is suitable for multiple computer vision and autonomous driving research tasks, including:

Object detection of heterogeneous road users

Multi-agent trajectory prediction

Motion forecasting in unstructured traffic scenes

Road user interaction modeling

Autonomous driving perception research

The dataset can also be used as input for trajectory extraction pipelines used in motion prediction frameworks.

6. Data Collection and Preprocessing

The dataset was constructed using the following pipeline:

Traffic videos were collected from urban Indian road environments.

Videos were converted into frame-level RGB image sequences.

Road users were annotated using a semi-automatic annotation pipeline.

Bounding boxes were manually verified to ensure annotation quality.

Annotations were converted into YOLO format for compatibility with modern object detection frameworks.

This pipeline enables the dataset to be easily integrated into training pipelines for deep learning-based detection and trajectory prediction models.

7. Usage Notes

Bounding box coordinates are provided in normalized YOLO format.

Each label file corresponds to a single image frame.

Frames may contain multiple road users of different classes.

The dataset can be used for both object detection and trajectory-based research.

8. Ethical Considerations

The dataset was collected from public road environments where individuals are visible as part of normal traffic scenes.

The dataset does not intentionally include any personally identifiable information. The dataset is intended strictly for academic and research purposes in the fields of computer vision and autonomous driving.

9. Limitations

This dataset represents a subset (Lite Version) of a larger dataset used in the research study.

Only bounding box annotations are provided.

Environmental metadata such as weather conditions, lighting variations, and time of day are not explicitly labeled.

The dataset may not represent all possible traffic scenarios.

10. License

This dataset is released for academic research purposes only.

Commercial use, redistribution, or modification for commercial applications is not permitted without permission from the authors.

11. Citation

If you use this dataset in your research, please cite the associated research work:

@dataset{indian_motion_forecasting_dataset,
  title={Indian Road Motion Forecasting Dataset},
  author={Akhil A Kumar},
  year={2026},
  note={Dataset for motion forecasting of heterogeneous road users in Indian traffic environments}
}
