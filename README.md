# FruitCounting
Apple Detection and Counting Using YOLOv5

# Problem Statement & Objective
We propose a Fruit Recognition System that analyses and processes images of fruits to identify them based on their type, maturity, or both. These techniques are simple for a human to perform unless he has no prior knowledge of the fruit. Computers, on the other hand, have failed miserably at these tasks. To implement the process of recognizing fruits, the procedure can be broken down into three key stages: 1) Image acquisition, which is accomplished by using image capture devices to acquire images of the fruit samples. 2) Fruit picture samples are restored, smoothed, or enhanced during pre-processing. According to some sources, pre-processing also include transforming raw photos to a predefined state (i.e., Grayscale or different color spaces). 3) Image Analysis examines the output of the preprocessing step in order to identify the fruit.

Once the fruits are recognized and located from the visual inputs, count of on-tree fruits can be obtained which helps in yield estimation. Yield estimation is crucial when it comes to improving field management and getting the outcome for the season’s harvest. Also, farmers can plan their next plantation strategy based on the previous yields. 

# Flowchart for the Proposed System

![image](https://user-images.githubusercontent.com/73229846/180719707-e8a8c2a3-01ba-4e44-a946-8758b31a38bb.png)

We use YOLOv5 for detection and obtain the count of apples from images sourced from an orchard.

# Comparison of different versions of YOLOv5

Amongst various versions of the YOLOv5, we have trained three models and evaluated them on the basis of their precision, recall and mAP scores. The three models are YOLOv5n, YOLOv5s and YOLOv5x. The following table shows the evaluation scores of the three models trained on our custom dataset.

Model   |Precision|	Recall |	mAP
YOLOv5n |	0.588   |	0.617  |	0.588
YOLOv5s |	0.648   |	0.595  |	0.626
YOLOv5x |	0.624   |	0.564  |	0.597

Thus, an inference of our experiment of training and evaluating the three versions, we found YOLOv5s to be giving us the best results on our dataset as per the mAP score. The higher the mAP score, better the model is considered.

# Results

We have tested our custom trained YOLOv5s on unseen images from the dataset acquired from an apple orchard. These are some samples from the test results:

![image](https://user-images.githubusercontent.com/73229846/180720771-cc65149a-3762-438c-90c4-41694aeee3fb.png)

![image](https://user-images.githubusercontent.com/73229846/180720817-daa2cb44-ace1-4a15-8acc-4cf3bd31b149.png)
                           
![image](https://user-images.githubusercontent.com/73229846/180720960-508caa31-b6fb-4818-910e-1a7c463bcb17.png)
                           
![image](https://user-images.githubusercontent.com/73229846/180720989-34481c78-29a9-482b-96b3-961086a691b6.png)

# Analysis

The images in the result section depict the achievement of our objectives. The first image, shows the detection in the bright illumination condition and the distance of the tree from the camera is a little less. The second image, has dull lighting conditions and distance of the trees from the camera has increased as seen in the previous image. The third and fourth images, have bright illumination, the distance of trees from the camera is fairly large and there are apples fallen on the ground as well. The results show that the model YOLOv5s suits our requirements and fulfills the objectives of our project.

The training metrics are depicted in the graph below. The graphs show the variation of loss across the epochs and the precision and recall values curve across the training epochs.

![image](https://user-images.githubusercontent.com/73229846/180721397-7a89e768-e4fd-4f59-aca9-f7460807dbde.png)
                            
![image](https://user-images.githubusercontent.com/73229846/180721596-3fd08cd3-9107-440e-9b8e-0d104fabd3b3.png)

The above figure, shows the F1 Curve for the model, which represents that the precision and recall are normalized best at confidence value 0.440.

![image](https://user-images.githubusercontent.com/73229846/180721866-b015d332-253f-4849-a174-143409a05a2c.png)
                            
The above figure, shows the precision value peaks at 1.0 at the confidence value of 0.834. 

![image](https://user-images.githubusercontent.com/73229846/180722117-618b3243-2a9a-4342-9cac-7b218796cb24.png)

Similarly, this figure shows the recall value of 0.89. 

![image](https://user-images.githubusercontent.com/73229846/180722305-7fb7e159-0a26-4f92-83a6-1061fa041ba6.png)       

This is the confusion matrix for the model which the depicts the true positives, false positives, true negatives and false negatives values predicted by the model.

# Conclusion

We discussed work done in fruit detection and counting. All the above-mentioned studies were successful in the detection of respective fruits in certain conditions. Most of the studies discussed covered fruit detection under various illumination and occlusion conditions except for a few. Some studies detected and counted fruits with high precision and covered all the challenging aspects while some studies only performed detection and some of them did not address occlusion conditions along with failing to detect or count all of the fruits present in the input image or video. 
