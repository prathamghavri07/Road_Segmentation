## Road Segmentation on Indian Roads
Performed road segmentation using the IDD dataset with a U-Net architecture, targeting 30 different classes (e.g., sky, road, vehicle, pole) for masking drivable regions in autonomous driving. Achieved an inference time of 2.4 ms on an NVIDIA Tesla P100 GPU

## Dataset
Credits
IDD: A Dataset for Exploring Problems of
Autonomous Navigation in Unconstrained Environments
https://idd.insaan.iiit.ac.in/

## Libraries and Framework 
PyTorch,PIL,OpenCv,Matplotlib,Numpy,Pandas,Json

## Understanding the Data
Two Datatypes gtFine_polygons.json and img
the structure of Json file was 
"imgHeight": 964, "imgWidth": 1280, "objects": [
  {
      "date": "13-Apr-2018 15:51:45",
      "deleted": 0,
      "draw": true,
      "id": 37,
      "label": "vegetation",
      "polygon": {coordinates of the corresponding polygon of the label}

Data Distribution
![image](https://github.com/user-attachments/assets/160e5c59-2b56-4638-b08f-ae29e37fcd35)


## Data Preprocessing
Creating Masks for Drivable regions using Json Files
![image](https://github.com/user-attachments/assets/5f65872d-1685-45ec-9e58-b681e18521fc)
![image](https://github.com/user-attachments/assets/fd9105ea-e2ce-4b16-b06e-6f1d3c3f7e35)

- Resizing Image and Binary Masks to (256,256)
- Batch_size=16

## Training and Inference
U-Net Architecture with loss criteria BCEWithLogitsLoss and Adam Optimisation
![image](https://github.com/user-attachments/assets/746aeced-a991-48e7-9de8-ddadd73e1202)

Inference time using NVIDIA Tesla P100 GPU is 2.4 ms
![image](https://github.com/user-attachments/assets/87e18b40-dc1c-488f-a52e-75f068d4b58d)
![image](https://github.com/user-attachments/assets/f5709588-e57d-41de-ab16-b0047654b909)



