# Detection-and-Counting-of-Wheat-Heads-Under-Various-Image-Conditions-Source-Locations

### By: Jonathan Rasmussen

## Description of the Problem

The average global wheat production in the world from 2008 - 2013 reached
approximately 680 million tonnes [1]. The ability to easily estimate the health
and growth potential of wheat of is important to farmers [2]. The quantity of
wheat heads, the spikes on top of the wheat stem that grows when the plants
reached maturity, is a useful proxy for crop health [3]. Given the quantity of
wheat in a field, human counting is impractical and prone to error [3]. There is
a need to develop an image detection system that could detect the number of
wheat heads in images of vast fields of wheat accurately. Developing a solution
for this problem will use aspects taught by the course including data processing & 
neural networks.

Given the importance of wheat as a crop there is already a significant body
of research applying machine learning to evaluating crops. Convolutional Neural
Networks (CNNs) are of particular interest and many researchers have worked
to apply them [2, 3, 4].Hasan et al. in 2018 designed a RCNN (regions based
CNN) system for identifying different phenotypes of wheat based on density of
wheat heads[4]. In their study they wanted to create a model that was robust
to changes in illumination and high amount of occlusion of target features [4].
Madec et al. in 2019 investigated applying an RCNN and TasselNet system
to counting wheat heads [3]. In their work they found that while both methods
could effectively identify wheat heads the Faster-RCNN system was more effective [3]. However Faster-RCNN system required high resolution images (0.
mm) which represents a potential limitation of the technique [3]. Sadeghi-Tehran et al. in 2019 write about their development of the DeepCount system
[2]. This system created clusters of ‘superpixels’ using simple linear clustering
to derive relevant features and then used a CNN to identify wheat heads [2].
The model was faced with wheat in various stages of maturity, high occlusion of
features and varied illumination conditions [2].Tan et al.recently published a
paper describing their algorithm "EfficientDet" [5]. This algorithm was shown
to achieve more accurate and less computationally expensive object detection
when compared to other CNN based systems [5]. This may represent an opportunity for it to be incorporated into a system for counting wheat heads. Given
the strong background of research into both wheat detection and computerized
object recognition there are many opportunities to build off of past work.

There are a few important challenges to machine learning systems that will
need to be addressed. As is typical for image detection machine learning, the
concern of over-fitting the model is present. The project will be trained on four
separate datasets of images and careful observation of metrics will be conducted
in order to minimize the possibility of over-fitting. To further train the model,
image manipulation techniques, such as rotations, will be employed in order
to improve model performance. Several challenges highlighted for this specific
project is as follows. Several of the images may have overlap between different
heads of wheat [3]. This could affect the algorithm resulting in an increase of
false negative detection results [3]. With careful preprocessing, vetting procedure, and labeling processes this challenge may be resolved. Another major
challenge for image analysis programs is being confused by background effects
[3]. For example, a possible flaw is a program trained on pictures of wheat on a
sunny day getting inaccurate results on images that include a cloudy sky. The
datasets will have a large variation in weathers, climates, soil types, and wheat
phenotype in order to mitigate the affect any variation between images may
have on the performance of the model.

## Solution to the Problem

The aim of this project is to develop a CNN algorithm in order to detect the
number of wheat heads in a given image. Specifically the proposed algorithm will
be a Faster-RCNN. The Faster-RCNN method has demonstrated effectiveness
in wheat head detection. [2, 3, 4]. Our work project will further investigate
other CNN methods. In particular, the recently published EfficientDet method
of compound scaling to improve the performance of CNN algorithms will be
implemented and compared to determine the optimal algorithm [5]. Several
preprocessing methods must be implemented to the dataset prior to training the
algorithm. Due to it’s size relative to the the other datasets, the format seen
in the Global Wheat Dataset will be the standard approach for this project.
Therefore the three other datasets to be used in this project must be processed
in order to adhere and be applicable to the training of the algorithm. Several
other preprocessing methods, such as flips, rotations other methods will be used
to improve performance of the algorithm. The performance of the algorithm
will be determined by evaluating the precision of the algorithm. The precision
of the algorithm is the number of true positive outcomes compared to the all
ground truth objects.

![equation](https://latex.codecogs.com/gif.latex?Precision%20%3D%20%5Cfrac%7BTrue%20Positives%7D%7BTrue%20Positives%20&plus;%20False%20Positives%7D)

As commented above we plan to use multiple datasets. This includes the
Kaggle competition data (available: [http://www.global-wheat.com/).](http://www.global-wheat.com/).) This is a
set of high resolution 1024 by 1024 pixel images. There is the SPIKE dataset
(available: https://sourceforge.net/projects/spike-dataset/). This was used by
Hasan et al. and contains manually annotated images of wheat [4]. The Wheat
Ears Detection dataset used by Madec et al. will be used as well (available:
https://github.com/simonMadec/Wheat-Ears-Detection-Dataset) [3]. This data
set is 236 high resolution RGB images of wheat. The final dataset that will be
used is the Sadeghi-Tehran et al. (available: https://ckan.grassroots.tools/) [2]
This contains colour high resolution images of wheat.


## References

[1] Peter R. Shewry and Sandra J. Hey. “The contribution of wheat to human
diet and health”. In:Food and Energy Security4.3 (2015), pp. 178–202.
doi:10.1002/fes3.64. eprint:https://onlinelibrary.wiley.com/
doi/pdf/10.1002/fes3.64.url:https://onlinelibrary.wiley.com/
doi/abs/10.1002/fes3.64.

[2] Pouria Sadeghi-Tehran et al. “DeepCount: In-Field Automatic Quantifica-
tion of Wheat Spikes Using Simple Linear Iterative Clustering and Deep
Convolutional Neural Networks”. In:Frontiers in Plant Science10.Septem-
ber (2019), pp. 1–16.issn: 1664462X.doi:10.3389/fpls.2019.01176.

[3] Simon Madec et al. “Ear density estimation from high resolution RGB
imagery using deep learning technique”. In:Agricultural and Forest Mete-
orology 264.October 2018 (2019), pp. 225–234.issn: 01681923.doi:10.
1016/j.agrformet.2018.10.013.url:https://doi.org/10.1016/j.
agrformet.2018.10.013.

[4] Md Mehedi Hasan et al. “Detection and analysis of wheat spikes using
Convolutional Neural Networks”. In:Plant Methods14.1 (2018), pp. 1–
13.issn: 17464811.doi:10.1186/s13007- 018- 0366- 8.url:https:
//doi.org/10.1186/s13007-018-0366-8.

[5] Mingxing Tan, Ruoming Pang, and Quoc V. Le.EfficientDet: Scalable and
Efficient Object Detection. 2019. arXiv:1911.09070 [cs.CV].


