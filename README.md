# Captcha-Recognition-by-CNN 
### Mo Wu (mw3774)  Mingdi Han (mh4928)

In this project, we are going to implement the CAPTCHA recognition by building and training a machine learning model. Verification code (GAPTCHA) is an effective tool to distinguish whether a user is a computer or a human. 

<img width="224" alt="屏幕快照 2019-05-11 下午7 25 07" src="https://user-images.githubusercontent.com/42648807/57575957-401f9600-7423-11e9-9838-1680656f3e78.png"><img width="340" alt="屏幕快照 2019-05-11 下午7 28 46" src="https://user-images.githubusercontent.com/42648807/57575959-43b31d00-7423-11e9-877c-7e4b24001d8e.png">

There are two verification codes shown in the figure above. The code in green box is a classic one, this type of codes can be recognized by performing character segmentation and identification (SVM). The effect of this recognition method depends heavily on the effect of image segment, however, due to the distortion of the letters in the pink box, a rectangular window is hard to split characters and it's time-consuming. We will try to build a CNN model considering the picture as a whole part and recognizing directly to solve this problem in this project.
## Data
About getting data, the number of characters and letters in one captcha is 4, then there are 4*62 outputs including captital letters and small letters. In order to gain high accuracy in CNN model, a large amount of data will be needed to train. There are two ways to generate data, one is to download captcha at one time and we can use it for many times, the other one is to define a data generator to get captcha by using GPU and trainnig the model at the same time which will be convienient since we can have infinite pictures. But we still provide basic data source in the above folder if you like to try (contains 3000 captchas so accuracy will be limited).
## Model
We train the CNN model on GPU with three convolution layers having approximatly 93% accuracy (it would be higher if trains longer) and save it including four files. Also there is an .ipynb from colaboratory if you want to see the whole executive process.
