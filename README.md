# Perception-Self-Driving-Cars

## Road Segmentation (any FCN)
FCN model for road segmentation task. 

upsampling - nearst neighbours, interpolation, transpose convolution (learnable filter)

image classification network to segmentation network (image to int label convert image to image)

FCN 32 - Coarser structure in image 
FCN 16 - Finer structure in image 


##  2D object Detection (YOLO)
1. Anchor Boxes 
2. Intersection over union 
3. Bounding Box Prediction (by intersection over union using non max sepression)



## Object Tracking (Deep Sort - Deep Simple Onlne Real Time Tracking)
1. Get the bounding box prediction (Yolo for instance)
2. Kalman Filer [Future prediction] (ansumes a linear velocity model and gets the predictions according to  it. Outputs a probability distributionns). It gives score in mahalanobis. Oclusion can be a prblem. 
3. IOU matching
4. The matchiing in brute force is O(N! which is huge) so we use Hungerian Algorithm O(N^3)
5. Deep Appearance Descriptor uses CNN (Like given a person in different angles images it can say if it is the same person or a different person.) is gives score in cosine. 
6. Cascade matching 

Finally Track 

## Multi task learning (Image Segmentation and Depth Estimation)
weighted loss average for different tasks

