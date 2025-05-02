<img src="image/KDASmain.png" alt="KDAS" width="800"/>
# KookminUniv
Kookmin University Driving &amp; Autonomous System

## Introduction

To recognize traffic lights and traffic signs during autonomous driving, we adopted the YOLO object detection model.  
YOLO models learn distinctive features of objects, optimize weights through training, and perform real-time detection based on those weights.  
Among various YOLO versions, we selected **YOLOv8s**, which offers an excellent balance between computational speed and detection accuracy, making it ideal for real-time embedded applications.  
The trained PyTorch model was integrated into our system as a ROS2 node. Upon detecting objects, the node publishes the corresponding class IDs, which are then utilized by a MATLAB-based control system for decision-making.

---

## Dataset Structure

We constructed a custom dataset using QLab-generated images, specifically designed to train the model on five traffic-related classes:  
**roundabout**, **stop**, **crosswalk**, **yield**, and **red sign**.



---

## Test Results

Both quantitative evaluation metrics and qualitative visual inspection confirmed that the trained model achieves a level of performance suitable for real-world application.  
The detection accuracy and consistency across various scenarios verified the reliability of the deployed model.

---

## Additional Files

We have provided the following files as part of this repository:
- **ROS2 inference node** implementation
- **Trained model weights** (`model.pt`)
- **Training scripts** used for model development
- **Dataset** used for model learning
