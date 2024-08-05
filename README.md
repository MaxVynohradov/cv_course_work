# Analysis of Military Aircraft Detection Dataset

Link: [https://www.kaggle.com/datasets/a2015003713/](https://www.kaggle.com/datasets/a2015003713/)
(it was single +/- big dataset of aircrafts that I found)

### The goal was:
- inspect some public Aircraft datasets, does them suitable for learning
- attemt to lear network on greyscale version of images (to use just 1 channel instead of 3)
- attemt to lear tiny neural network, to not consume a lot of resources
- attemt to use  out-of-box neural network, that suitable for small devices (with low resources) - MobileNetV3Small

### Implementations steps (Research):

1. [Step 1: analyse of dataset](Step_1_Intro_and_DS_Analys.ipynb.ipynb) .
   Conclusion: dataset is not really good
3. [Step 2: work with grayscale images and custom NN based on SeparableConv2D and GlobalAveragePooling2D](Step_2_grayscale_learning.ipynb) Conclusion:
    - Accuracy is bad  - near 25%, and according to graphics model overfit a little.  
    - Looks like 128x128 is to small size to make good prediction, 256x256 is quite better
    - Single channel make computation faster but in the same time accuracy lower. But in this case it make sense coz we do not want rely on colors
5. [Step 3: attempt to use MobileNetV3Small](Step_3_MobileNetV2_learning.ipynb)



### Plans TODO: 

1. Improve accuracy
2. Attempt to clean up data set
3. Try to use trained models on video
4. Try to use the same model on single channel images and regular 3 channels, to compare difference (not finished in the step 3)
5. Try to use TinyML approaches: [](https://blog.tensorflow.org/2021/05/building-tinyml-application-with-tf-micro-and-sensiml.html)
   