# VHRV: Very High-Resolution Benchmark Dataset for Vessel Detection 
VHRV (Very High Resolution Vessels) Dataset

![detecting_vessels](https://github.com/user-attachments/assets/6fcad456-6a94-4390-b868-94feacfaf726)

Welcome to the official repository for VHRV dataset, associated with our research article "VHRV: Very High-Resolution Benchmark Dataset for Vessel Detection" published in the Remote Sensing Applications: Society and Environment (RSASE) journal. To access our paper ---> **[VHRV Paper](https://authors.elsevier.com/a/1lWHP8M-mmzWZQ)** 

## **Dataset Details**

VHRV dataset, namely Very High-Resolution Vessels, constitutes a formative contribution to the field of computer vision, specifically addressing vessel detection practices from remote sensing imagery. This dataset has been thoughtfully built to meet the requirements of advancing research and development in object detection algorithms, particularly in the maritime context. Its purpose is to provide a versatile alternative, that contains consistent and rich content by adding more vessel types with having different scales, for deep learning models to detect opulent of ships under single vessel class in high-resolution remote sensing 
images.

- **Number of Total Images**: 1,502
- **Number of Total Vessel Instances**: 10,158
- **Spatial Resolution**: Ranges from 0.1 m to 0.25m
- **Image Resolution**: 4800x2886 pixels
- **Annotation Format**: YOLO
- **Annotation Style**: HBB (Horizontal Bounding Box)

![vessel_img_samples](https://github.com/user-attachments/assets/f1e9aa6b-fe2c-477a-a50c-53ae311ffda7)

Use of the Google Earth images must respect the ["Google Earth"](https://about.google/brand-resource-center/products-and-services/geo-guidelines/) terms of use. **All images and their associated annotations in VHRV dataset can be used for academic purposes only, but any commercial use is prohibited.**

### Download

VHRV dataset can be downloaded here ---> **[Download VHRV](https://drive.google.com/file/d/1Hf6XRlsAd-x97tVzGweZmLwRFzdk4TEv/view?usp=drive_link)**  .




## Deep Learning
To evaluate the effectiveness of the VHRV dataset, we conducted comprehensive experiments using both two-stage (R-CNN-based) and one-stage (YOLO-based) deep learning models. The results, as presented in our RSASE journal article, demonstrate the robustness of the dataset across various architectures. For reproducibility and further exploration, we provide the trained model weights used in these experiments.

#### Two-stage experiments (RCNN models) 

| Model                  | Backbone<br><sup>Type/Depth  | size<br><sup>(pixels) | mAP<sup>test<br>0.50 | mAP<sup>test<br>0.50:0.95 | mAP<sup>val<br>0.50 | mAP<sup>val<br>0.50:0.95 |
| -----------------------|------------------|-----------------------|-----------|--------|----------------------|---------------------------|
| [Faster R-CNN](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_faster_rcnn_r50_fpn_coco.pth)           | Restnet 50  |  1333x800             | 0.921     | 0.631  | 0.924                | 0.653                     |
| [Faster R-CNN](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_faster_rcnn_r101_fpn_coco.pth)          | Restnet 101 |  1333x800             | 0.933     | 0.631  | 0.925                | 0.648                     |
| [Libra R-CNN](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_libra_faster_rcnn_r50_fpn_coco.pth)         | Restnet 50  |  1333x800             | 0.928     | 0.643  | 0.919                | 0.659                     | 
| [Libra R-CNN](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_libra_faster_rcnn_r101_fpn_coco.pth)        | Restnet 101 |  1333x800             | 0.929     | 0.634  | 0.930                | 0.661                     | 
| [Cascade R-CNN](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_cascade_rcnn_r50_fpn_coco.pth)              | Restnet 50  |  1333x800             | 0.931     | 0.668  | 0.926                | 0.683                     |
| [Cascade R-CNN](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_cascade_rcnn_r101_fpn_coco.pth)           | Restnet 101 |  1333x800             | 0.925     | 0.657  | 0.925                | 0.677                     | 

R-CNN based algorithms have been implemented and evaluated in a unified code library MMDetection.

#### Single-stage experiments (YOLO models) 

| Model                     | size<br><sup>(pixels) | mAP<sup>test<br>0.50 | mAP<sup>test<br>0.50 | mAP<sup>val<br>0.50 | mAP<sup>val<br>0.50:0.95 | params<br><sup>(M) |
| --------------------------|--------------|-----------|--------|--------|----------------------|---------------------------|
| [YOLOv5x](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_yolov5x.pt)          |  1024         | 0.985     | 0.835  | 0.971     | 0.848         | 56.9               | 
| [YOLOv6l](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_yolov6l.pt)         |  1024         | 0.982     | 0.812  | 0.975     | 0.823         | 56.9               |
| [YOLOv7x](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_yolov7x.pt)         |  1024         | 0.988     | 0.832  | 0.979     | 0.846         | 56.9               | 
| [YOLOv8x](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_yolov8x.pt)        |  1024         | 0.978     | 0.828  | 0.975     | 0.844         | 56.9               |
| [YOLOv9c](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_yolov9c.pt)            |  1024         | 0.981     | 0.845  | 0.973     | 0.856         | 56.9               | 
| [YOLOv10x](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_yolov10x.pt)        |  1024         | 0.978     | 0.817  | 0.967     | 0.824         | 56.9               | 
| [YOLO11x](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_yolo11x.pt)        |  1024         | 0.981     | 0.835  | 0.972     | 0.852         | 56.9               |
| [YOLOv12x](https://github.com/buyukkanber/vhrv/releases/download/v1.0.0/vhrv_yolov12x.pt)           |  1024         | 0.984     | 0.844  | 0.974     | 0.854         | 56.9               | 

YOLO models were executed using their original source code libraries, with the exception of YOLOv12, which was implemented with Ultralytics adaptation.

## **Citation**

If you make use of the VHRV dataset, please cite our following paper: https://doi.org/10.1016/j.rsase.2025.101641


We make this dataset available for **academical purposes only**. You may not use or distribute this dataset for commercial purposes.


```bibtex
@article{BUYUKKANBER2025101641,
  title = {VHRV: Very High-Resolution Benchmark Dataset for Vessel Detection},
  journal = {Remote Sensing Applications: Society and Environment},
  pages = {101641},
  year = {2025},
  issn = {2352-9385},
  doi = {https://doi.org/10.1016/j.rsase.2025.101641},
  url = {https://www.sciencedirect.com/science/article/pii/S2352938525001946},
  author = {Furkan Büyükkanber and Mustafa Yanalak and Nebiye Musaoğlu},
  keywords = {Vessel detection, Ship dataset, Remote sensing images, Deep learning, Convolutional neural networks}
}
```

## **Contact**

For further information or any question, you can use the issues (https://github.com/buyukkanber/vhrv/issues) tab


