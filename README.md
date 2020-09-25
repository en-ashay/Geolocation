# Geolocation
Working on geolocation data set to develop a research paper thesis


[Visualize]..(https://heartbeat.fritz.ai/class-activation-maps-visualizing-neural-network-decision-making-92efa5af9a33)

https://bair.berkeley.edu/blog/2020/04/23/decisions/

## Papers

https://sci-hub.tw/https://doi.org/10.3390/rs10040568#

https://arxiv.org/pdf/1910.01279.pdf

https://www.researchgate.net/deref/https%3A%2F%2Fgithub.com%2Ftabayashi0117%2FScore-CAM%2Fblob%2Fmaster%2Fgradcamutils.py

https://arxiv.org/pdf/2007.00649v1.pdf

https://github.com/yosinski/deep-visualization-toolbox



# Info

#### Key Findings:

1. Three data sets out of which 2 are fixed sizes and one has subparts.
     AID dataset can give data based on the country and other filters so are variable in size.

2. Authors use Feature Fusion methodology i.e.
     Extracting features from the same image multiple times using more than one Deep Neural Network and then combining those features.
      In a way, it is similar to the collection of data in different conditions as we get some variation in total input feature values of the data for each case.

3. the authors then use a simple CNN network to make predictions based on these features.




#### How to proceed :

1. Study about the difference in features extracted from various networks and for what they are good.for.
( Maybe Survey papers can help for these)

e.g. say architecture A is good at detecting colours in an image and arch. 2 at detecting boundaries. Combines they can better differentiate a field for the road as they have two features as compared to using one network.

2. Find out difficulties in current models like what feature mainly drives their prediction or what features are they bad at predicting.

3. How to combine various obtained features I.e. deciding on ensembling techniques to boost the performance? Like using class probabilities or partial predictions, etc.

Concepts from Supervised learning Stacked ensemble classifiers can be used here.

4. Deciding the final meta classifier for the prediction. 

5. Also what kind of data augmentation needs to be applied?



## [Reserach_gate_answer](https://www.researchgate.net/post/What_are_the_best_CNN_feature_visualization_techniques)

I dig myself into CNN explainability in the past months. Most of the projects are suitable only one purpose or damn slow per image. I found an implementation of GradCAM, GradCAM++ and ScoreCAM from a Japanese developer on Github. It is awesome, no dependencies and very easy to integrate into your Python stack. And these methods can be run on a larger scale on many images in a reasonable amount of time:
https://github.com/tabayashi0117/Score-CAM/blob/master/gradcamutils.py
But it is for Python-Tensorflow (Keras). I can't help in other frameworks-programming languages.
Other notes:
- SHAP APIs are not straightforward to use and that method is damn slow. Not very useful to do quick iterations of your work.
- Backprop-based techniques got criticism for being not really working.
- LIME got similar criticism.
- For saliency maps, I did not find them useful at all.
Any other methods are very much WIP, no public software or you have to implement yourself. I found the above mentioned CAM-based methods, easy to integrate, more or less working and they are relative quick per image.

# Score cam for visualization
[Official_CVPR](https://openaccess.thecvf.com/content_CVPRW_2020/papers/w1/Wang_Score-CAM_Score-Weighted_Visual_Explanations_for_Convolutional_Neural_Networks_CVPRW_2020_paper.pdf)
