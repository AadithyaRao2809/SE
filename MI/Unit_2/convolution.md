## CNN

Ann with convolution layers,pooling layers and fully connected(ann) layers.

### Why CNN?
- You can use ANN,but high computation cost.
- Overfitting cause you are capturing every single pattern
- Lose spacial information/arrangement info
![](../../Attachments/convolution-20230929.png)
why should the last part of the number 2 go to the first neuron? ANN problem

Cnn tries to extract simple edges first.
Convolution layers extract features
Filter moves generating features for conv layer

### Convolution

![](../../Attachments/convolution-20230929-1.png)
![](../../Attachments/convolution-20230929-2.png)
![](../../Attachments/convolution-20230929-3.png)
different filters to detect different edges
on this filter, lower 1's have weightage

Filter has NxN weights and one bias

In 3d one filter will give 2d, many will give those many output layers.

#### Padding
- We pad because the pixels on the corner for example shows up only once, but someother pixels show up more.
- We can pad to increase the occurances of those pixels.

#### Stride
- skip multiple inclusions of same pixel
- high level features you want
- computing easier



$$output=\lfloor{\frac{n-f}{s}\rfloor}+1$$

![](../../Attachments/convolution-20230929-4.png)
![](../../Attachments/convolution-20230929-5.png)

#### Problems with convolution
- memory
- ![](../../Attachments/convolution-20230929-6.png)
	1.5 GB

- translational invariance
	depends on where the feature is as filter if affected by pixel location

### Pooling
![](../../Attachments/convolution-20230929-7.png)
![](../../Attachments/convolution-20230929-8.png)
![](../../Attachments/convolution-20230929-9.png)
- max polling can enhance features
- Imagine different 9's ,if some feature of that 9 is in a slightly different pixel location, it will still get pooled in the same place.
- Control's overfitting 
- Eliminate low level details
- Always has a 2D kernel


### Normalization
![](../../Attachments/convolution-20230929-10.png)
	
### Dropouts
Cnn is like ann with dropouts
![](../../Attachments/convolution-20230929-11.png)
![](../../Attachments/convolution-20230929-12.png)
![](../../Attachments/convolution-20230929-13.png)