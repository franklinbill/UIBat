# ![logo](https://github.com/UIBat/UIBat/blob/main/UIBat-logol-1.png) 

# UIBat
A tool to automatically detect, localize, and repair the UI display issues in Android apps.<img style="width:40px" src="https://github.com/UIBat/UIBat/blob/main/UIBat-logol-2.png"> 


## Issues Detection, Localization and Repair Approach (./UIBat/)
*UIBat* is named as UIBat as it is like a bat to effectively detect, localize and repair the UI display issues. And UIBat (nocturnal like bat) can complement with conventional automated program repair (diurnal like bird) for ensuring the robustness of the Mobile GUI. Automatically detect, localize and repair UI display issues based on the screenshots of the mobile apps under test.
* *UIBat.rar* : source code of UIBat.

Due to the space limitation of our paper, we omitted some details of our model in the detection part of the UI display issue. We will describe the model in detail here.

Given the input UI screenshot, we convert it into a certain image size with fixed width and height as w * h, and the image is normalized. Then the screenshot is input into the convolution neural network ResNet50. The Convolutional layer's parameters consist of a set of learnable filters. The purpose of the convolutional operation is to extract the different characteristics of the input (i.e., feature extraction). After the convolutional layer, the screenshots will be abstracted as the feature graph. 
However, with the network depth increasing, accuracy gets saturated and then degrades rapidly, it is easy to appear the vanishing / exploding gradients problem and degradation problem. Because the gradient propagates back to the previous layer, repeated multiplication may make the gradient infinitesimal. As a result, with the deeper layers of the network, its performance tends to be saturated or even rapidly decline. In order to solve this problem, ResNet50 introduces the concept of residual error to solve this problem. ResNet50 solves the degradation problem by introducing a deep residual learning framework. Instead of making each layer directly fit a desired underlying mapping, it explicitly matches these layers with a residual mapping. 

After obtaining the feature map through ResNet50, we input the feature map into Region Proposal Network (RPN) module. The RPN takes the feature map (of any size) as input and outputs a set of rectangular 3 object proposals, each with an objectness score. Then, a 3x3 slide window is used to traverse the whole feature map. In the process of traversing, nine anchors are generated according to rate and scale (1:2, 1:1, 2:1) in each window center. Then, full connection is used to classify each anchor (foreground or background) and preliminary bounding boxes expression. Then the bounding box expression is used to modify the anchors to obtain accurate proposals. 

According to the feature map obtained by the feature extraction module and proposal obtained by RPN module. Input it into the ROI pooling layer to calculate the proposal feature maps. Finally, the proposal feature maps are input into the classification module, and the specific category (such as component occlusion, missing image, etc.) of each proposal is calculated through the fully connected neural networks (FC) and softmax layer, and the probability vector is output. At the same time, the position offset of each proposal is obtained by using bounding box expression again, which is used to regression more accurate target detection frame.

We implement our model based on the PyTorch framework. 
The model is trained in an NVIDIA GeForce RTX 2060 GPU (16G memory) with 100 epochs for about 8 hours.



<!-- ![Overview of UIBat](https://github.com/UIBat/UIBat/blob/main/overview-11.png)-->

<div align=center>
<img src="https://github.com/UIBat/UIBat/blob/main/overview-v2-11.png" height="560px"/>
</div>

we use 6000 manually labeled buggy screenshots and 6000 non-buggy screenshots. They have obvious visual differences, as shown in below Figure, so can be distinguished with computer vision technologies. The few false positives don't influence the follow-up fixing, i.e., no template is matched.

<div align=center>
<img src="https://github.com/UIBat/UIBat/blob/main/5-kind-bug.png" height="260px"/>
</div>

# UIBat website

We develop the UIBat platform for automatic detecting, localizing and repairing the UI display issue. 
**Please note** that we are very sorry that the domain name(url link) and server used by our UIBat now contain personal information. For the requirements of **double-blind review**, we give the demo video and hide the domain name information. After the blind review, we will update GitHub with the domain name(the url link) of UIBat. 
Up to now, UIBat detects **129 previously undetected UI display issues from GitHub**, which again indicates the prevalence of UI display issues, and the necessity for the auto-repair. UIBat can repair 121 (94%) of them. For the **121 submitted pull requests**, **92 of them are successfully merged** by developers, while the remaining are still pending (**none of them is rejected**).
We provide demo video as shown in below video for helping the understanding. The video link is: https://youtu.be/1qbPwKLDspA

