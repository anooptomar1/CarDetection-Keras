# CarDetection-Keras
"Car Detection" is trained in Keras using Tensorflow as back-end. It's taking an image as input and it  
gives a binary decision whether a car is present in the image or not. It's a Dense Neural Network. After train, converting the .h5 model
into .mlmodel to use in Xcode. (Please check the CarDetection-iOS project for that :  https://github.com/ashislaha/CarDetection-iOS ).

Training Data set is uploaded in https://drive.google.com/drive/folders/0B0QC-w3ZqaT1RzlGeGtYeVE2cTA . Put the data set into your working 
directory to train the model. It contains around 1500 training data & 100 test data where both car & non-car images are present.

Used both Convolutional Neural Network(CNN) & Dense Neural Network(DNN) to train the model. 

CNN gives 99.5% accuracy on Training data & 85.7% on Test data.
DNN gives 96%   accuracy on Training data & 86% on Test data.

Used Metrics to train in CNN : loss='binary_crossentropy', metrics=['accuracy'], optimizer='adadelta'

Used Metrics to train in DNN : loss='binary_crossentropy', metrics=['accuracy'], optimizer='rmsprop'

CNN TRAIN RESULTS : 

1403/1403 [==============================] - 15s - loss: 0.6524 - acc: 0.6436 - val_loss: 0.9084 - val_acc: 0.0000e+00

Epoch 2/25
1403/1403 [==============================] - 16s - loss: 0.4943 - acc: 0.6807 - val_loss: 1.8831 - val_acc: 0.1859

Epoch 3/25
1403/1403 [==============================] - 17s - loss: 0.4469 - acc: 0.8054 - val_loss: 1.2435 - val_acc: 0.4936

Epoch 4/25
1403/1403 [==============================] - 17s - loss: 0.4180 - acc: 0.8460 - val_loss: 1.2767 - val_acc: 0.5321

Epoch 5/25
1403/1403 [==============================] - 17s - loss: 0.3950 - acc: 0.8589 - val_loss: 1.3212 - val_acc: 0.1987

Epoch 6/25
1403/1403 [==============================] - 16s - loss: 0.3745 - acc: 0.8646 - val_loss: 0.9387 - val_acc: 0.5321

Epoch 7/25
1403/1403 [==============================] - 16s - loss: 0.3486 - acc: 0.8781 - val_loss: 1.1476 - val_acc: 0.4615

Epoch 8/25
1403/1403 [==============================] - 16s - loss: 0.3289 - acc: 0.8988 - val_loss: 1.0224 - val_acc: 0.6026

Epoch 9/25
1403/1403 [==============================] - 16s - loss: 0.3077 - acc: 0.9166 - val_loss: 1.0229 - val_acc: 0.5962

Epoch 10/25
1403/1403 [==============================] - 16s - loss: 0.2598 - acc: 0.9187 - val_loss: 0.9742 - val_acc: 0.6154

Epoch 11/25
1403/1403 [==============================] - 16s - loss: 0.1989 - acc: 0.9237 - val_loss: 0.7049 - val_acc: 0.7436

Epoch 12/25
1403/1403 [==============================] - 17s - loss: 0.1671 - acc: 0.9430 - val_loss: 1.8158 - val_acc: 0.2885

Epoch 13/25
1403/1403 [==============================] - 18s - loss: 0.1479 - acc: 0.9501 - val_loss: 0.7246 - val_acc: 0.7308

Epoch 14/25
1403/1403 [==============================] - 18s - loss: 0.1328 - acc: 0.9551 - val_loss: 0.3967 - val_acc: 0.8526

Epoch 15/25
1403/1403 [==============================] - 18s - loss: 0.1128 - acc: 0.9658 - val_loss: 1.1458 - val_acc: 0.5641

Epoch 16/25
1403/1403 [==============================] - 17s - loss: 0.0941 - acc: 0.9786 - val_loss: 0.4958 - val_acc: 0.8141

Epoch 17/25
1403/1403 [==============================] - 19s - loss: 0.0869 - acc: 0.9793 - val_loss: 0.7014 - val_acc: 0.7564

Epoch 18/25
1403/1403 [==============================] - 19s - loss: 0.0693 - acc: 0.9829 - val_loss: 1.3635 - val_acc: 0.5513

Epoch 19/25
1403/1403 [==============================] - 18s - loss: 0.0591 - acc: 0.9865 - val_loss: 1.5397 - val_acc: 0.5321

Epoch 20/25
1403/1403 [==============================] - 18s - loss: 0.0535 - acc: 0.9922 - val_loss: 0.4658 - val_acc: 0.8526

Epoch 21/25
1403/1403 [==============================] - 18s - loss: 0.0422 - acc: 0.9886 - val_loss: 0.6229 - val_acc: 0.8013

Epoch 22/25
1403/1403 [==============================] - 18s - loss: 0.0359 - acc: 0.9929 - val_loss: 1.1915 - val_acc: 0.6603

Epoch 23/25
1403/1403 [==============================] - 19s - loss: 0.0324 - acc: 0.9929 - val_loss: 0.5470 - val_acc: 0.8333

Epoch 24/25
1403/1403 [==============================] - 18s - loss: 0.0265 - acc: 0.9943 - val_loss: 0.6891 - val_acc: 0.7885

Epoch 25/25
1403/1403 [==============================] - 17s - loss: 0.0246 - acc: 0.9950 - val_loss: 0.9546 - val_acc: 0.7179

238/238 [==============================] - 1s     
('\nTest accuracy:', 0.85714285614109842)


DNN TRAIN RESULTS : 

This is the accuray after trained by 50 epochs , almost 96% accurate on train data & on unknown test data 86.5% accurate

1559/1559 [==============================] - 1s - loss: 3.2284 - acc: 0.5843      
Epoch 2/50
1559/1559 [==============================] - 1s - loss: 0.6219 - acc: 0.6555     
Epoch 3/50
1559/1559 [==============================] - 1s - loss: 0.5822 - acc: 0.6748     
Epoch 4/50
1559/1559 [==============================] - 1s - loss: 0.5466 - acc: 0.7158     
Epoch 5/50
1559/1559 [==============================] - 1s - loss: 0.5378 - acc: 0.7261     
Epoch 6/50
1559/1559 [==============================] - 1s - loss: 0.5637 - acc: 0.7325     
Epoch 7/50
1559/1559 [==============================] - 1s - loss: 0.5088 - acc: 0.7498     
Epoch 8/50
1559/1559 [==============================] - 1s - loss: 0.4936 - acc: 0.7620     
Epoch 9/50
1559/1559 [==============================] - 1s - loss: 0.4763 - acc: 0.7806     
Epoch 10/50
1559/1559 [==============================] - 1s - loss: 0.4761 - acc: 0.7870     
Epoch 11/50
1559/1559 [==============================] - 1s - loss: 0.4780 - acc: 0.7851     
Epoch 12/50
1559/1559 [==============================] - 1s - loss: 0.4429 - acc: 0.7973     
Epoch 13/50
1559/1559 [==============================] - 1s - loss: 0.4191 - acc: 0.8063     
Epoch 14/50
1559/1559 [==============================] - 1s - loss: 0.4025 - acc: 0.8172     
Epoch 15/50
1559/1559 [==============================] - 1s - loss: 0.3982 - acc: 0.8185     
Epoch 16/50
1559/1559 [==============================] - 1s - loss: 0.3764 - acc: 0.8287     
Epoch 17/50
1559/1559 [==============================] - 1s - loss: 0.3763 - acc: 0.8326     
Epoch 18/50
1559/1559 [==============================] - 1s - loss: 0.3340 - acc: 0.8518     
Epoch 19/50
1559/1559 [==============================] - 1s - loss: 0.3490 - acc: 0.8448     
Epoch 20/50
1559/1559 [==============================] - 1s - loss: 0.3379 - acc: 0.8467     
Epoch 21/50
1559/1559 [==============================] - 1s - loss: 0.2957 - acc: 0.8672     
Epoch 22/50
1559/1559 [==============================] - 1s - loss: 0.2984 - acc: 0.8698     
Epoch 23/50
1559/1559 [==============================] - 1s - loss: 0.2772 - acc: 0.8801     
Epoch 24/50
1559/1559 [==============================] - 1s - loss: 0.2720 - acc: 0.8756     
Epoch 25/50
1559/1559 [==============================] - 1s - loss: 0.2553 - acc: 0.8890     
Epoch 26/50
1559/1559 [==============================] - 1s - loss: 0.2503 - acc: 0.8948     
Epoch 27/50
1559/1559 [==============================] - 1s - loss: 0.2546 - acc: 0.8820     
Epoch 28/50
1559/1559 [==============================] - 1s - loss: 0.2467 - acc: 0.8993     
Epoch 29/50
1559/1559 [==============================] - 1s - loss: 0.2597 - acc: 0.9006     
Epoch 30/50
1559/1559 [==============================] - 1s - loss: 0.2255 - acc: 0.9185     
Epoch 31/50
1559/1559 [==============================] - 1s - loss: 0.2272 - acc: 0.9051     
Epoch 32/50
1559/1559 [==============================] - 1s - loss: 0.2169 - acc: 0.9179     
Epoch 33/50
1559/1559 [==============================] - 1s - loss: 0.2009 - acc: 0.9307     
Epoch 34/50
1559/1559 [==============================] - 1s - loss: 0.1967 - acc: 0.9282     
Epoch 35/50
1559/1559 [==============================] - 1s - loss: 0.2119 - acc: 0.9211     
Epoch 36/50
1559/1559 [==============================] - 1s - loss: 0.1919 - acc: 0.9352     
Epoch 37/50
1559/1559 [==============================] - 1s - loss: 0.2073 - acc: 0.9288     
Epoch 38/50
1559/1559 [==============================] - 1s - loss: 0.1893 - acc: 0.9339     
Epoch 39/50
1559/1559 [==============================] - 1s - loss: 0.2120 - acc: 0.9301     
Epoch 40/50
1559/1559 [==============================] - 1s - loss: 0.1560 - acc: 0.9436     
Epoch 41/50
1559/1559 [==============================] - 1s - loss: 0.1803 - acc: 0.9352     
Epoch 42/50
1559/1559 [==============================] - 1s - loss: 0.1694 - acc: 0.9436     
Epoch 43/50
1559/1559 [==============================] - 1s - loss: 0.1909 - acc: 0.9371     
Epoch 44/50
1559/1559 [==============================] - 1s - loss: 0.1414 - acc: 0.9493     
Epoch 45/50
1559/1559 [==============================] - 1s - loss: 0.1431 - acc: 0.9525     
Epoch 46/50
1559/1559 [==============================] - 1s - loss: 0.1349 - acc: 0.9589     
Epoch 47/50
1559/1559 [==============================] - 1s - loss: 0.1633 - acc: 0.9525     
Epoch 48/50
1559/1559 [==============================] - 1s - loss: 0.1732 - acc: 0.9474     
Epoch 49/50
1559/1559 [==============================] - 1s - loss: 0.1404 - acc: 0.9615     
Epoch 50/50
1559/1559 [==============================] - 1s - loss: 0.1170 - acc: 0.9557     
 32/238 [===>..........................] - ETA: 0s('\nTest accuracy:', 0.86554621698475687)
