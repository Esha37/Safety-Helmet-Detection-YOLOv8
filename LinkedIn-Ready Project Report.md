# LinkedIn-Ready Project Report

## Project Title

**Safety Helmet Detection System Using YOLOv8**

## Project Overview

As part of the AIRI Team PITB AI Internship Task 1, I developed an end-to-end Computer Vision object-detection system for workplace safety images. The system uses YOLOv8n to detect three annotated object classes: **person, helmet, and head**. The project covered dataset preparation, Pascal VOC-to-YOLO annotation conversion, dataset splitting, model training, evaluation, inference on unseen images, and error analysis. The final system produces bounding boxes, class labels, and confidence scores on test images.

## Tools and Technologies

- Python
- Google Colab
- Google Drive
- YOLOv8n
- Ultralytics
- PyTorch
- OpenCV
- NumPy and Matplotlib
- Pascal VOC XML and YOLO TXT formats

## Dataset and Training

A subset of 150 images from the Hard Hat Detection dataset was used. The data was divided into 105 training images, 30 validation images, and 15 test images. The model was trained for 30 epochs at 640-pixel image size with batch size 4 on CPU because GPU access was unavailable during the final training run.

## Results

The final test results were:

| Metric | Result |
|---|---:|
| Precision | 0.820 |
| Recall | 0.418 |
| mAP@0.5 | 0.467 |
| mAP@0.5:0.95 | 0.263 |

The helmet class performed best with a test mAP@0.5 of **0.779**. Person detection achieved a test mAP@0.5 of **0.599**. The head class performed poorly because it was underrepresented in the selected data and appeared in only a small number of test images.

## Error Analysis

The main errors included false negatives, loose or overlapping person boxes, missed small helmets, low-confidence predictions in difficult scenes, and weak head predictions. Crowded scenes, occlusion, low-light images, small objects, complex backgrounds, and class imbalance contributed to these errors.

## What I Learned

- How to define a real-world Computer Vision object-detection problem.
- How to organize images, annotations, and train/validation/test splits.
- How Pascal VOC XML annotations are converted into YOLO TXT format.
- How YOLO class IDs and normalized bounding-box coordinates work.
- How to train a pretrained YOLOv8 model in Google Colab.
- How to evaluate a detector using precision, recall, and mAP.
- Why annotation quality, class balance, and error analysis are important for model performance.

## Future Improvements

Future work will include collecting more balanced examples for the head class, reviewing annotations more extensively, adding difficult crowded and low-light images, training with GPU resources, testing a larger YOLO model, and deploying the detector as a Streamlit application or real-time video/CCTV demo.

## LinkedIn Post Draft

Today, I completed an end-to-end Computer Vision project as part of the **AIRI Team PITB AI Internship Task 1**.

I built a **Safety Helmet Detection System using YOLOv8**. The project covered the complete AI workflow:

- Problem selection
- Dataset preparation
- Annotation-format conversion
- YOLO-format dataset organization
- Model training on Google Colab
- Model evaluation
- Inference on unseen images
- Error analysis
- Final documentation

The model detects **person, helmet, and head** classes and produces bounding boxes with confidence scores. On the test set, it achieved a precision of **0.820**, recall of **0.418**, and mAP@0.5 of **0.467**. The helmet class performed best, while the head class requires more balanced training examples.

This project helped me understand that successful Computer Vision systems depend not only on the model architecture, but also on clean data, consistent annotations, class balance, proper evaluation, and systematic error analysis.

**Tools used:** Python, Google Colab, Google Drive, YOLOv8, Ultralytics, PyTorch, OpenCV, NumPy, and Matplotlib.

#ComputerVision #DeepLearning #YOLOv8 #ArtificialIntelligence #MachineLearning #Python #AIRI #PITB #AIInternship

> Note: The source dataset annotations were converted and visually reviewed. They were not completely redrawn manually from scratch; additional manual annotation would be required if the internship evaluator enforces that criterion strictly.

## Submission Link

Google Drive project folder: https://drive.google.com/drive/folders/1cZzOlLsU_AOmuWZEcUkVJ3Z_muUkuSoW?usp=drive_link

## Submission Note

The project is submitted through Google Drive. The folder contains the Colab notebook, submission ZIP, PDF report, error analysis, README, and requirements file.
