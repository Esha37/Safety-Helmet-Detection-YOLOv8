# Safety Helmet Detection Using YOLOv8

This project implements YOLOv8n object detection for workplace safety images.

Classes:
- person
- helmet
- head

Dataset split:
- Train: 105 images
- Validation: 30 images
- Test: 15 images

Training:
- Model: YOLOv8n
- Epochs: 30
- Image size: 640
- Batch size: 4
- Device: CPU

Test results:
- Precision: 0.820
- Recall: 0.418
- mAP@0.5: 0.467
- mAP@0.5:0.95: 0.263

The helmet class performed best. The head class performed weakly because it was underrepresented.
